# VARIABLES DE CONTROL

## ENTRADAS

> `BI_1`    **ST_SF** 	*ACTIVO* / *INACTIVO*	Estado de operación de Ventilador de suministro

> **BI_2**	`IN_FT1`  	[SUCIOS/LIMPIOS]	Estado de prefiltros

< **BI_3**	`IN_FT2` 	[SUCIOS/LIMPIOS]	Estado de filtros de bolsa

< **BI_4**	`ST_INC`  	[ALARMA/NORMAL]		Estado de alarma de detección de incendios

**AI_5**  	`IN_SAT`  	[°C]				Temperatura de suministro de aire
**AI_6**  	`IN_RAT`	[°C]				Temperatura de retorno de aire
**AI_7** 	`IN_SPT` 	[°C]				Temperatura de cuarto
**AI_8** 	`ST_HCV`    [%]					Estado de apertura de válvula de agua caliente
**AI_9** 	`ST_CCV` 	[%]					Estado de apertura de válvula de agua helada
**BI_12**	`MANUAL`	[ON/OFF]			Arranque manual de sistema desde tablero

## SALIDAS

**BO_1**	`SS_SF`  	[ARRANQUE/PARO]		Arranque de ventilador de suministro de aire
**AO_1**  	`CN_SF`		[%]					Control de velocidad de ventilador de suministro de aire
**AO_2**  	`CN_HCV`  	[%]					Control de apertura de válvula de agua caliente
**AO_3**  	`CN_CCV`  	[%]					Control de apertura de válvula de agua helada