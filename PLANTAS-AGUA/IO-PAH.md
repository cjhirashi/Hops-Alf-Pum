# SISTEMA DE CONTROL - PAH - Planta de Agua Helada

Sistema de control de Planta de agua helada, este sistema opera en conjunto con sistema de control de planta de agua de condensados

Tarjeta de control **BACnet MS/TP**- `NX7-ECO-NG` - [RIKMED](www.rikmed.com)

### ENTRADAS

> `AI_1`		**IN_SWT**		[ *°C* ]				    Temperatura de suministro de agua
>
> `AI_2`		**IN_RWT**		[ *°C* ]				    Temperatura de retorno de agua
>
> `AI_3`		**IN_DP**		[ *PSI* ]				    Presión Diferencial de circuito de agua 
>
> `BI_4`		**ST_BM1**		[ *ACTIVO* / *INACTIVO* ]	Estado de operación de Bomba 1
>
> `BI_5`		**ST_BM2**		[ *ACTIVO* / *INACTIVO* ]	Estado de operación de Bomba 2
>
> `BI_6`		**ST_BM3**		[ *ACTIVO* / *INACTIVO* ]	Estado de operación de Bomba 3
>
> `BI_7`		**IN_EQ1**		[ *ACTIVO* / *INACTIVO* ]	Estado de operación de Chiller 1
>
> `BI_8`		**IN_EQ2**		[ *ACTIVO* / *INACTIVO* ]	Estado de operación de Chiller 2
>
> `BI_9`		**ST_VL1**		[ *ABIERTA* / *CERRADA* ]	Estado de apertura de válvula de Chiller 1
>
> `BI_10`		**ST_VL2**		[ *ABIERTA* / *CERRADA* ]	Estado de apertura de válvula de Chiller 1

### SALIDAS

> `BO_1`		**SS_BM1**		[ *ARRANQUE* / *PARO* ]		Arranque de Bomba 1
>
> `BO_2`		**SS_BM2**		[ *ARRANQUE* / *PARO* ]		Arranque de Bomba 2
>
> `BO_3`		**SS_BM3**		[ *ARRANQUE* / *PARO* ]		Arranque de Bomba 3
>
> `BO_4`		**SS_EQ1**		[ *ARRANQUE* / *PARO* ]		Arranque de Chiller 1
>
> `BO_5`		**SS_EQ2**		[ *ARRANQUE* / *PARO* ]		Arranque de Chiller 2
>
> `BO_6`		**OUT_VL1**		[ *ABRIR* / *CERRAR* ]		Apertura de válvula de chiller 1
>
> `BO_7`		**OUT_VL2**		[ *ABRIR* / *CERRAR* ]		Apertura de válvula de chiller 1
>
> `BO_8`		**SS_PAK**		[ *ARRANQUE* / *PARO* ]		Arranque de Planta de Agua de Condensados