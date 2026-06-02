# sesion-10b
## 22, May
## Apuntes
No pude ir a esta clase porque estaba enferma pero mis compañeros me pasaron sus apuntes <3
### Electricidad vs. Electrónica 

A veces se confunden, pero en la clase quedó claro que hacen cosas muy distintas:

* **Electricidad:** Es la energía pura que viaja por el circuito. Lo que hace que las cosas simplemente prendan (cables, baterías, enchufes).
* **Electrónica:** Es la información y el control. Es cómo organizamos y manipulamos esa energía mediante componentes para que haga tareas específicas y súper precisas.
* Ejemplo rápido: En una lámpara, la corriente que viaja es electricidad, pero el sistema que decide cómo y cuándo regula el circuito es electrónica.
---

### Avance de Proyecto: A definir el rumbo y buscar osciladores

El gran objetivo ahora es: Buscar y definir ¡qué haremos!

¿Qué debemos hacer específicamente? Nos toca crear un oscilador o modificar radicalmente el que ya utilizamos en nuestra entrega 1.

* Recordatorio rápido: Un oscilador es un circuito electrónico capaz de convertir corriente continua (la de la batería) en corriente alterna, generando una frecuencia y una forma de onda específicas. Básicamente actúa como un "metrónomo" o señal de reloj. Es fundamental para sincronizar sistemas, crear tonos en instrumentos musicales o portar señales de radio.

**Buscando en Hackaday**

Nos pusimos a indagar por la página de **Hackaday** (que tiene proyectos increíbles de electrónica) buscando circuitos y formas de modificar nuestro oscilador base. Entre tanta búsqueda, encontramos una opción súper interesante usando un chip nuevo que nos llamó mucho la atención.

**Nuestra Opción 1: Utilizar el chip CD4046**

Este integrado es un bucle bloqueado por fase (PLL). Los PLL son circuitos dulces y verdaderas joyitas de la electrónica. En su uso normal, tú le metes una forma de onda con una frecuencia dada y el chip te tira una onda cuadrada sincronizada, pero a una frecuencia más alta.

* **Tiene un VCO (Oscilador Controlado por Voltaje)** integrado en su interior. Al ser controlado por voltaje, podemos cambiar el tono del sonido de una manera mucho más dinámica y loca introduciendo variaciones de tensión.
* **Pines clave que anotamos:** La entrada de voltaje para controlar el VCO está en el **pin 9**, y la salida de la onda sonora está en el **pin 4**.
  
El CD4046B es un chip CMOS de bajo consumo que consta de este oscilador lineal (VCO) y dos comparadores de fase diferentes que comparten entradas.

¡Eso por el momento! El siguiente paso es ver si armamos el esquemático, calcular bien los componentes y empezar a tirar cables para ver si resulta. <3

---
 
### . Conceptos Filosóficos (Sobre las lecturas) 

* **El gusto vs. El criterio:** El gusto es súper subjetivo y no se puede discutir, pero los criterios que hay detrás de un diseño o una obra sí se conversan.
* **Fenomenología (Husserl):** Movimiento filosófico que estudia cómo aparecen los fenómenos y cómo los experimentamos directo en nuestra conciencia, dejando de lado los prejuicios. Pero ojo, a veces se queda corto.
* **Postfenomenología (Don Ihde):** Analiza cómo la tecnología media en nuestra experiencia. Ya no somos "sujetos aislados mirando objetos", sino que las tecnologías arman nuestra realidad y definen cómo percibimos el mundo. Al final, la sensación más verdadera es cuando tocas las cosas físicamente.

### Lectura Vilém Flusser

* **Capítulo 6 (Distribución):** Las fotos se masifican por la reproducción. El valor no está en el papel físico, sino en la información que transmiten. Al volverse un flujo constante, terminan influyendo en cómo actuamos y entendemos el mundo (igualito a lo que pasa hoy con las redes sociales).
* **Capítulo 7 (Recepción):** La gente suele ver las fotos muy por encima sin cuestionar el trasfondo. Interpretar imágenes es tan importante como saber leer. Hay dos conceptos clave aquí:
* **Diálogo:** Es donde se produce la información.
* **Discurso:** Es cómo se almacena en nuestras memorias. Como tiene un factor interpretativo y propio de cada uno según su contexto, se termina generando un *metadiscurso*. Una foto nunca es un elemento objetivo, siempre está sujeta a interpretación.
