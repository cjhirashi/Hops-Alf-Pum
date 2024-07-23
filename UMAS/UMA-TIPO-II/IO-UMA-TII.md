# SISTEMA DE CONTROL - UMA TI - Unidad Manejadora de Aire tipo 1

Sistema de control de Unidad Manejadora de aire de volumen constante, control de válvula proporcional de agua helada

Tarjeta de control **BACnet MS/TP** - `NX5-ECO-HVAC` - [RIKMED](www.rikmed.com)

- **UMA-06** `DI-11006` `MAC-9`

- **UMA-07** `DI-11007` `MAC-10`

- **UMA-11** `DI-11011` `MAC-14`

- **UMA-17** `DI-11017` `MAC-20`

- **UMA-18** `DI-11018` `MAC-21`

- **UMA-19** `DI-11019` `MAC-12`

### ENTRADAS

> `AI_1`  		**IN_SAT**  	[ *°C* ]				    Temperatura de suministro de aire
> `AI_2`  		**IN_RAT**		[ *°C* ]				    Temperatura de retorno de aire
> `AI_3` 		**IN_SPT** 		[ *°C* ]				    Temperatura de cuarto
> `AI_4` 		**ST_HCV**     	[ *%* ]					    Estado de apertura de válvula de agua caliente
> `AI_5` 		**ST_CCV** 		[ *%* ]					    Estado de apertura de válvula de agua helada
> `BI_9` 		**ST_CM** 		[ *ACTIVO* / *INACTIVO* ]	Estado de activación de expansión directa enfriamiento
> `BI_10`		**ST_SF** 		[ *ACTIVO* / *INACTIVO* ]	Estado de operación de Ventilador de suministro
> `BI_11`		**IN_FT1**  	[ *SUCIOS* / *LIMPIOS* ]	Estado de prefiltros
> `BI_12`		**IN_FT2** 		[ *SUCIOS* / *LIMPIOS* ]	Estado de filtros de bolsa
> `BI_13`		**ST_INC**  	[ *ALARMA* / *NORMAL* ]		Estado de alarma de detección de incendios
> `BI_16`		**MANUAL**		[ *ON* / *OFF* ]			Arranque manual de sistema desde tablero
	
### SALIDAS

> `BO_1`		**SS_CM**  		[ *ARRANQUE* / *PARO* ]		Activación de expansión directa enfriamiento
> `BO_2`		**SS_SF**  		[ *ARRANQUE* / *PARO]		Arranque de ventilador de suministro de aire
> `AO_1`  		**CN_SF**		[ *%* ]					    Control de velocidad de ventilador de suministro de aire
> `AO_2`  		**CN_HCV**  	[ *%* ]					    Control de apertura de válvula de agua caliente
> `AO_3`  		**CN_CCV**  	[ *%* ]					    Control de apertura de válvula de agua helada