# sesion-13a
Martes 09 de junio del 2026 - Lectura - Inicio Proyecto 3 / Examen

# Lectura 

### Capítulos 1 y 2 (Música y Pintura)

***La desmaterialización del objeto***, en estos capítulos, Yoko Ono plantea algo que al principio choca con nuestra formación técnica, que la obra de arte no es el objeto físico, sino la instrucción. En Música, al pedirnos que escuchemos el sonido de la nieve o el latido de un corazón, nos obliga a desplazar el foco de lo "producido" hacia la "percepción". No se trata de la partitura, sino de cómo el usuario final procesa ese estímulo.

En la sección de Pintura, esto se vuelve aún más radical. Instrucciones como "deja que la luz del sol pase a través" para crear una obra, sugieren que el arte es dinámico y depende totalmente del entorno. No es un cuadro estático colgado en una pared, es un proceso que interactúa con el medio ambiente y con el tiempo.

Como opinión personal, llevando esto al terreno del Diseño de Carcasas, la reflexión se vuelve súper interesante. Normalmente, uno piensa en una carcasa como una estructura rígida, un contenedor de hardware cuya única función es proteger o verse "bonito" (estética). Sin embargo, tras leer a Ono, entiendo que el diseño de una carcasa es, en realidad, el diseño de una interfaz sensorial.

### ¿ Qué quiere decir interfaz sensorial ?
Una interfaz es cualquier punto donde dos sistemas se encuentran (como yo y el compu). Normalmente pensamos en la pantalla, pero una interfaz sensorial se refiere a todo lo que mis sentidos perciben al interactuar con un objeto físico.

Y en relación con mi opinión sobre las carcasas, me refiero a que:

* **Tacto (Háptica):** No es solo una tapa; es si el material es suave, rugoso, frío o cálido. Eso le da una "instrucción" a tu mano de cómo agarrarlo.
* **Oído:** El sonido que hace la carcasa cuando la cierras o cuando tus dedos rozan el material.
* **Vista:** Cómo la luz rebota en la superficie (si es mate o brillante).

### ¿Por qué lo relaciono con Yoko Ono? 
Porque Yoko dice que la obra no es el cuadro, sino lo que uno siente al leer la instrucción. Al diseñar una carcasa, lo que estoy diseñando no es solo "una caja de plástico", sino la experiencia sensorial de la persona que la va a usar.

 **En resumen:** Decir que la carcasa es una "interfaz sensorial" significa que el objeto sirve para conectar al ser humano con la tecnología a través de los sentidos, no solo de la vista.

* **Más allá de lo físico:** Al igual que en su "Música", donde el silencio es parte de la obra, en una carcasa el "vacío", la textura y el peso comunican algo. No es solo plástico o metal, es la sensación térmica al tocarlo o el sonido que hace al encajar. Estas secciones me hicieron ver que diseñar una carcasa es diseñar la experiencia de sostener el objeto.
  
---

* **Intención y Visibilidad:** Yoko nos enseña a "ver lo invisible". En el diseño técnico, esto se traduce en la intención detrás de cada curva o cada material. Si una carcasa es translúcida, no es solo por moda, es una instrucción visual sobre la transparencia del sistema interno.
  
---

* **El objeto como proceso:** Así como sus "Pinturas" cambian con la luz, una carcasa interactúa con el usuario, se desgasta, se ensucia, se personaliza. Aprender que el diseño no termina cuando sale de la fábrica, sino que continúa en manos del usuario, me dio una perspectiva mucho más amplia para mi proyecto. Es entender que estamos diseñando soportes para la vida cotidiana, no solo cajas para cables.

### Conversación en clases

Hablamos de distintos temas al inicio. Luego hablaron de los arreglos que le hicieron a nuestras PCBs para poder mandarlas a fabricar y que pudieran funcionar. Nos hicieron comentarios sobre todos los ajustes realizados a cada grupo, como la colocación de resistencias, huellas, etc. Cada grupo tiene obligatoriamente una placa que se mandará a hacer. Comentaron que el jack no lo entendimos bien o no quedó claro cómo funcionaba.

## Guía de Exportación desde KiCad - Nos subiran video más a detalle 

 **Antes de empezar:** Asegúrarse de que las zonas de cobre estén rellenas y pasa el DRC para evitar errores de última hora.

### 1. Selección de Capas (Las 7 obligatorias)

Para que el fabricante acepte el diseño, se debe incluir estas capas en la sección de **Trazar (Plot)**:

1. `Edge.Cuts` — Contorno de la placa
2. `F.Cu` — Cobre superior
3. `B.Cu` — Cobre inferior
4. `F.Mask` — Máscara de soldadura frontal
5. `B.Mask` — Máscara de soldadura trasera
6. `F.Silkscreen` — Serigrafía/Texto frontal
7. `B.Silkscreen` — Serigrafía/Texto trasero

### 2. Generación de Archivos

- **Gerbers:** En la ventana de "Trazar", seleccionar la carpeta de destino y hacer clic en **Trazar**. Se crearán los archivos `.gbr`.
- **Taladrado:** Hacer clic en **Generar archivos de taladrado**. Es vital para que la máquina sepa dónde hacer los huecos. Se generan los archivos `.drl`.

### 3. Verificación y Entrega

1. **Visor Gerber:** Usar el visualizador de KiCad para cargar todos los archivos. Revisar que el contorno esté bien definido y que los agujeros coincidan con los pads.
2. **Empaquetado:** Seleccionar todos los archivos de la carpeta (`.gbr`, `.drl`, `.gbrjob`), hacer clic derecho y eligir **Comprimir en .zip**.

**Material de Trabajo:** Los profes subieron una carpeta con la versión corregida de nuestros diseños. La ruta es: Archivos > Producción > [Nombre del archivo].zip

### Sobre JLCPCB (Fabricación)

Los profes nos explicaron que esta es la plataforma que se usaron para mandar a fabricar las placas a China. 

* **Plataforma de fabricación:** Es la web donde se cargan los archivos finales para que las máquinas en China impriman el circuito.
* **Carga del ZIP:** Solo hay que arrastrar el archivo .zip que generamos (con los Gerbers y el archivo de taladrado).
* **Visualización automática:** La página tiene su propio visor que permite ver cómo quedará la placa físicamente antes de pagar.
* **Parámetros estándar:** Aunque hay muchas opciones, los profes nos guían para elegir lo básico (material FR-4, grosor de 1.6mm y 2 capas).
* **Producción real:** Es el paso final para pasar del diseño digital en KiCad a tener la placa física en nuestras manos.

Hablamos sobre las cuotas y el costo de la producción. Los profes financiarán gran parte del gasto, ya que muchos de los materiales se quedarán en el laboratorio, por eso, en el fondo, esto termina siendo una inversión para el LIB (por lo que entendí).

###  Carcasa y Experiencia de Usuario (UX)

Entramos al tema de cómo "vestir" el proyecto para que no parezca solo un experimento de ingeniería, sino un producto pensado para el usuario.

**Referencias de diseño**
  
* **Macumbista (Banjolin):** Uso de cajas de madera (como las de joyas) adaptadas.
* **Corazón Robota:** Uso de cajas de bombones o chocolates.
* **Victor Mazón (Signum):** Estilo con todo el circuito a la vista, usando separadores para levantar las placas.
* **Bleep Labs:** Otros referentes de estética DIY.

**Estándares y Decisiones**
  
* **No hay un estándar impuesto:** la clave es saber explicar a la comisión por qué elegimos esa estética.
* **Dato de UX:** El volumen normalmente sube hacia la derecha. Si lo hacemos al revés, hay que saber justificarlo.
* **Colaboración:** Se puede poblar la placa propia, trabajar en duplas o incluso intercambiar/mezclar placas con otros grupos.

### Materiales y Formatos

* **Hammond Boxes:** Cajas de aluminio clásicas (vistas en la tienda Katode).
* **Eurorack DIY:** Formatos tipo "sándwich" o placas montadas en ángulo.
* **Perfboard:** Placas perforadas para prototipar rápido o modificar circuitos sin tener que mandar a pedir a China (siempre que se explique el porqué).

**Montaje**
  
* **Separadores:** Pueden ser de plástico (Victronics) o usar pernos M3 como opción más barata para separar placas o hacer sándwiches.
* **Impresión 3D:** También es una opción válida para la carcasa.

Vimos referentes de carcasas (Macumbista, Corazón Robota, Victor Mazón) y opciones de montaje como las Hammond Boxes de Katode o el uso de separadores y pernos M3. El enfoque es la experiencia de usuario y ser capaces de justificar cada decisión de diseño ante la comisión.

El examen vale un 50% de la nota final, los profes en esta situación son nuestros abogados en caso de que algo no se entienda al momento de que expliquemos el trabajo. 

* Hicieron una votación sobre si manteniamos los grupos y ganó el que sí, luego nos explicaron las intrucciones del examen.

* Si o si, soldar 3 placas. 
* lista de materiales
* Propuesta de 2 partituras para performance de 5 minutos con el sintetizador diseñado

**FORO llllllll.cl** hablan sobre los sintetizadores que nos puede ayudar.
**PODEMOS AGREGAR LDR EN VEZ DE POTENCIOMETROS PAR OBTENER MEJOR SONIDO**

**PROXIMO MARTES TENDREMOS LAS PCBS EN MANOS**
**EXAMEN 07-06/10 QUEDA UN MES**
