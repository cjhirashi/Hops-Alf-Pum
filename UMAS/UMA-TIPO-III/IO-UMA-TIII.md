# SISTEMA DE CONTROL - UMA TI - Unidad Manejadora de Aire tipo 3

Sistema de control de Unidad Manejadora de aire de volumen variable, control de extracción de volumen variable, control de válvula proporcional de agua helada, control de expansión directa

Tarjeta de control **BACnet MS/TP** - `NX7-ECO-NG` - [RIKMED](www.rikmed.com 'Sistemas de control DDC')

- **UMA-02** `DI-11002` `MAC-5`

- **UMA-04** `DI-11004` `MAC-7`

- **UMA-05** `DI-11005` `MAC-8`

- **UMA-08** `DI-11008` `MAC-11`

### ENTRADAS

> `BI_1`		**ST_CM**			[ *ACTIVO* / *INACTIVO* ]	ESTADO DE UNIDAD CONDENSADORA DE AIRE
> `BI_2`		**ST_SF**			[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE VENTILADOR DE SUMINISTRO
> `BI_3`		**ST_EF**			[ *ACTIVO* / *INACTIVO* ]	ESTADO DE OPERACION DE VENTILADOR DE EXTRACCION
> `AI_4`		**IN_SAT**			[ *°C* ]				    TEMPERATURA DE SUMINISTRO DE AIRE (ENTRADA)
> `AI_5`		**IN_RAT**			[ *°C* ]				    TEMPREATURA DE RETORNO DE AIRE (ENTRADA)
> `AI_6`		**IN_SPT1**			[ *°C* ]				    TEMPERATURA DE AREA 1
> `AI_7`		**IN_SPT2**			[ *°C* ]				    TEMPERATURA DE AREA 2
> `BI_8`		**IN_FT1**			[ *SUCIOS* / *LIMPIOS* ]	ESTADO DE PREFILTROS
> `BI_9`		**IN_FT2**			[ *SUCIOS* / *LIMPIOS* ]	ESTADO DE FILTROS DE BOLSA
> `AI_10`		**IN_FT3**			[ *"WC* ]				    ESTADO DE FILTROS HEPA (ENTRADA)
> `BI_11`		**ST_INC**			[ *ALARMA* / *NORMAL* ]		ESTADO DE ALARMA DE INCENDIOS
> `AI_12`		**IN_SAP**			[ *"WC* ]				    PRESION DE SUMINISTRO DE AIRE (ENTRADA)
> `AI_13`		**IN_EAP**			[ *"WC* ]				    PRESION DE EXTRACCION DE AIRE (ENTRADA)
> `AI_14`		**IN_SPP1**		    [ *"WC* ]				    PRESION DE AREA 1
> `AI_15`		**IN_SPP2**		    [ *"WC* ]				    PRESION DE AREA 2
> `AI_16`		**ST_HCV**			[ *%* ]					    ESTADO DE APERTURA DE VALVULA DE AGUA CALIENTE
> `AI_17`		**ST_CCV**			[ *%* ]					    ESTADO DE APERTURA DE VALVULA DE AGUA HELADA
> `AI_18`		**ST_DMS1**		    [ *%* ]					    ESTADO DE APERTURA DE COMPUERTA DE SUMINISTRO 1
> `AI_19`		**ST_DMS2**		    [ *%* ]					    ESTADO DE APERTURA DE COMPUERTA DE SUMINISTRO 2
> `AI_20`		**ST_DME1**		    [ *%* ]					    ESTADO DE APERTURA DE COMPUERTA DE EXTRACCION 1
> `AI_21`		**ST_DME2**		    [ *%* ]					    ESTADO DE APERTURA DE COMPUERTA DE EXTRACCION 2
> `BI_22`		**MANUAL**			[ *ON* / *OFF* ]			Arranque manual de sistema desde tablero
	
### SALIDAS

> `BO_1`		**SS_CM**			[ *ARRANQUE* / *PARO* ]		ARRANQUE DE UNIDAD CONDENSADORA DE AIRE 1
> `BO_2`		**SS_SF**			[ *ARRANQUE* / *PARO* ]		ARRANQUE DE VENTILADOR DE SUMINISTRO DE AIRE
> `BO_3`		**SS_EF**			[ *ARRANQUE* / *PARO* ]		ARRANQUE DE VENTILADOR DE EXTRACCION DE AIRE
> `AO_1`		**CN_SF**			[ *%* ]					    CONTROL DE VELOCIDAD DE VENTILADOR DE SUMINISTRO DE AIRE
> `AO_2`		**CN_EF**			[ *%* ]					    CONTROL DE VELOCIDAD DE VENTILADOR DE EXTRACCION DE AIRE
> `AO_3`		**CN_HCV**			[ *%* ]					    CONTROL DE APERTURA DE VALVULA DE AGUA CALIENTE
> `AO_4`		**CN_CCV**			[ *%* ]					    CONTROL DE APERTURA DE VALVULA DE AGUA HELADA
> `AO_5`		**CN_DMS1**			[ *%* ]					    CONTROL DE APERTURA DE COMPUERTA DE SUMINISTRO 1
> `AO_6`		**CN_DMS2**			[ *%* ]					    CONTROL DE APERTURA DE COMPUERTA DE SUMINISTRO 2
> `AO_7`		**CN_DME1**			[ *%* ]					    CONTROL DE APERTURA DE COMPUERTA DE EXTRACCION 1
> `AO_8`		**CN_DME2**			[ *%* ]					    CONTROL DE APERTURA DE COMPUERTA DE EXTRACCION 2