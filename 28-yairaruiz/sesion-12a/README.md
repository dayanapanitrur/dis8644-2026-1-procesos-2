# sesion-12a

## Proyecto 02 trabajo en clases

Gracias a la corrección de la clase anterior, donde habían errores en el esquemático, se pudo hacer sonar la propuesta 1. La dejamos lista, pero aún teníamos problemas con la propuesta 2 porque no oscilaba. Pau y Santi trataron de solucionarlo, pero no sabíamos cuál era el problema. Después de desarmarla varias veces, logró sonar una vez y luego murieron los chips.

Teníamos dos opciones: comprar nuevamente los chips al día siguiente y trabajar al límite, o cambiar la propuesta por los chips que sí teníamos disponibles. Así que esa fue la mejor solución.

La propuesta 2 pasó de tener cuatro chips (40106, 4040, 4051 y 40106) a una propuesta que habíamos visto desde el principio en Hackaday. Esta propuesta constaba de dos chips 40106 y funcionó muy rápido, así que fue la opción más segura.

De donde lo sacamos: https://hackaday-com.translate.goog/2015/02/04/logic-noise-sweet-sweet-oscillator-sounds/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc


Proceso: ya teniendo listas la propuestas, verificamos que los esquemáticos tuvieran los cambios actuales para dividirnos la creación de las pcb y nuestra información para la presentación. 

para poder empezar la creación de las pcb necesitabamos el diseño y concepto de las propuestas: 

### Propuesta 1:

Estábamos haciendo una lluvia de ideas y Santi recordó una conversación que tuvimos en clases sobre Chile, las playas que conocíamos y también sobre música. A partir de eso, nos recomendó La exiliada del sur de Inti-Illimani, porque tiene un párrafo que menciona al chirihue, un pajarito cuyo sonido se relacionaba muy bien con el del oscilador.
Investigando un poco más, descubrimos que la letra pertenecía a un poema de Violeta Parra, lo que nos pareció aún más interesante de citar. Por eso decidimos nombrar la propuesta Chirihue Mecanizado.

Desembarcando en Riñihue
Se vio la Violeta Parra
Sin cuerdas en la guitarra
Sin hojas en el coligüe
Una banda de chirigües
Le vino a dar un concierto

![esquemático circuito](./imagenes/esquematico-1.png)

Propuesta de diseño:

![pcb front](./imagenes/pcb-front-1.png)

![pcb back](./imagenes/pcb-back-1.png)

+ Descripción general/conceptual:

Nuestro circuito es un oscilador, cuya función es generar una forma de onda que posteriormente se convertirá en sonido. El Chirihue Mecanizado lleva su nombre gracias al parecido de su sonido con el canto de este pájaro, que posee una melodía particular donde repite sonidos extremadamente cortos y agudos de manera continua, variando de cierta forma tanto en la tonalidad como en el ritmo.

Esta propuesta lleva el apellido “Mecanizado” porque nuestros sonidos se encuentran limitados por las condiciones de la máquina y, aunque quisiéramos, no podríamos imitar su canto original, creado por la naturaleza. Por lo tanto, esta es nuestra reinterpretación de su voz.

+ ¿Cómo funciona?

Nuestro circuito está compuesto por los chips 40106 y LM324, los cuales nos permiten crear un oscilador simple y experimental. Este tipo de circuito genera una onda cuadrada, pero al producir variaciones en el attack y decay (ataque y decaimiento), puede acercarse al comportamiento sonoro de una onda de sierra o triangular.
De esta manera, logramos obtener sonidos cortos, repetitivos y variables que recuerdan al canto del chirihue, reinterpretándolo a través de medios electrónicos.

### Propuesta 2:

El sonido de este oscilador nos recordó mucho a un teléfono, por lo que lo relacionamos con las comunicaciones. A partir de esa idea aparecieron las comunicaciones espaciales y la lógica de los satélites. Cata mencionó una parte del cuento Caleidoscopio de Ray Bradbury, sobre unos astronautas cuya nave explota y quedan flotando en el espacio, reflexionando mientras esperan la muerte.

Nos pareció interesante la relación con las comunicaciones a distancia y las señales de radio en medio de la inmensidad del espacio, especialmente por este fragmento:

"Espacio, miles de kilómetros de espacio, y voces vibrando en su centro. Ningún hombre al alcance de la vista, sólo las ondas de radio se agitaban tratando de emocionar a otros hombres".


![esquemático circuito](./imagenes/esquematico-2.png)

+ Descripción general/conceptual

El sonido generado por el oscilador puede asemejarse al de una llamada o transmisión espacial dependiendo de cómo se regulan las ondas. El chip CD40106 tiene una compuerta inversora o Schmitt Trigger; si la entrada está en 0, la salida pasa a 1 y cuando la entrada está en 1, la salida pasa a 0.

Básicamente mantienen una constante comunicación para poder generar el sonido, igualando la recepción constante de señales entre la Tierra y el espacio. Somos las comunicaciones espaciales desde la tierra (humanos monitoreando la “llamada” hacia objetos en el espacio, como nosotros estamos mandando una señal mediante el potenciador/chip para así poder realizar la señas y sea audible al resto).

+ Descripción de funcionamiento

Comunicaciones Espaciales utiliza un chip CD40106 que es un inversor Schmidt Trigger, esto significa que contiene 6 inversores Schmitt Trigger independientes (si la entrada está en bajo (0), la salida está en alto (1) y viceversa) recibiendo un voltaje de 9v.

+ Diseño:

![pcb front](./imagenes/pcb-front-2.png)
![pcb back](./imagenes/pcb-back-2.png)
