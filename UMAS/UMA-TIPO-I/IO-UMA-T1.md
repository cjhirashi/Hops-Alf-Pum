# SISTEMA DE CONTROL - UMA TI - Unidad Manejadora de Aire tipo 1

Sistema de control de Unidad Manejadora de aire de volumen constante, control de válvula proporcional de agua helada

Tarjeta de control **BACnet MS/TP** - `NX7-ECO-Lite` - [RIKMED](www.rikmed.com)

- **UMA-01** `DI-21001` `MAC-4`

- **UMA-03** `DI-22003` `MAC-6`

- **UMA-09** `DI-22009` `MAC-12`

- **UMA-10** `DI-22010` `MAC-13`

- **UMA-12** `DI-21012` `MAC-15`

- **UMA-13** `DI-21013` `MAC-16`

- **UMA-14** `DI-21014` `MAC-17`

- **UMA-15** `DI-21015` `MAC-18`

- **UMA-16** `DI-21016` `MAC-19`

- **UMA-20** `DI-13020` `MAC-23`

- **UMA-22** `DI-14022` `MAC-24`

- **UMA-23** `DI-15023` `MAC-25`

- **UMA-24** `DI-15024` `MAC-26`

- **UMA-25** `DI-14025` `MAC-27`

## PUNTOS DE CONTROL

### ENTRADAS

> **BI_1**   `ST_SF` 	    [ *ACTIVO* / *INACTIVO* ]	Estado de operación de Ventilador de suministro
>
> **BI_2**	`IN_FT1`        [ *SUCIOS* / *LIMPIOS* ]	Estado de prefiltros
>
> **BI_3**	`IN_FT2`        [ *SUCIOS* / *LIMPIOS* ]	Estado de filtros de bolsa
>
> **BI_4**	`ST_INC`        [ *ALARMA* / *NORMAL* ]		Estado de alarma de detección de incendios
>
> **AI_5** 	`IN_SAT`        [ *°C* ]				    Temperatura de suministro de aire
>
> **AI_6**  `IN_RAT`	    [ *°C* ]				    Temperatura de retorno de aire
>
> **AI_7** 	`IN_SPT` 	    [ *°C* ]				    Temperatura de cuarto
>
> **AI_8** 	`ST_HCV`        [ *%* ]					    Estado de apertura de válvula de agua caliente
>
> **AI_9** 	`ST_CCV` 	    [ *%* ]					    Estado de apertura de válvula de agua helada
>
> **BI_12**	`MANUAL`	    [ *ON* / *OFF* ]			Arranque manual de sistema desde tablero

### SALIDAS

> **BO_1**	`SS_SF`  	    [ *ARRANQUE* / *PARO* ]		Arranque de ventilador de suministro de aire
>
> **AO_1**  `CN_SF`	        [ *%* ]					    Control de velocidad de ventilador de suministro de aire
>
> **AO_2**  `CN_HCV`        [ *%* ]					    Control de apertura de válvula de agua caliente
>
> **AO_3**  `CN_CCV`  	    [ *%* ]					    Control de apertura de válvula de agua helada

### VARIABLES: Sensores y setpoints

> **RES_FLT_1**	    `RAT`           -reading-   [ *°C* ]                    Temperatura de retorno de aire
>
> **RES_FLT_2**	    `SPT`			-reading-   [ *°C* ]	                Temperatura de área 1
>
> **ADF_1**		    `SP_SPT`		-writing-   [ *°C* ]	                Setpoint de temperatura de área
>
> **ADF_2**		    `SP_SPT_MAX`	-reading-   [ *°C* ]	                Límite máximo de setpoint de temperatura de área 
>
> **ADF_3**		    `SP_SPT_MIN`	-reading-   [ *°C* ]	                Límite mínimo de setpoint de temperatura de área
>
> **RES_FLT_4**	    `SAT`		    -reading-	[ *°C* ]	                Temperatura de suministro de aire  
>
> **RES_FLT_5**	    `SP_SAT`	    -reading-	[ *°C* ]	                Setpoint de temperatura de suministro de aire  
>
> **RES_BIT_1**	    `ST_FT1`	    -reading-	[ *SUCIOS* / *LIMPIOS* ]    Estado de filtros 1 (gráficos) 
>
> **RES_BIT_2**	    `ST_FT2`	    -reading-	[ *SUCIOS* / *LIMPIOS* ]    Estado de filtros 2 (gráficos) 
>
> **RES_FLT_10**	`Y0`			-reading-
>
> **ADF_10**		`Y1`		    -reading-	[ *°C* ]	                Límite máximo de temperatura de salida  
>
> **ADF_11**		`Y2`		    -reading-	[ *°C* ]	                Límite mínimo de temperatura de salida  
>
> **RES_FLT_11**	`X0`			-reading-
>
> **ADF_12**		`X1`		    -reading-	[ *°C* ]	                Límite máximo de temperatura de entrada  
>
> **ADF_13**		`X2`		    -reading-	[ *°C* ]	                Límite mínimo de temperatura de entrada  
>
> **RES_FLT_12**	`M`				-reading-
>
> **RES_FLT_13**	`BX`			-reading-
>
> **RES_FLT_14**	`B`				-reading-
>
> **RES_FLT_15**	`YX`		    -reading-
		
### VARIABLES: Timers
	
> **ADF_14**		`LM_TM`			-reading-	[ *SEG* ]		LIMITE DE CONTEO TIMERS 
>
> **RES_FLT_16**	`T_SYS_ON`		-reading-	[ *SEG* ]		TIMER ON, ACTIVACION SISTEMA 
>
> **RES_FLT_17**	`T_SYS_OFF`		-reading-	[ *SEG* ]		TIMER OFF, ACTIVACION SISTEMA 
>
> **RES_FLT_18**	`T_VSUM_ON`		-reading-	[ *SEG* ]		TIMER ON, ACTIVACION CONTROL VENTILACION SUMINISTRO 
>
> **RES_FLT_19**	`T_VSUM_OFF`	-reading-	[ *SEG* ]		TIMER OFF, ACTIVACION CONTROL VENTILACION SUMINISTRO 
>
> **RES_FLT_22**	`T_TM_ON` 		-reading-	[ *SEG* ]		TIMER ON, ACTIVACION CONTROL TEMPERATURA 
>
> **RES_FLT_23**	`T_TM_OFF`		-reading-	[ *SEG* ]		TIMER OFF, ACTIVACION CONTROL TEMPERATURA 
>
> **RES_FLT_24**	`T_FT_ON`		-reading-	[ *SEG* ]		TIMER ON, ACTIVACION CONTROL FILTROS 
>
> **RES_FLT_25**	`T_FT_OFF`		-reading-	[ *SEG* ]		TIMER OFF, ACTIVACION CONTROL FILTROS 
>
> **RES_FLT_26**	`T_SF_ON`		-reading-	[ *SEG* ]		TIMER ON, ESTADO VENTILADOR SUMINISTRO 
>
> **RES_FLT_27**	`T_SF_OFF`		-reading-	[ *SEG* ]		TIMER OFF, ESTADO VENTILADOR SUMINISTRO 
>
> **RES_FLT_30**	`T_CM_ON`		-reading-	[ *SEG* ]		TIMER ON, ESTADO DE COMPRESOR 
>
> **RES_FLT_31**	`T_CM_OFF`		-reading-	[ *SEG* ]		TIMER OFF, ESTADO DE COMPRESOR 
>
> **RES_FLT_32**	`T_TEST_ON`		-reading-	[ *SEG* ]		TIMER ON, TEST
	
### VARIABLES: Principal
		
> **RES_BIT_201**	`P_MANUAL`      -reading-
>
> **RES_BIT_3**	    `MODO`			-writing-	[ *AUTO* / *MANUAL* ]		MODO DE ARRANQUE DE SISTEMA 
>
> **RES_BIT_4**	    `ACT_HOR`		-reading-	[ *ACTIVO* / *INACTIVO* ]	ACTIVACION HORARIO DE SISTEMA
>
> **RES_BIT_5**	    `ACT_MAN`		-writing-	[ *ACTIVO* / *INACTIVO* ]	ACTIVACION MANUAL DE SISTEMA
>
> **RES_BIT_6**	    `SS_SYS`		-reading-	[ *ACTIVAR* / *PARO* ]		ACTIVACION GENERAL DEL SISTEMA
>
> **RES_BIT_7**	    `ST_SYS`		-reading-	[ *ACTIVO* / *INACTIVO* ]	ESTADO DE ACTIVACION GENERAL DEL SISTEMA 
>
> **RES_BIT_8**	    `AL_SYS`		-reading-	[ *ALARMA* / *NORMAL* ]		ALARMA GENERAL DEL SISTEMA
>
> **RES_BIT_9**	    `SS_VSUM`		-reading-	[ *ACTIVAR* / *PARO* ]		ACTIVACION DE MODULO DE CONTROL DE VENTILACION DE SUMINISTRO
> 
> **RES_BIT_10**	`ST_VSUM`		-reading-	[ *ACTIVO* / *INACTIVO* ]	ESTADO DE MODULO DE CONTROL DE VENTILACION DE SUMINISTRO
> 
> **RES_BIT_11**	`AL_VSUM`		-reading-	[ *ALARMA* / *NORMAL* ]		ALARMA DE MODULO DE CONTROL DE VENTILACION DE SUMINISTRO
> 
> **ADF_15**		`DL_VSUM_ON`	-reading-	[ *SEG* ]				RETARDO DE ACTIVACION DE MODULO DE CONTRO DE VENTILACION DE SUMINISTRO 
>
> **ADF_16**		`DL_VSUM_OFF`	-reading-	[ *SEG* ]				RETARDO DE PARO DE MODULO DE CONTROL DE VENTILACION DE SUMINISTRO 
>
> **RES_BIT_15**	`SS_TM`			-reading-	[ *ACTIVAR* / *PARO* ]		ACTIVACION DE MODULO DE CONTROL DE TEMPERATURA 
>
> **RES_BIT_16**	`ST_TM`			-reading-	[ *ACTIVO* / *INACTIVO* ]	ESTADO DE MODULO DE CONTROL DE TEMPERATURA 
>
> **RES_BIT_17**	`AL_TM`			-reading-	[ *ALARMA* / *NORMAL* ]		ALARMA DE MODULO DE CONTROL DE TEMPERATURA 
>
> **ADF_19**		`DL_TM_ON`		-reading-	[ *SEG* ]				RETARDO DE ACTIVACION DE MODULO DE CONTRO DE TEMPERATURA
> 
> **ADF_20**		`DL_TM_OFF`		-reading-	[ *SEG* ]				RETARDO DE PARO DE MODULO DE CONTROL DE TEMPERATURA
>
> **RES_BIT_18**	`SS_FT`			-reading-	[ *ACTIVAR* / *PARO* ]		ACTIVACION DE MODULO DE CONTROL DE FILTRACION 
>
> **RES_BIT_19**	`ST_FT`			-reading-	[ *ACTIVO* / *INACTIVO* ]	ESTADO DE MODULO DE CONTROL DE FILTRACION 
>
> **RES_BIT_20**	`AL_FT`			-reading-	[ *ALARMA* / *NORMAL* ]		ALARMA DE MODULO DE CONTROL DE FILTRACION 
>
> **ADF_21**		`DL_FT_ON`		-reading-	[ *SEG* ]				RETARDO DE ACTIVACION DE MODULO DE CONTRO DE FILTRACION
>
> **ADF_22**		`DL_FT_OFF`		-reading-	[ *SEG* ]				RETARDO DE PARO DE MODULO DE CONTROL DE FILTRACION 
>
> **RES_BIT_40**	`ALM_PARO`		-reading-	[ *ALARMA* / *NORMAL* ]		ALARMA CRITICA PARA PARO DE SISTEMA 
>
> **RES_BIT_41**	`RESET_ALM`		-reading-	[ *RESET* / *NORMAL* ]		RESET DE ALARMA CRITICA 
	
	//.......................................................................................
	// VARIABLES: [ VENTILACION SUMINISTRO ]

	DEF		RES_BIT_42	ALM_SF			// [READ]	[ALARMA/NORMAL]		ALARMA DE ARRANQUE VENTILADOR SUMINISTRO 
	DEF		ADF_70		VEL_MAX			// [READ]	[%]					VELOCIDAD DE VENTILADOR MAXIMA
	DEF		ADF_71		VEL_MIN			// [READ]	[%]					VELOCIDAD DE VENTILADOR MINIMA
	
	//.......................................................................................
	// VARIABLES: [ TEMPERATURA ]
	
	DEF		RES_FLT_34	TEMP			// [READ]	[°C]				TEMPERATURA EN OPERACION
	DEF		RES_BIT_44	SL_TEMP			// [WRITE]	[CUARTO/RETORNO]	SELECTOR DE TEMPERATURA EN OPERACION
	
	DEF		ADF_23		LM_AL_TM		// [READ]	[°C]				LIMITE MAX MIN PARA ALARMA POR TEMPERATURA FUERA DE RANGO
	DEF		RES_BIT_45	AL_TEMP_H		// [READ]	[ALARMA/NORMAL]		ALARMA POR TEMPERATURA DE AREA ALTA
	DEF		RES_BIT_46	AL_TEMP_L		// [READ]	[ALARMA/NORMAL]		ALARMA POR TEMPERATURA DE AREA BAJA
	DEF		RES_BIT_47	AL_SAT_H		// [READ]	[ALARMA/NORMAL]		ALARMA POR TEMPERATURA DE SUMINISTRO ALTA
	DEF		RES_BIT_48	AL_SAT_L		// [READ]	[ALARMA/NORMAL]		ALARMA POR TEMPERATURA DE SUMINISTRO BAJA
	
	//.......................................................................................
	// VARIABLES DE CONTROLES DE DEMANDA
	
		// VARIABLES: [ PID1 ] VENTILADOR SUMINISTRO
		DEF		RES_FLT_36	PI1_VAR		// [Read]						VARIABLE DE CONTROL
		DEF		RES_FLT_37	PI1_SP		// [Read]						SETPOINT DE CONTROL
		DEF		RES_BIT_49	PI1_SS		// [Read]						ACTIVACION DE CONTROL
			// VARIABLES: PI 1
			DEF		ADF_26		PI1_DIR		// [Read]	[1/-1]			DIRECCION DE CONTROL
			DEF		ADF_27		PI1_P		// [Read]	[#.#]			BANDA PROPORCIONAL
			DEF		ADF_28		PI1_I		// [Read]	[#.#]			BANDA INTEGRAL
			DEF		ADF_29		PI1_MAX		// [Read]	[%]				LIMITE MAXIMO
			DEF		ADF_30		PI1_MIN		// [Read]	[%]				LIMITE MINIMO
			DEF		RES_FLT_38	PI1_ERR		// [Read]					ERROR
			DEF		RES_FLT_39	PI1_RP		// [Read]	[%]				RESULTANTE PROPORCIONAL
			DEF		RES_FLT_40	PI1_RI		// [Read]	[%]				RESULTANTE INTEGRAL
			DEF		RES_FLT_41	PI1_RIS		// [Read]	[%]				RESULTANTE INTEGRAL ACUMULATIVO
			DEF		RES_FLT_42	PI1_OUT		// [Read]	[%]				DEMANDA DE CONTROL
	
		// VARIABLES: [ PID3 ] TEMPERATURA DE AREA
		DEF		RES_FLT_50	PI3_VAR		// [Read]						VARIABLE DE CONTROL
		DEF		RES_FLT_51	PI3_SP		// [Read]						SETPOINT DE CONTROL
		DEF		RES_BIT_51	PI3_SS		// [Read]						ACTIVACION DE CONTROL
			// VARIABLES: PI 3
			DEF		ADF_36		PI3_DIR		// [Read]	[1/-1]			DIRECCION DE CONTROL
			DEF		ADF_37		PI3_P		// [Read]	[#.#]			BANDA PROPORCIONAL
			DEF		ADF_38		PI3_I		// [Read]	[#.#]			BANDA INTEGRAL
			DEF		ADF_39		PI3_MAX		// [Read]	[%]				LIMITE MAXIMO
			DEF		ADF_40		PI3_MIN		// [Read]	[%]				LIMITE MINIMO
			DEF		RES_FLT_52	PI3_ERR		// [Read]					ERROR
			DEF		RES_FLT_53	PI3_RP		// [Read]	[%]				RESULTANTE PROPORCIONAL
			DEF		RES_FLT_54	PI3_RI		// [Read]	[%]				RESULTANTE INTEGRAL
			DEF		RES_FLT_55	PI3_RIS		// [Read]	[%]				RESULTANTE INTEGRAL ACUMULATIVO
			DEF		RES_FLT_56	PI3_OUT		// [Read]	[%]				DEMANDA DE CONTROL
			
		// VARIABLES: [ PID4 ] TEMPERATURA DE SUMINISTRO
		DEF		RES_FLT_57	PI4_VAR		// [Read]						VARIABLE DE CONTROL
		DEF		RES_FLT_58	PI4_SP		// [Read]						SETPOINT DE CONTROL
		DEF		RES_BIT_52	PI4_SS		// [Read]						ACTIVACION DE CONTROL
			// VARIABLES: PI 4
			DEF		ADF_41		PI4_DIR		// [Read]	[1/-1]			DIRECCION DE CONTROL
			DEF		ADF_42		PI4_P		// [Read]	[#.#]			BANDA PROPORCIONAL
			DEF		ADF_43		PI4_I		// [Read]	[#.#]			BANDA INTEGRAL
			DEF		ADF_44		PI4_MAX		// [Read]	[%]				LIMITE MAXIMO
			DEF		ADF_45		PI4_MIN		// [Read]	[%]				LIMITE MINIMO
			DEF		RES_FLT_59	PI4_ERR		// [Read]					ERROR
			DEF		RES_FLT_60	PI4_RP		// [Read]	[%]				RESULTANTE PROPORCIONAL
			DEF		RES_FLT_61	PI4_RI		// [Read]	[%]				RESULTANTE INTEGRAL
			DEF		RES_FLT_62	PI4_RIS		// [Read]	[%]				RESULTANTE INTEGRAL ACUMULATIVO
			DEF		RES_FLT_63	PI4_OUT		// [Read]	[%]				DEMANDA DE CONTROL
			DEF		RES_FLT_64	PI4_OUT_D	// [Read]	[%]				DEMANDA DE CONTROL (DOBLE) DIRECTA
			DEF		RES_FLT_65	PI4_OUT_I	// [Read]	[%]				DEMANDA DE CONTROL (DOBLE) INVERSA
			
	//.......................................................................................
	// VARIABLES: [ VARIABLES TEST ]
	
	DEF		RES_BIT_54	SS_TEST			// [WRITE]	[ACTIVAR/PARO]		ACTIVACION DE PRUEBA GENERAL DE SISTEMA 
	DEF		RES_BIT_55	TEST			// [READ]	[ACTIVO/INACTIVO]	ACTIVACION DE PRUEBA
	DEF		RES_FLT_73	TEST_STEP		// [READ]						RESPUESTA TEST
	DEF		ADF_51		T_TEST_1		// [READ]	[SEG]				TIEMPO DE PRUEBA 1
	DEF		ADF_52		T_TEST_2		// [READ]	[SEG]				TIEMPO DE PRUEBA 2
	DEF		ADF_53		T_TEST_3		// [READ]	[SEG]				TIEMPO DE PRUEBA 3
	DEF		ADF_54		T_TEST_4		// [READ]	[SEG]				TIEMPO DE PRUEBA 4
	DEF		ADF_55		T_TEST_5		// [READ]	[SEG]				TIEMPO DE PRUEBA 5
	DEF		ADF_56		T_TEST_6		// [READ]	[SEG]				TIEMPO DE PRUEBA 6
	DEF		ADF_57		T_TEST_7		// [READ]	[SEG]				TIEMPO DE PRUEBA 7
	DEF		ADF_58		T_TEST_8		// [READ]	[SEG]				TIEMPO DE PRUEBA 8
	DEF		ADF_59		T_TEST_9		// [READ]	[SEG]				TIEMPO DE PRUEBA 9
	DEF		ADF_60		T_TEST_10		// [READ]	[SEG]				TIEMPO DE PRUEBA 10