# sesion-09b

### Encargo esquemáticos y PCB en KiCad

**1. Construcción del esquemático**
   
Comencé realizando el esquemático del circuito “4 steps” basado en el temporizador 555.
Durante el proceso, el principal inconveniente fue que el orden de las patitas del chip 555 no coincidía con el esquemático de referencia que estaba utilizando. Esto me confundió al momento de conectar los componentes.

Como no sabía aún cómo modificar el orden de las patitas en KiCad, y considerando que los profesores explicarían ese tema más adelante, decidí utilizar el orden estándar entregado por KiCad.

Para resolver la conexión de manera correcta, apliqué la lógica vista en clases, priorizando la funcionalidad del circuito, especialmente manteniendo la conexión de GND cercana a la patita correspondiente (pin 5) aunque su posición visual estuviera arriba en el esquema.
El esquemático del 555 lo completé sin errores. 



![esquematico](./imagenes/esquematico.png) 



**2. Asignación de huellas**
   
En este paso no pude recordar la ubicación de ciertas cosas en la parte de biblioteca de huellas, por lo que revisé los videos de la clase para guiarme. 


![huellas](./imagenes/huellas.png) 



**3. De huellas  a PCB**

Después de asignar las huellas, seguí con el proceso de pasar el esquemático a PCB, el cual me tomó más tiempo porque  lo vimos en la clase del martes.

Primero trabajé en el contorno de la placa en la capa Edge Cuts, definiendo la forma del PCB. Luego comencé a ubicar los componentes dentro del contorno, intenté  organizarlos según la cercanía de las conexiones entre ellos para facilitar las conexiones después.

Como el circuito no tenía demasiados componentes, los acomodé de forma ordenada, pero más que nada priorizando la lógica de la conexiones.

**4. Pistas**

Primero conecté las líneas de alimentación (positivos), y luego las conexiones entre los distintos componentes.

En este proceso tuve algunos problemas, porque olvidé ajustar el tamaño de las pistas al inicio. Cuando me di cuenta, ya había avanzado bastante y no supe cómo cambiarlo en ese punto del trabajo.

También tuve una duda importante: cuando una pista no podía continuar en la misma capa debido a los cruces, los cambiaba a la capa trasera del PCB. En algunos casos continué algunas pistas en esa capa, pero no estaba segura si estaba correcta.

Entre en un momento llena de dudas con  el uso de vías, ya que no entendí completamente cuándo es mejor:

+ usar una pista en la parte frontal 
+ cambiar a la parte trasera
+ o utilizar una vía para conectar ambas


![pistas](./imagenes/pistas.png) 


**DUDAS:** 

+ ¿Cuál es la diferencia exacta entre usar una pista en otra cara y usar una vía?
+ ¿Cuándo se debe cambiar de cara y cuándo es obligatorio usar una vía?
+ ¿Cómo se puede cambiar el tamaño de las pistas después de haber comenzado, sin tener que rehacer todo?
+ ¿Cómo cambiar o reorganizar el orden de las patitas del 555 en KiCad?

**Resultado final: no agregue la conexión del negativo porque no estaba segura cómo hacerlo**

![pcb](./imagenes/pcb.png) 

De los dos módulos, decidí trabajar solo con uno para enfocarme en comprender mejor en el 555, ya que es más sencillo y me permitía avanzar de forma más clara sin confundirme con demasiada información al mismo tiempo. Aun así, el circuito con el 555 me quedó incompleto por las dudas que surgieron durante el proceso.



