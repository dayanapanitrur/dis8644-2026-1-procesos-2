# sesion-10b

### Flusser, cap. 6, 7

**Capítulo 6:**  En este capítulo se habla de que hay cuatro métodos de discursos, refiriéndose a discursos como la fase en que se distribuye la información producida por un diálogo y específicamente en el cuarto método,  el emisor envía su información al espacio vacío, como en la comunicación por radio, produciendo una “masificación”.

+ La distribución de fotografías aplica a este método de discurso.

+ A pesar de que las fotografías se pueden reproducir de mano en mano se han creado aparatos innumerables para distribución fotografía, que poseen un programa, “el cual programa a la sociedad”.

Acá también se habla de los canales de información donde se reproduce la fotografía y dependiendo del canal de información, la fotografía tiene un diferente significado, así como puede pasar de un significado artístico, comercial, científico, etc. El trabajo del fotógrafo también depende del canal, es decir, al tomar la fotografía el fotógrafo está pensando en un canal específico de distribución y esto influye en cómo toma la fotografía.  

**Capítulo 7:** Primero empieza comparando al fotógrafo con un jugador de ajedrez, por su profundo interés en descubrir formas novedosas  y producir situaciones nuevas e informativas. También ,menciona que la función del texto está subordinada a la función de la imagen, el texto no explica la fotografía, la sustenta porque preferimos apoyarnos en ella y nos libera de un pensamiento conceptual y hace innecesario el cuestionarnos la búsqueda de causa y efecto. 

+ Las fotografías constituyen un “círculo mágico” y Flusser nos está incitando a que este círculo es lo que debemos traspasar. 


## Apuntes en clase: 

En esta clase tomé apuntes del libro "Make electronic music from scratch" para reforzar la materia sobre los osciladores, primero anoté algo importante que sale en el libro y que mencionó el profe Aaron en la clase:

**¿Cual es la diferencia entre un dispositivo eléctrico y un electrónico?**

Ambos usan electricidad, pero filosóficamente es distinta, un dispositivo eléctrico usa la electricidad como fuente de energía y requieren un usuario quien hace el pensamiento de su función. 

un dispositivo electrónico usa electricidad como un lenguaje, además usa señales de voltaje como una forma de comunicarse consigo mismo. Utiliza cantidad diminuta de voltaje para cada función del dispositivo. 

Por ejemplo : 

+ Los circuitos eléctricos es como ver una maratón y corren en círculos 

+ Los circuitos electrónicos parecen corredores atravesando pista de obstáculos y en cada obstáculo sus cuerpos reaccionan de forma interesante e inesperada 

### Osciladores: 

**“El corazón del sintetizador es el oscilador”** se mueve de un lado al otro entre dos extremos. 

+ Oscilador electrónico: se refiere a un circuito que produce una onda repetitiva de voltaje. Se usa esa onda de voltaje para mover la frecuencia que queremos. 


### Circuito IC

Son pequeñas cajas negras llenas de resistencias, capacitores, diodos y otro componentes. 

Se numeran comenzando desde la esquina inferior izquierda y siguiendo el sentido antihorario 

+ Pendiente: Leer capitulo 06: cómo combinar osciladores 
+ Capítulo 13: 4046

## trabajo en proyecto 02 : 

Primero empezamos a investigar que chips podíamos conseguir y que onda se generaba 

+ consideramos: 

+ 40106 cmos
+ 4046 cmos (onda cuadrada)
+ 4093 (cuadrada) 
+ LM324 (onda cuadrada y triangular) 

(Las más sencillas de hacer son las cuadradas y la triangular)


Preguntando al profe Misa qué recomendación nos daba de chip para generar ondas de sierra y nos recomendó este esquemático para la primera propuesta: 

![ejemplo](./imagenes/ejemplo.png/)

(aca solo se considera la parte del oscilador, para nos confundirnos el profe nos ayudó a entender el esquemático específicamente del oscilador) 


![propuesta1](./imagenes/propuesta1.png/)


Para este oscilador necesitamos estos componentes que no tenemos: 

+ chip 40106 y LM324

+ LM741 y LM358  pueden ser una opción de  reemplazo de LM324

+ 4 DIODOS IN4148

**Tipo de onda que se genera:**


![onda](./imagenes/onda.png/)


Elegimos el 40106 y el LM324 porque permiten crear un oscilador simple y experimental. El circuito genera una onda cuadrada, pero produce variaciones attack y decay, acercándose a una onda sierra o triangular.  

Esto hace que la señal no sea completamente brusca como una onda cuadrada pura, sino que tenga transiciones más suaves que modifican el sonido.

