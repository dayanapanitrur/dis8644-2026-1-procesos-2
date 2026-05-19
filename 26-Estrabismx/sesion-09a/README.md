# sesion-09a

## KiCad 2: la venganza ##

---

Dejo esto como recordatorio no solo para mí, para quien le sirva. Hagan commit cada 5 minutos aprox. Perdí todo el avance de esta sesión por ese descuido, asi que acá vamos otra vez 

---

### Paso 4: Definir Pistas ###

- Vamos a definir el tamaño de las pistas y las vias, en simple palabras el ⊘ del cable. Estas pueden ser por ambos lados de la PCB

  > Pista: Simil de lo que es un cable
  >
  > Via: Es una perforación rellena de cobre, que conecta 2 o más caras de una PCB, en este caso la cara superior e inferior

  ![Captura de Pantalla](./imagenes/sc24.png)

<br>

  + Para definir las pistas se selecciona esa opción y se escribe la información pertinente, en nuestro caso estamos utilizando 0.4mm y 0.8mmm
  
  + Al lado tambien aparece la opción de Vias, siendo los valores 0.3mm y 0.6mm correspondientes

  + Estos valores se basan en las tolerancias propuestas por el fabricante que vamos a utilizar ***JLCPCB***, en su apartado de _capabilities_ ➙ [https://jlcpcb.com/capabilities/pcb-capabilities]

    ![Captura de Pantalla](./imagenes/sc25.png)

<br>

### Paso 5: Repartir componentes ###

Acá es donde decidimos la distribución de cada componente, es decir, establecemos la interfaz con el usuario.

Puntos a considerar:

- Debe exisitir cierto espacio entre cada componente, para el paso de las pistas entre ellos

- Al mover cada componente se aprecia una tenue línea que se conecta a otros componentes, esta nos indica con cuales se relaciona directamente. Estas líneas son dinámicas, es decir que si posee más de una posible conexión, va a priorizar mostrar la más cercana

  ![Captura de Pantalla](./imagenes/sc16.png)

  ![Captura de Pantalla](./imagenes/sc17.png)

> Para visualizar el modo 3D ➙ _CTRL_ + _3_

<br>

  ![Captura de Pantalla](./imagenes/sc18.png)

<br>

### Paso 6: Rutear componentes ###

Ahora con las vias y pistas vamos a conectar todas las terminales, a excepción de todo lo GND, esto es porque vamos a utilizar otro proceso

- Vamos a conectar pistas alternando caras, cuando no podamos por espacio utilizaremos vías

    + Al iniciar a trazar ➙ _X_, se va a seleccionar una terminal, luego se van a remarcar con cuales podemos conectar, seguiremos este proceso una y otra vez

- Una vez este todo conectado (menos GND como mencioné), se va a _"pintar"_ el resto de la placa como tierra, esto se hace con ➙ _CTRL_ + _SHIFT_ + _Z_


  ![Captura de Pantalla](./imagenes/sc26.png)

> Utilizamos la config que aparece en la imagen

<br>

- Ahora encerramos por fuera el contorno y clickeamos _B_ (por background)

  ![Captura de Pantalla](./imagenes/sc27.png)

  ![Captura de Pantalla](./imagenes/sc21.png)

  ![Captura de Pantalla](./imagenes/sc22.png)

<br>

### Paso 7: Exportar ###

El nombre lo dice todo

---

## Aprendizajes ##

- Como mencione antes, hacer commits constantes 😞

- Tambien fijarse en el encapsulado de los chips para seleccionar la huella, nosotros usamos constantemente DIN. Anteriormente confundí la huella y utuliza una SOIC,

<br>

## Libro: Hacia una Filosofía de la fotgrafía ##

Este libro de Flusser no plantea una verdad, sino que es una invitación a reflexionar ¿sobre que?

Sobre como las imagenes han visto afectada sus interpretaciones, considerando que inicialmente las personas no leían y las pinturas y vitrales eran un medio para dar a conocer la palabra de Dios. Es decir que en un inicio se tenía una función más decriptiva de la _"realidad"_, unra representación de lo que está escrito

Una vez que la invención de la cámara ocurre, el paradigma de la pintura cambia, está se vuelca en la expresión, en representar el sentir, el pensar. Se vuelven medios de representación más simbolica, esto termina ocurriendo de igual manera con la fotografía, puesto que la gente en un momento empezó a experimentar y entender que una cámara no congela un instante en el tiempo, ese instante posee contexto, por lo que una imagen una imagen no es una verdad absoluta, es una interpretación de la realidad o de lo que nosotros entendemos.

Es importante rescatar que todo este proceso no solo ocurre con ambos medios, sino que tambien debemos entender como esto afecta y se relaciona con la escritura. Cuando empezamos a ver la profundidad que refleja una sola fotografía, empezamos a definirla, es decir, reduciarla a palabras, las que a su vez reducen la interpretación de esta realidad.

De momento hay todavia más capítulos del libro, seguire leyendo y profundizando estas reflexiones que me parecen interesantes, no solo por la premisa, si no por el planteamiento que esto es algo que ocurre y seguira ocurriendo por la naturaleza del medio
