# sesion-09a

# Apuntes clase 12/05

Esta clase tuvo que ser mediante zoom debido a un incendio en república, lo cual hace un poco más difícil el trabajo ya que estamos usando el computador para trabajar y para ver la clase al mismo tiempo, lo cual es un poco confuso y nos puede distraer.

### Repaso rápido de KiCad

Para iniciar la materia nos hicieron un repaso rápido de cómo se utiliza KiCad, lo cual agradezco bastante ya que se me habían olvidado las siguientes cosas:

+ Para modificar el tamaño de la lámina en la cual estamos trabajando tenemos que hacer doble click dentro de la viñeta que se encuentra en la esquina abajo a la derecha.
+ Con click derecho se puede eliminar la asignación de una huella dentro del panel de asignación de huellas.
+ Para asignar huellas de manera más directa, selecciona el símbolo y presiona la tecla ``F`` de _footprint_ (huella).
+ ``Alt + 3`` para entrar al visor 3D.

### Capas de cobre

``F.Cu`` y ``B.Cu`` son las capas en donde se encuentran las pistas de cobre (las cuales son el equivalente a los cables dentro de nuestra protoboard) en donde una trabaja por el lado frontal (``F.Cu``) y la otra trabaja por el lado de atrás (``B.Cu``). Podemos tener distintos anchos en las pistas, los cuales tienen que ser mínimo de 0.3 mm.

Para poder añadir y editar grosores tenemos que hacerlo en la esquina superior izquierda donde se menciona la "Pista", luego de hacer click nos aparecerá la opción de ``Editar tamaños predefinidos...`` que es en donde podremos añadir y editar grosores para las pistas.

![Opciones de tamaños](./imagenes/editar-tamano.png)

Cuando hagamos click en la opción que se muestra en la imagen anterior, nos aparecerá que estamos en la sección de ``Reglas de diseño -> Tamaños predefinidos``. Ya estando en este lugar, tenemos que presionar el símbolo ``+`` que se encuentra en la sección inferior de ``Pistas`` como se muestra en la siguiente imagen:

![Agrego de tamaños](./imagenes/tamanos-predefinidos.png)

Cuando presionamos el símbolo ``+`` ya podremos agregar los tamaños que queremos, que en nuestro caso fue de 0.4mm y 0.8mm.

Como ya tenemos los grosores deseados, podemos empezar a crear las pistas ubicándonos en la capa correspondiente (``F.Cu`` o ``B.Cu``) y seleccionando la herramienta de ``Enrutar Pista Única`` o apretando la tecla ``X``.

![Herramienta para hacer las pistas](./imagenes/enrutar-pista.png)

Luego de aprender ésto, empezamos a hacer las conexiones positivas ya que Misa dijo que es mejor dejar el GND para el final con una herramienta que lo hace más rápido, por lo que seleccionamos la herramienta de ``Enrutar Pista Única`` y empezamos a conectar las cosas a VCC. Para evitar que se toquen las pistas, puedes ir turnando entre el lado frontal y el lado trasero, pero en el caso de que aún así no puedas hacerlo sin pasar a llevar otra pista, puedes usar la opción de ``Vías``, las cuales se hacen con la misma opción de enrutar pistas pero cuando quieras cambiar del lado frontal al trasero (o al revés), tienes que presionar la tecla ``V`` y se hará un orificio por donde viajará la pista de una cara de la PCB a la otra. Para poder editar el tamaño de la vía, tenemos que hacer el mismo proceso que se hizo con las pistas solo que ésta vez presionaremos el símbolo ``+`` que está en la columna de ``Vías``.

![Tamaños para vías](./imagenes/editar-vias.png)

Cuando ya tengamos todos los positivos conectados entre sí, Misa nos indicó que utilicemos la herramienta de ``Dibujar Zonas Rellenas`` que nos aparece al costado derecho o simplemente podemos hacer ``Ctrl + Shift + Z``. 

![Herramienta zonas rellenas](./imagenes/zonas-rellenas.png)

Una vez la seleccionemos, haremos click en nuestra tabla de trabajo y nos aparecerán las propiedades de la zona, en donde tenemos que ponerle un nombre a ésta y luego asignarle el "Nombre de red", en el cual tenemos que seleccionar la opción de ``GND``. Luego de delimitar el espacio (el cual no importa que sea más grande que la PCB con tal de que la abarque por completo) tenemos que presionar la tecla ``B``, lo cual hará que se rellenen todos los espacios en GND.

![Opciones nombre de red](./imagenes/gnd.png)

Para poder montar nuestra PCB a nuestra carcasa, tenemos que hacerle hoyos para poder poner separadores o pernos (los pernos son la opción más barata), por lo que Misa nos recomienda su tamaño predeterminado que es para el perno M3. Para poder añadir los espacios para los pernos, hay que buscar en símbolos la opción de ``Mounting Hole`` y pondremos cuatro en nuestro esquemático. Luego de tenerlo en el esquemático, le añadimos la huella ``mounting hole 3.2mm`` que corresponde al M3 para luego pasarlo al editor de placas y poder ubicarlos en donde nos guste.

> DATO: para poder importar vectores, hay que descargar un archivo .dxf o podemos hacer nuestro propio vector, ir a archivo, seleccionar la opción de importar gráficos, buscamos nuestra imagen y podremos modificar su escala si es necesario.

---

# Encargos

### KiCad

Como encargo se nos indicó practicar lo que aprendimos en la clase, lo cual fue hacer esquemáticos y PCB. Para practicar, tenemos que elegir dos de las cuatro partes que componen nuestro sintetizador (el que realizamos para el gran proyecto 01) y replicarlo en KiCad, tanto el esquemático con nuestras modificaciones como la PCB de éste.

Para éste encargo decidí hacer la sección del reloj (chip 555) y del amplificador (lm386), en el cual solo hicimos unos cambios en la sección del 555. Al momento de hacer el esquemático del 555 no tuve mucho problema fuera del hecho de que me molestó el orden de los pins, ya que el pin 5 se encuentra en la parte superior siendo que va directo a GND, lo cual intenté cambiar buscando información en google (terminé en este link: <https://www.build-electronic-circuits.com/how-to-edit-symbol-in-kicad/>) en donde me indicaron que tenía que hacer una copia del símbolo para poder editarlo dentro de una biblioteca nueva, pero al momento de hacer eso solo me permitía editar el ``NE555D`` y no el ``NE555P``, lo cual se me hizo raro y preferí dejarlo como viene por default ya que solo es tirar un cable para al lado, no sé por qué me molestó tanto en su momento la verdad.

Cuando terminé de mover los componentes y unirlos, llegó el momento de asignar huellas y utilicé las que nos habían mencionado la clase antes pasada, los cuales son los siguientes:

+ Capacitores cerámicos: ``Capacitor_THT:C_Disc_D3.8mm_W2.6mm_P2.50mm``
+ Resistencias: ``Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal``
+ Capacitores con polaridad: ``Capacitor_THT:CP_Radial_D5.0mm_P2.50mm``
+ LEDs: ``LED_THT:LED_D5.0mm``
+ Potenciómetro: ``Potentiometer_THT:Potentiometer_Alps_RK163_Single_Horizontal``
+ Parlante: ``TerminalBlock:TerminalBlock_MaiXu_MX126-5.0-02P_1x02_P5.00mm``
+ Chip de 8 pins (555 y lm386): ``Package_DIP:DIP-8_W7.62mm``
+ Batería 9V: ``TerminalBlock:TerminalBlock_MaiXu_MX126-5.0-02P_1x02_P5.00mm``
+ Separadores: ``MountingHole:MountingHole_3.2mm_M3``

Una vez ya agregadas las huellas, di el esquemático por terminado y quedó así:

![Esquemático 555 sintetizador "Tincado"](./imagenes/clock-synth-tincado.jpg)

Como ya todos los símbolos tenían sus huellas asignadas, pasé todos los elementos al modo placa para poder empezar a editar mi PCB. Como tamaño elegí hacer un rectángulo de 90 x 55 mm (tamaño de tarjeta de presentación) y dejé las puntas redondeadas con un radio de 7mm. Como ya tenía el límite definido, empecé a ordenar los componentes y luego hice las pistas de cobre de todos los positivos para dejar los negativos al final. Cuando terminé de hacer las pistas, me di cuenta que no había cambiado su tamaño por lo que borré todo (que no es mucho la verdad) y lo hice con los tamaños que utilizamos durante la clase, lo que me dejó la duda de si es posible editar el tamaño después de haber hecho todas las pistas o si necesariamente tiene que ser antes de partir con todo. Cuando terminé de hacer las pistas (incluyendo las que tienen vías) quise poner un vector ya que se veía muy vacío el lado derecho de la placa, por lo que seguí los pasos que nos mostraron en clases y puse un vector de snoopy junto a una de las frases que más usan los fans de Peanuts, lo cual quedó así:

![Lado frontal de la PCB](./imagenes/pistas-frontales.png)

![Lado trasero de la PCB](./imagenes/pistas-traseras.png)

![PCB por ambos lados](./imagenes/total-pcb.png)

![Render PCB](./imagenes/pcb-render.png)
