# sesion-11b

29-05-2026

## Unos y Ceros

Maniqueísmo: El maniqueísmo es una antigua religión fundada por el sabio persa Mani en el siglo III d. C. Postula que el universo está regido por dos fuerzas cósmicas eternas e irreductibles: el Bien (la Luz) y el Mal (las Tinieblas), que se encuentran en constante conflicto.

1 = Blanco - Verdadero

0 = Negro - Falso

Lógica aristotélica: A = A

El principio de abstracción es un proceso mental en el que se aíslan las características esenciales de un objeto, concepto o situación, ignorando sus detalles particulares. Permite generalizar ideas, reducir la complejidad y crear modelos aplicables a múltiples escenarios.

No contradicción: A y no A a la vez.

Tercio excluido.

No todo es siempre lo mismo, o sea que yo hace 3 años no soy igual a lo que soy hoy.

---

Este fue el proceso que seguimos durante la clase:

|paso|proceso|
|----|-------|
| 1 | Empezamos armar el circuito del cd 4015 en la protoboard, para empezar hacer las pruebas en fisico |
| 2 | Se empezo a haver la v2 del circuito cd4040, con las mejoras, con las conexciones para el cd4015 |
| 3 | 1er intento, no resulto, nos olivamos de conectar las placas entre si | 
| 4 | 2do intento prendio, se prendio hasta el 4 led pero no oscila ni se reinicia, falto conectar el reset, el pin 1 iba conectado al pin 9 pero estaba mal conectado | 
| 5 | Sospechas se cambiaron los leds del paso 5 y paso 6 |
| 6 |  fallas cambiamos leds quemados malas conexiones de leds resitencias que no tocaban la plaquita |
| 7 | se cambio la resistencia del 555 de 1k a 15k y logramos hacer el circuito mas estable |
| 8 | Al cambiar las resistencia dio mas tiempo al chip mas margen temporal al tiempo, un clock mas lento hace el circuito mas estable |
