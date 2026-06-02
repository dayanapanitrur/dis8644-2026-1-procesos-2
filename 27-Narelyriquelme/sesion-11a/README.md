# sesion-11a
## Apuntes 26, May
### Avance en KiCad y Conexiones Estándar

En esta clase nos enfocamos principalmente en avanzar con los proyectos grupales directamente en KiCad. Con nuestro grupo tomamos la decisión de trabajar en el diseño de circuitos osciladores evaluando distintas alternativas para experimentar. La sesión estuvo dividida entre el diseño digital de los esquemáticos en el software y una explicación teórica fundamental que nos dio el profesor sobre la estandarización en sistemas modulares. Entender estos estándares nos sirve para asegurar que todas las placas que diseñemos se puedan conectar entre sí sin problemas de compatibilidad eléctrica o de señal, unificando criterios de alimentación y dimensiones para que todo calce a la perfección en un sistema compartido.

---

### Osciladores y Alternativas de Diseño

Como grupo estuvimos evaluando varias opciones, pero nos interesó trabajar con el chip CD4046. Encontramos 2 opciones que consideramos que eran las más viables:

#### Opción 1: Configuración de Oscilador de Alta Estabilidad (Hackaday)

Esta alternativa la seleccionamos desde la página de Hackaday y se centra en el uso de inversores digitales con histéresis para limpiar cualquier ruido presente en las etapas previas del circuito:

1. **CD40106 (Inversor Schmitt Trigger)**
* Contiene seis inversores digitales independientes con entradas de disparo Schmitt Trigger.
* Su característica clave es la histéresis, que le permite filtrar el ruido de señales inestables.
* Permite crear osciladores o generadores de ondas cuadradas utilizando solo un condensador y una resistencia.


2. **CD4046 (Bucle de Enganche de Fase - PLL)**
* Integra un oscilador controlado por tensión (VCO) y un bucle de enganche de fase (PLL).
* Es ampliamente utilizado para multiplicar frecuencias, demodular señales FM y crear conversores de tensión a frecuencia.
* Opera en un rango de voltaje de 3 V a 18 V.

![Esquematico 1](./imagenes/opcion1.jpeg)

#### Opción 2: Configuración con Temporizador y Divisor de Décadas (YouTube)

Esta segunda alternativa la sacamos desde un video de YouTube y utiliza un enfoque clásico de temporización mediante pulsos de reloj para activar secuencias de sonido de forma ordenada:

1. **NE555P (Temporizador de Precisión)**
* Es un circuito integrado temporizador de precisión altamente versátil

2. **CD4017 (Contador/Divisor de Décadas)**
* Es un circuito integrado contador/divisor de décadas.
* Es ampliamente utilizado para crear secuenciadores de luces, temporizadores y contadores.

3. **CD4046 (VCO y PLL)**
* Mantiene las mismas funciones de control por tensión descritas en la primera alternativa para modular las frecuencias del sistema.

![Esquematico 2](./imagenes/opcion2.jpeg)

---

### Estándar Eurorack y Conexiones de Placas

El profesor nos recalcó que para conectar de forma segura todos nuestros circuitos debemos respetar rigurosamente las conexiones estándar de la arquitectura Eurorack, que es un formato modular creado por Dieter Doepfer en 1995. Esto asegura que la energía y las señales se compartan sin destruir los componentes.

#### Reglas de Diseño y Dimensiones

A partir de las explicaciones del profesor, definimos los siguientes parámetros obligatorios:

1. **Dimensiones de la Placa**
* El tamaño máximo permitido para la fabricación de la placa PCB es de 10 x 10 cm.

2. **Compatibilidad Energética**
* Todos los módulos del sistema deben compartir exactamente las mismas conexiones y recibir la misma cantidad de energía para evitar diferencias de potencial dañinas.
#### Componentes de Conexión y Regulación

Siguiendo detalladamente el diagrama de *estandar.png*, configuramos los bloques de entrada, control de encendido y distribución interna:

1. **Entrada de Alimentación (`Barrel_Jack_Switch`)**
* Recibe fuentes externas de corriente continua con voltajes situados entre los 7 V y los 12 V.
* **Configuración física:** Debe conectarse con la polaridad de centro positivo.

2. **Interruptor de Encendido (`SW_SPDT`)**
* Actúa como el switch general de paso para habilitar o cortar el suministro eléctrico hacia el resto del circuito de la placa.

3. **Regulador de Voltaje (`U2` - `L7805`)**
* Nivela y estabiliza la alimentación de manera fija a 5 V.
* El circuito se alimenta estrictamente de aquí en adelante, ya que todos los chips del módulo requieren funcionar obligatoriamente con una tensión constante de 5 V.

4. **Conector de Distribución (`J5` - `Conn_01x03_Pin`)**
* Distribuye las líneas de tensión hacia las distintas etapas internas ordenadas de la siguiente manera:
* Pin 3 = 12 V
* Pin 2 = 5 V
* Pin 1 = GND (Tierra)

5. **Conexiones de Audio e Interfaz (`J4` - `AudioJack2_SwitchT`)**
* Utilizado como puerto estándar para el envío y recepción de señales de control de voltaje (VCO) y audio entre diferentes placas.
* **Modificación de Footprint:** En KiCad se debe cambiar manualmente el número de los pines al orden jerárquico 1, 2 y 3 para reemplazar correctamente la configuración nativa de tipo T/TN/S.

![Componentes Estandar](./imagenes/estandar.png)

---

### Comentario sobre Vilém Flusser (Capítulos 8 y 9)

Al leer los capítulos 8 y 9 del libro de Flusser, puedo ver cómo sus ideas conectan con lo que estamos haciendo en el taller. El autor nos plantea que los objetos y los aparatos tecnológicos que creamos no son herramientas neutras, sino que cargan con una especie de programa invisible que define cómo nos relacionamos con el mundo. Nos damos cuenta de que estamos atrapados en las reglas que el propio fabricante del hardware pensó hace décadas.

El verdadero desafío como diseñadores está en hackear ese uso predeterminado; no quedarnos solo en seguir el manual que viene de fábrica, sino usar la técnica y la flexibilidad de la electrónica para liberar nuevas posibilidades creativas que rompan con lo estructurado. Si no entendemos cómo operan esos códigos de control interno, terminamos siendo nosotros los programados por el aparato, en vez de ser nosotros quienes decidimos qué construir con él.
