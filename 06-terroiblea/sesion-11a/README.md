# sesion-11a

Martes 26 de Mayo, 2026.

Nota del día: dato curioso: exactamente hoy paso un mes de mi cumple!! 

## Referentes (y otras cosas)

- elevator music <https://www.youtube.com/@ElevatorMusicLive>
- Rainer Krause (hizo la exposición "Llluvia" junto con Misaa, a fin de año van a hacer otra exposición que se llama "Viento") <https://rkrause.cl/milimetropolis/>

## Qué hice hoy 

### Desglose trabajo - parte 01 

 (esto fue hecho con ayuda de chatGPT, me sirvió para poder entender mejor cada parte del proyecto y qué es lo que estamos haciendo)

“Logic Noise: Filters And Drums” de Hackaday - <https://hackaday.com/2015/03/25/logic-noise-filters-and-drums/>. 

Es básicamente un sintetizador de percusión analógico hecho con chips CMOS, resistencias y capacitores. NO usa un microcontrolador ni samples ya que el sonido percusivo sale de un filtro resonante que “suena” cuando recibe un pulso.

¿Qué está intentando hacer el circuito?

- Generar un “golpe” eléctrico muy corto (trigger).
- Mandarlo a un filtro resonante.
- El filtro empieza a oscilar por un instante.
- Esa oscilación se apaga lentamente.
- Eso produce el “TUM” percusivo.

El concepto MÁS importante: “ringing” - Cuando golpeas una cuerda, un tambor, una mesa, no suenan eternamente. Suele hacer algo como "TUMMmmm.." (y se muere). Entonces hay que lograr que el circuito haga eso mismo.

El filtro Twin-T entra en resonancia por un momento y luego **decae**. Ese decaimiento ES el **sonido percusivo**.

En la siguiente foto se ve como funciona esa bajada. En vez de completar la oscilación normal (amarillo), llega al pick y cae (verde).

![funcionamiento](./imagenes/funcionamiento.png)

#### Componentes 

- CD4069UB (importante que sea “UB” (unbuffered), el 4069EB no funciona igual).
- CD40106 (oscilador de trigger, genera pulsos automáticamente).
- Resistencias de 1K, 10k, 22k, 47k, 100k, etc.
- Potenciómetros de 100k
- Capacitores (importantes para el tono) 10nF, 22nF, 100nF, 1uF

Recordar: Mientras MÁS grande el capacitor, más grave el drum. Mientras MÁS pequeño, más agudo el sonido. 

Extras (generales):

- protoboard.
- cables.
- caimanes.
- amplificador/audio interface.

Información 4069UB: <https://hackaday.com/2015/03/09/logic-noise-sawing-away-with-analog-waveforms/> (¿"For starters, let’s aim to get a voltage gain of -1"?)

#### Explicación

El circuito comienza con un CD40106 configurado como oscilador, que genera una señal cuadrada alternando continuamente entre encendido y apagado (ON/OFF), funcionando únicamente como un reloj electrónico. Esta señal pasa luego por un capacitor, que elimina la parte continua de la onda y deja únicamente los cambios bruscos de voltaje, produciendo pulsos extremadamente cortos llamados triggers. Estos triggers se envían a un filtro resonante Twin-T, formado por resistencias y capacitores dispuestos en una configuración de doble “T”. El filtro posee una frecuencia natural de resonancia y, al recibir cada trigger, comienza a oscilar brevemente en esa frecuencia de la misma manera que una campana vibra después de ser golpeada. Dependiendo de los valores de sus componentes, puede resonar en frecuencias graves (por ejemplo 80 Hz para un bombo), medias (200 Hz para un tom) o más agudas (500 Hz para un bongo). La señal resultante es amplificada mediante un CD4069UB utilizado fuera de su propósito habitual como compuerta lógica, actuando aquí como amplificador analógico para reforzar la resonancia y aumentar la duración del sonido. La característica percusiva se consigue porque el Twin-T está ligeramente desajustado (detuned): si estuviera perfectamente calibrado oscilaría indefinidamente como una senoide continua, pero al descalibrarlo pierde energía gradualmente y la oscilación se extingue por sí sola, generando el típico decaimiento (decay) de un tambor. Finalmente, el tono (pitch) del sonido puede modificarse cambiando los valores de las resistencias y capacitores del filtro; en general, mayores valores producen sonidos más graves y menores valores producen sonidos más agudos.

- Flujo total
  
40106 oscillator
↓
capacitor trigger
↓
Twin-T resonator
↓
4069UB amplifier
↓
lowpass filter
↓
audio out

#### Recomendación 

NO copies todo de una (circuito entero, no hacerlo de una)

Hazlo modular:
- oscilador.
- trigger.
- resonador.
- filtro.
- salida.
  
Así entiendes qué está haciendo cada parte. Y en caso de algo te puedes dar cuenta si algo funciona o si algo no funciona. Es mejor que funcionen por separado y despues ir conectando todo. 

## Qué hice hoy

Comenzamos a armar la idea 1 de proyecto (circuito).

En el esquematico no sale pero: 

En el 40106 y en el 4069UB:

- pin 14 a VCC.
- pin 7 a GND.

No nos funciono a la primera y no logramos igualar el sonido al que sale en el video, pero Aarón dijo que servía igual por que percutaba. 

Para modificar el sonido cambiamos algunas resistencias y capacitadores buscando hacer que el sonido sea mas grave. 

![trabajo_en_clase](./imagenes/trabajo.png)

- Esquema idea de circuito (idea 2): (realizado por carla)

misma base, solo cambia el oscilador inicial, en este caso como idea base es empezar por un 555 para ver como resulta. 

![esquema](./imagenes/esquema.png)
