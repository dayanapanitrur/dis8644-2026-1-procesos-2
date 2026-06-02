# sesion-11b
## Proyectos Solemene 

La clase comenzó con una reflexión sobre los capítulos que habíamos leído previamente y una conversación sobre el próximo libro que trabajaremos, correspondiente a Yoko Ono. Durante la discusión se destacó la importancia de desarrollar el hábito de la lectura como una herramienta para ampliar nuestra visión crítica, generar opiniones propias y fortalecer la capacidad de análisis frente a distintos temas. La idea principal fue comprender que la lectura no consiste únicamente en adquirir información, sino también en aprender a reflexionar y construir un pensamiento autónomo.

Tambien se nos enseño un nuevo elemento ( circuito de alimentación ) para incorporar en el circuito ( no olvidar ) y que todoe stengamso el mismo parametro.

![alimentacion](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/8c423e5cf4a47d012067d87f8d8234afb2660fd3/12-paulafuentesm/sesion-11b/imagenes/alimetacion.jpg)

## Propuesta 01: chip 40106
----

![esquematico-1](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/2d885f5ed1811df5a17cec7d451d679f70b9c275/12-paulafuentesm/sesion-11a/imagenes/esquematico-1.png)
Imagen: esquematico primer bloque

Durante toda la clase nos enfocamos en hacer funcionar la Propuesta 1. El objetivo principal fue montar el circuito en protoboard, corregir los errores identificados en la clase anterior y comprobar si el oscilador generaba una señal audible de manera correcta.

![protoboard-1](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/d82b160f21bbb9a748114124d96aa79e0149bc64/12-paulafuentesm/sesion-11b/imagenes/protoboard-1.jpg)

### 1er intento 
----

Armamos el circuito siguiendo el esquemático desarrollado en la clase anterior e incorporamos las correcciones que habíamos identificado durante la revisión ( foto anterior). Al conectar el parlante a la salida de audio observamos que el circuito generaba pulsaciones y que los potenciómetros modificaban correctamente el comportamiento del LED. Sin embargo, el parlante no emitía sonido o este era extremadamente bajo. En algunos momentos las pulsaciones luminosas del LED parecían coincidir con el sonido, pero posteriormente dejaban de hacerlo, generando resultados inconsistentes. Esto nos indicó que parte del circuito estaba funcionando, aunque existía algún problema en la etapa de audio o en la transmisión de la señal.

### 2do intento
----
Tras aproximadamente veinte minutos intentando encontrar el error, decidimos desmontar completamente el circuito y volver a armarlo desde cero. Aunque ya nos resultaba menos frustrante que en experiencias anteriores, fue necesario revisar cada conexión para descartar errores de montaje.

Una vez reconstruido el circuito, realizamos dos salidas distintas para comprobar si el problema se encontraba en una sección específica del diseño. Gracias a esta prueba pudimos concluir que esa parte del circuito estaba funcionando correctamente. Sin embargo, el sonido seguía siendo muy bajo y, después de un tiempo, dejó de escucharse por completo, mientras que el LED continuaba funcionando con normalidad ( locura). Esto nos permitió decir que la alimentación estaba llegando al circuito y que el problema probablemente se encontraba en e la señal de audio o en alguna conexión incorrecta relacionada con la amplificación o el oscinador ( creemos que mas por el amplificador).

Al finalizar la clase concluimos que era necesario revisar nuevamente el esquemático con mayor detalle, verificando especialmente la conexión de las patas de los circuitos integrados y la ruta completa de la señal. Con base en esta revisión realizamos nuevas modificaciones al diseño, dejando preparado un esquemático corregido para ser probado durante la siguiente clase.

![propuesta01-correc](https://github.com/paulafuentesm/dis8644-2026-1-procesos-2/blob/d82b160f21bbb9a748114124d96aa79e0149bc64/12-paulafuentesm/sesion-11b/imagenes/propuesta01-correc.png)
Imagen: esquematico con correciones. (prox. clase probar)
