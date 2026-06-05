# Clase 11b — Investigación de Sallen-Key y filtros paso alto / paso bajo

**Tema:** investigación de filtros activos, Sallen-Key y circuitos integrados  
**Objetivo:** buscar una forma de construir un filtro que pudiera funcionar como paso alto y paso bajo

---

## Resumen de la clase

En esta clase llegamos con información más investigada sobre el filtro **Sallen-Key**. La idea era entender mejor cómo funcionaba esta configuración y qué circuitos integrados podíamos usar para construir filtros activos.

Nuestro objetivo era lograr un filtro que pudiera trabajar como **paso alto** y **paso bajo**, o al menos entender cómo se podían construir ambas versiones. Esto era importante porque para el proyecto necesitábamos controlar distintas zonas de frecuencia.

Durante la clase no alcanzamos a explorar demasiado, porque todavía estábamos tratando de concretar el filtro que aparecía en la página o referencia del profesor Misa. La mayor parte del trabajo fue revisar opciones, entender el circuito y ver cómo podíamos llevarlo a algo más claro.

---

## Qué es un filtro Sallen-Key

El filtro **Sallen-Key** es una configuración de filtro activo que usa un amplificador operacional junto con resistencias y capacitores.

Se usa mucho porque permite hacer filtros de segundo orden de forma relativamente simple. Puede servir para filtros paso bajo, paso alto o incluso otras variantes, dependiendo de cómo se acomoden los componentes.

La estructura general incluye:

- resistencias;
- capacitores;
- un amplificador operacional;
- una salida filtrada.

El operacional normalmente ayuda a aislar y estabilizar la señal, funcionando como buffer o etapa activa.

---

## Paso bajo y paso alto

La idea era lograr un filtro que pudiera cumplir ambas funciones:

| Tipo de filtro | Qué hace |
|---|---|
| Paso bajo | Deja pasar frecuencias bajas y atenúa frecuencias altas. |
| Paso alto | Deja pasar frecuencias altas y atenúa frecuencias bajas. |

En simple, el filtro paso bajo suaviza o corta lo más agudo, mientras que el paso alto elimina o reduce lo más grave.

Para nuestro proyecto, esto podía servir para modificar el sonido y controlar qué parte de la señal queríamos escuchar o procesar.

---

## Circuitos integrados revisados

Como estábamos trabajando con filtros activos, tuvimos que revisar qué amplificadores operacionales podían servir.

Los principales fueron:

| Integrado | Característica |
|---|---|
| `LM324` | Tiene cuatro amplificadores operacionales en un solo chip. |
| `LM358` | Tiene dos amplificadores operacionales, útil para pruebas más simples. |

El **LM324** puede convenir si queremos armar más de una etapa de filtro dentro del mismo integrado. Por ejemplo, una etapa paso bajo y otra paso alto.

El **LM358** puede servir para pruebas más pequeñas, ya que tiene menos operacionales, pero es más simple para comenzar.

---

## Por qué usamos operacionales

Los filtros pasivos usan solo resistencias y capacitores, pero tienen limitaciones. En cambio, un filtro activo usa un amplificador operacional para mejorar el comportamiento de la señal.

Algunas ventajas de usar un operacional son:

- ayuda a mantener la señal;
- permite hacer filtros más estables;
- puede evitar que una etapa afecte demasiado a otra;
- permite diseñar filtros de segundo orden;
- sirve para trabajar mejor con señales de audio o control.

---

## Filtro Sallen-Key paso bajo

El filtro Sallen-Key paso bajo deja pasar las frecuencias bajas y atenúa las altas.

En la referencia revisada, el circuito aparece como un filtro de segundo orden que se puede aplicar a distintos amplificadores operacionales. La frecuencia de corte depende principalmente de los valores de las resistencias y capacitores.

Una forma simplificada de entenderlo es:

```text
Frecuencias bajas → pasan
Frecuencias altas → se reducen
```

Esto puede servir para suavizar una señal o eliminar ruido agudo.

---

## Filtro Sallen-Key paso alto

El filtro Sallen-Key paso alto funciona de manera contraria al paso bajo. En este caso, se dejan pasar las frecuencias altas y se atenúan las bajas.

```text
Frecuencias bajas → se reducen
Frecuencias altas → pasan
```

Este tipo de filtro puede servir para quitar frecuencias graves o dejar pasar señales más rápidas.

---

## Problema de la clase

Aunque llegamos con información sobre Sallen-Key, no pudimos avanzar tanto en la exploración del circuito durante la clase.

El principal problema fue que todavía estábamos tratando de concretar el filtro de la página o referencia del profesor Misa. Antes de probar demasiadas variantes, necesitábamos entender bien ese diseño base.

Entonces la clase fue más de investigación y ajuste que de resultado final.

---

## Lo que intentábamos lograr

La idea general era tener una base de filtro activo que pudiera servirnos para:

- probar un filtro paso bajo;
- probar un filtro paso alto;
- usar LM324 o LM358;
- revisar valores de resistencias y capacitores;
- entender la frecuencia de corte;
- llevar el circuito a KiCad;
- acercarnos a un diseño que después pudiéramos montar o fabricar.

---

## Dudas que quedaron

- Qué integrado conviene más para nuestro filtro: `LM324` o `LM358`.
- Cómo adaptar correctamente el Sallen-Key a paso alto.
- Qué valores de resistencias y capacitores usar.
- Cómo calcular o ajustar la frecuencia de corte.
- Si conviene hacer ambos filtros separados o en una misma placa.
- Cómo adaptar bien el circuito del profesor Misa.

---

## Ideas importantes que me quedaron

- Sallen-Key es una configuración útil para filtros activos.
- Puede usarse para paso bajo o paso alto, dependiendo del diseño.
- El operacional es clave para estabilizar y manejar mejor la señal.
- El LM324 sirve si necesitamos varias etapas.
- El LM358 sirve para pruebas más simples.
- La frecuencia de corte depende de resistencias y capacitores.
- Antes de hacer la placa, hay que entender bien el esquemático.
- No pudimos avanzar tanto porque primero había que concretar el filtro base.

---

## Reflexión personal

Esta clase fue más lenta, pero sirvió para aterrizar mejor el problema. Al principio parecía que solo había que buscar un filtro paso alto y uno paso bajo, pero después quedó claro que había que entender bien cómo funcionaba la configuración Sallen-Key y cómo se adaptaba a nuestro circuito.

También me di cuenta de que elegir el integrado no es solo tomar cualquiera que diga “amplificador operacional”. Hay que pensar cuántas etapas necesitamos, cómo se alimenta el circuito y si el chip sirve para el rango de señal que queremos trabajar.

Aunque no avanzamos tanto en pruebas, la clase ayudó a ordenar mejor el camino: primero entender el filtro base, después definir los componentes y recién ahí llevarlo con más seguridad a KiCad.

---

## Conclusión

En esta clase seguimos investigando cómo construir un filtro activo usando Sallen-Key. La meta era acercarnos a un circuito que pudiera trabajar como paso alto y paso bajo, usando integrados como el LM324 o el LM358.

No logramos cerrar completamente el diseño, pero sí entendimos mejor que el filtro depende de varias decisiones: el tipo de operacional, la configuración del circuito, los valores de resistencias y capacitores, y la frecuencia de corte que queremos lograr.

El siguiente paso sería concretar el esquemático del filtro base, probar valores y decidir si conviene hacer el paso alto y paso bajo como circuitos separados o como partes de un mismo diseño.
