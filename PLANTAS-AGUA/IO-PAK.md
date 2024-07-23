# SISTEMA DE CONTROL - PAK - Planta de agua de condensados

Sistema de control de Planta de agua de condensados, este sistema opera en conjunto con sistema de control de planta de agua helada

Tarjeta de control **BACnet MS/TP** - `NX7-ECO-NG` - [RIKMED](www.rikmed.com)

### ENTRADAS

> `AI_1`		**IN_OAH**		[ *%RH* ]				    HUMEDAD DE AIRE EXTERIOR
>
> `AI_2`		**IN_OAT**		[ *°C* ]				    TEMPERATURA DE AIRE EXTERIOR 
>
> `AI_3`		**IN_SWT**		[ *°C* ]				    TEMPERATURA DE SUMINISTRO DE AGUA 
>
> `AI_4`		**IN_RWT**		[ *°C* ]				    TEMPERATURA DE RETORNO DE AGUA 
>
> `BI_5`		**ST_BM1**		[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE BOMBA 1
>
> `BI_6`		**ST_BM2**		[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE BOMBA 2
>
> `BI_7`		**ST_BM3**		[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE BOMBA 3
>
> `BI_8`		**IN_EQ1**		[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE TORRE 1
>
> `BI_9`		**IN_EQ2**		[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE TORRE 2
>
> `BI_10`		**IN_ACT**		[ *ARRANQUE* / *PARO* ]		ARRANQUE DESDE SISTEMA DE PAH
	
### SALIDAS

> `BO_1`		**SS_BM1**		[ *ARRANQUE* / *PARO* ]		ARRANQUE DE BOMBA 1 
>
> `BO_2`		**SS_BM2**		[ *ARRANQUE* / *PARO* ]		ARRANQUE DE BOMBA 2 
>
> `BO_3`		**SS_BM3**		[ *ARRANQUE* / *PARO* ]		ARRANQUE DE BOMBA 3 
>
> `BO_4`		**SS_EQ1**		[ *ARRANQUE* / *PARO* ]		ARRANQUE DE TORRE 1 
>
> `BO_5`		**SS_EQ2**		[ *ARRANQUE* / *PARO* ]		ARRANQUE DE TORRE 2 
>
> `AO_1`		**CN_EQ1**		[ *%* ]					    CONTROL DE VELOCIDAD DE TORRE 1 
>
> `AO_2`		**CN_EQ2**		[ *%* ]					    CONTROL DE VELOCIDAD DE TORRE 2 