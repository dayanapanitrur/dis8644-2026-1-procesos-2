# sesion-11a
## Propuestas Proyectos 
Empezamos  a trabajar sin la protoboard, ya que aún nos faltaban algunos chips para realizar las pruebas físicas del circuito. Debido a que en esta clase debíamos tener listo el esquemático para continuar con el desarrollo del proyecto y que estuviéramos al tanto de que está haciendo el otro.

## Propuesta 01: chip 40106
Nos enfocamos en diseñar y revisar el circuito en el software. Decidimos utilizar el CD40106 como oscilador, ya que inicialmente pensábamos que requería una señal de reloj (clock) externa para funcionar. Sin embargo, al investigar más a fondo, descubrimos que el propio chip puede generar una oscilación mediante una configuración adecuada de resistencias, condensadores y compuertas Schmitt Trigger.

![esquematico-1](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/2d885f5ed1811df5a17cec7d451d679f70b9c275/12-paulafuentesm/sesion-11a/imagenes/esquematico-1.png)

Una vez completado el esquemático, realizamos una revisión detallada y detectamos varios aspectos que debían corregirse antes de avanzar a la fabricación o prueba del circuito.

En el segudo bloque teniamos todos los componentes por lo que pudimos armarlo, esto nos hizo darnos cuenta de algunos errores. 

![propuesta01](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/d3ded8bb6f8ecf4b81141c8559e627387f332b99/12-paulafuentesm/sesion-11a/imagenes/propuesta01.jpg)

### Problemas que pudimos ver despues ( arreglar ): 

+ Falta una etapa de amplificación de audio para alimentar correctamente el parlante y que el sonido pueda salir más fuerte. No está definida una salida de audio final para conectar el parlante.

+ Existen errores en la conexión de algunas patas del LM324, impidiendo un procesamiento adecuado de la señal.
  
+ Faltan los valores de algunos componentes, especialmente condensadores, lo que dificulta determinar la frecuencia de funcionamiento del circuito.

+ Se debe revisar la orientación de los diodos para asegurar que las rutas de carga y descarga funcionen según lo esperado. ( estan al reves)

## Propuesta 02: chip 4040
Funcionamiento fue investigado a partir de referencias encontradas en internet (clase anterior). Debido a esto, aún no contábamos con la certeza suficiente para montarlo físicamente en protoboard y comprobar su funcionamiento. ( quisimos primero qu ela propuesta 1 funcionara bien hasta de empezar esté)

El esquematico quedó en este estado inicial con el objetivo de revisarlo posteriormente, identificar posibles errores y realizar las correcciones necesarias antes de fabricar la placa o comenzar las pruebas prácticas.

![esquematico-2](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/2d885f5ed1811df5a17cec7d451d679f70b9c275/12-paulafuentesm/sesion-11a/imagenes/esquematico-2.png)

### Problemas que pudimos ver despues ( arreglar ): 
+ No se ha verificado experimentalmente el funcionamiento del circuito en protoboard.

+ Falta comprobar que el CD4040 esté recibiendo una señal de reloj adecuada para realizar el conteo.

+ No se observan valores definidos para algunos componentes, como el condensador C1. ( probar en proto )

+ No se incluye una etapa de amplificación de audio para conectar directamente un parlante.

+ Aún falta realizar pruebas para confirmar que el rango de frecuencias obtenido sea útil para la generación de sonido.
  
+ Colocar en el esquematico el diagrama de energia y led para ver si funciona
