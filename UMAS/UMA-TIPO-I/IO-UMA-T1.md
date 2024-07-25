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

