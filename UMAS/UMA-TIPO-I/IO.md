# VARIABLES DE CONTROL

### ENTRADAS

> `BI_1`    **ST_SF** 	    [ *ACTIVO* / *INACTIVO* ]	Estado de operación de Ventilador de suministro
>
> `BI_2`	**IN_FT1**      [ *SUCIOS* / *LIMPIOS* ]	Estado de prefiltros
>
> `BI_3`	**IN_FT2** 	    [ *SUCIOS* / *LIMPIOS* ]	Estado de filtros de bolsa
>
> `BI_4`	**ST_INC**      [ *ALARMA* / *NORMAL* ]		Estado de alarma de detección de incendios
>
> `AI_5`  	**IN_SAT**      [ *°C* ]				    Temperatura de suministro de aire
>
> `AI_6`  	**IN_RAT**	    [ *°C* ]				    Temperatura de retorno de aire
>
> `AI_7` 	**IN_SPT** 	    [ *°C* ]				    Temperatura de cuarto
>
> `AI_8` 	**ST_HCV**      [ *%* ]					    Estado de apertura de válvula de agua caliente
>
> `AI_9` 	**ST_CCV** 	    [ *%* ]					    Estado de apertura de válvula de agua helada
>
> `BI_12`	**MANUAL**	    [ *ON* / *OFF* ]			    Arranque manual de sistema desde tablero

### SALIDAS

> `BO_1`	**SS_SF**  	    [ *ARRANQUE* / *PARO* ]		Arranque de ventilador de suministro de aire
>
> `AO_1`  	**CN_SF**	    [ *%* ]					    Control de velocidad de ventilador de suministro de aire
>
> `AO_2`  	**CN_HCV**      [ *%* ]					    Control de apertura de válvula de agua caliente
>
> `AO_3`  	**CN_CCV**  	[ *%* ]					        Control de apertura de válvula de agua helada

## CODIGO

ARRANQUE MANUAL DE SISTEMA
	
```bash
	IF MANUAL == ON AND P_MANUAL == OFF AND ACT_MAN == OFF THEN ACT_MAN = ON ALSO P_MANUAL = ON
	IF MANUAL == ON AND P_MANUAL == OFF AND ACT_MAN == ON THEN ACT_MAN = OFF ALSO P_MANUAL = ON
	IF MANUAL == OFF THEN P_MANUAL = OFF
```

	// BLOQUE 1: SENSORES Y SETPOINTS 
	
		CALL SENSORES
		
		CALL SETPOINTS
		
		
	// BLOQUE 2: TIMERS 
	
		IF RES_BIT_37 == ON AND RES_BIT_242 = OFF THEN CALL TIMERS ALSO RES_BIT_242 = ON
		IF RES_BIT_37 == 0FF THEN RES_BIT_242 = OFF

		
	// BLOQUE 3: TEST DE SISTEMA
		IF SS_TEST == ON THEN CALL TEST_SISTEMA ALSO JUMP FINAL 
		
		
	// BLOQUE 4: PARO POR ALARMA
	
		// ALARMA GENERAL
			IF AL_VSUM == ON OR AL_TM == ON OR AL_FT == ON THEN AL_SYS = ON ELSE AL_SYS = OFF	
	
		// RESET ALARMA CRITICA
			IF RESET_ALM == ON THEN ALM_SF = OFF ALSO RESET_ALM = OFF
		
		// ALARMA CRITICA
			IF ALM_SF == ON THEN ALM_PARO = ON ELSE ALM_PARO = OFF
		
			IF ALM_PARO == ON THEN CALL PARO_ALARMA ALSO JUMP FINAL
					

	// BLOQUE 5: CONTROLES DE DEMANDA DEL SISTEMA
	
		// PERMISIVO PARA ACUMULADOR DE GENERADORES DE DEMANDA [ RES_BIT_241 ]
			IF RES_BIT_37 != RES_BIT_240 THEN RES_BIT_241 = ON ALSO RES_BIT_240 = RES_BIT_37 ELSE RES_BIT_241 = OFF
	
		// CONTROL DE DEMANDA DE TEMPERATURA (ZONA)
			PI3_VAR = TEMP
			PI3_SP = SP_SPT
			CALL PI3
			// CONVERSION DE DEMANDA DE TEMPERATURA AREA A SETPOINT DE SUMINISTRO DE AIRE
				Y0 = Y1 - Y2
				X0 = X1 - X2
				M = Y0 / X0
				BX = M * X1
				B = Y1 - BX
			YX = M * PI3_OUT
			SP_SAT = YX + B
		
		// CONTROL DE DEMANDA DE TEMPERATURA (SUMINISTRO)
			PI4_VAR = SAT
			PI4_SP = SP_SAT
			CALL PI4
			CN_CCV = PI4_OUT_D
			CN_HCV = PI4_OUT_I
			
		
	// BLOQUE 6: ARRANQUE DE SISTEMA
	
		// SELECTOR DE MODO DE OPERACION
			IF MODO == ON THEN SS_SYS = ACT_HOR ELSE SS_SYS = ACT_MAN
			
	
		// PROCESO DE ARRANQUE Y PARO DE SISTEMA
			IF SS_SYS == OFF THEN JUMP PARO 
			
		
			// ARRANQUE
		
				// ACTIVACIÓN: CONTROL DE VENTILACION SUMINISTRO
					IF T_SYS_ON > DL_VSUM_ON THEN SS_VSUM = ON
			
				// ACTIVACION: CONTROL DE TEMPERATURA 
					IF T_SYS_ON > DL_TM_ON AND ST_VSUM == ON THEN SS_TM = ON 
					
				// ACTIVACION: CONTROL DE FILTRACION 
					IF T_SYS_ON > DL_FT_ON AND ST_VSUM == ON THEN SS_FT = ON
					
				// ESTADO GENERAL DE SISTEMA
					IF ST_VSUM == ON AND ST_TM == ON AND ST_FT == ON THEN ST_SYS = ON ELSE ST_SYS = OFF
			
				JUMP MODULOS
				
		
			// PARO
			[PARO]
		
				// PARO: CONTROL DE FILTRACION 
					IF T_SYS_OFF > DL_FT_OFF THEN SS_FT = OFF
			
				// PARO: CONTROL DE TEMPERATURA 
					IF T_SYS_OFF > DL_TM_OFF THEN SS_TM = OFF 
					
				// PARO: CONTROL DE VENTILACION SUMINISTRO
					IF T_SYS_OFF > DL_VSUM_OFF AND ST_TM == OFF THEN SS_VSUM = OFF
					
				// ESTADO GENERAL DE SISTEMA
					IF ST_VSUM == OFF AND ST_TM == OFF AND ST_FT == OFF THEN ST_SYS = OFF ELSE ST_SYS = ON
					
	
	// BLOQUE 7: MODULOS DE CONTROL
	[MODULOS]
		
		// MODULO: CONTROL DE VENTILACION DE SUMINISTRO 
			CALL VENTILACION_SUMINISTRO 
		
		// MODULO: CONTROL DE TEMPERATURA 
			CALL TEMPERATURA 
		
		// MODULO: CONTROL DE FILTRACCION
			CALL FILTRACION 

	[FINAL]
END