# sesion-10a  
Martes 19 de Mayo

- sacar foto, que hay detras del clickeo dl botón
-> metaprograma   

caja negra... revisar

--------

## charla ##

-----------

## Revisión circuito

* al subir → se apura
* al bajar → se ralentiza
* el voltaje cambia la frecuencia
* convertir voltaje en frecuencia

Se estuvo revisando cómo la variación de voltaje afecta directamente el comportamiento temporal del circuito. La idea principal era entender que la frecuencia de oscilación puede controlarse mediante voltaje, algo fundamental para síntesis y modulación.

## Potenciómetro

* ajusta voltaje
* controla oscilación
* puede enviar voltaje al VCO

El potenciómetro funciona como un control manual del voltaje. Al modificar ese voltaje, cambia también la frecuencia del oscilador. El voltaje ajustado puede usarse como señal de control para un VCO.

## VCO

* oscilador controlado por voltaje
* más voltaje = más frecuencia
* menos voltaje = menos frecuencia

Relación principal:

f \propto V

La frecuencia depende del voltaje de entrada. El VCO transforma variaciones eléctricas en cambios de tono o velocidad de oscilación.

## CD4040

* contador binario
* divisor de frecuencia
* útil para osciladores y filtros de sonido

El CD4040 divide la frecuencia original en subdivisiones más lentas. Cada salida representa una división distinta de la señal inicial, lo que permite generar clocks, ritmos u oscilaciones derivadas. Apareció una comparación con “un chip convencional” que habría que revisar después porque los apuntes quedaron incompletos.

## Multiplexor (MUX)

* selector de señales
* varias entradas → una salida

El multiplexor funciona como un conmutador digital. Permite escoger qué señal pasa hacia la salida, por ejemplo distintas frecuencias provenientes de un contador o varias señales de oscilación. Relación con routing y selección de señales dentro de síntesis modular.

## Chips importantes para mi equipo de filtro de sonido

* revisar CD4040
* contador binario
* filtro-T

### Filtro-T

Tipo de filtro electrónico usado para moldear o cancelar ciertas frecuencias. Importante revisarlo después junto a diagramas y configuraciones posibles para audio/filtros 
