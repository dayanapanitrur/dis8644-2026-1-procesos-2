# sesion-09a

# Bitácora — Primer acercamiento a KiCad y diseño PCB

Durante este primer encargo utilizando KiCad, comenzamos explorando las herramientas básicas para la creación de esquemáticos y placas PCB. Al inicio fue complejo comprender la relación entre los símbolos electrónicos y las huellas físicas, pero poco a poco se logró entender cómo funciona el flujo de trabajo dentro del programa.

Primero realizamos los esquemáticos utilizando distintos componentes electrónicos como switches, capacitores, baterías y speakers. Luego aprendimos a asignar footprints o huellas a cada componente para poder llevarlos posteriormente a la PCB. En esta etapa aparecieron varios errores debido a componentes sin huellas asignadas o conexiones incorrectas entre elementos.

Uno de los aprendizajes más interesantes fue la visualización 3D de la placa. Descubrimos que presionando:

```txt
Alt + 3
````

es posible renderizar la PCB y observar cómo se vería físicamente el proyecto terminado. Esta herramienta ayudó bastante a entender la distribución real de los componentes y detectar errores de espacio o posiciones incorrectas.

También aprendimos a crear los bordes de la placa utilizando la capa:

```txt
Edge.Cuts
```

En esta sección se dibuja manualmente la forma de la PCB mediante líneas. Comprendimos que si el borde no está completamente cerrado, KiCad genera errores al momento de visualizar o exportar el diseño final.

Otro aspecto importante fue aprender a agregar componentes externos y modelos 3D descargados desde internet. En varias ocasiones algunos componentes no existían en las librerías predeterminadas de KiCad, por lo que fue necesario buscar archivos y librerías adicionales en GitHub y otras páginas. Luego estos archivos debían vincularse manualmente a los componentes para que aparecieran correctamente tanto en la PCB como en el render 3D.

Durante el desarrollo aparecieron distintos errores técnicos, especialmente relacionados con:

* componentes sin footprint,
* conexiones mal realizadas,
* pistas cruzadas,
* errores ERC y DRC,
* y problemas al actualizar la PCB desde el esquemático.

Muchos de estos problemas ocurrieron por errores pequeños dentro del esquemático o por no comprender completamente el funcionamiento de ciertas herramientas. Aun así, investigar tutoriales y documentación en internet ayudó bastante a complementar la información vista en clases y permitió avanzar con mayor seguridad.

Este primer acercamiento a KiCad permitió comprender de manera más práctica cómo se desarrolla una placa electrónica desde el esquemático inicial hasta su representación física en PCB y en render 3D. A pesar de las dificultades y errores durante el proceso, la experiencia ayudó a entender mejor tanto las capacidades del software como la lógica detrás del diseño electrónico.

<img width="1052" height="723" alt="esquematicoyerrores" src="https://github.com/user-attachments/assets/38b81455-ea6c-43e1-893a-b7b63561e343" /> 

# Bitácora — Corrección de errores y comprensión del esquemático en KiCad

Después de revisar nuevamente las clases y analizar varias veces el funcionamiento del circuito, logré comprender mejor cómo se conectan los componentes dentro del esquemático y cómo estos se relacionan posteriormente con la PCB. Esto ayudó bastante a corregir distintos errores que aparecían constantemente durante el desarrollo del proyecto. En esta etapa trabajé principalmente con un circuito basado en un temporizador 555 conectado a distintos switches, resistencias, capacitores, una batería y un speaker. A medida que avanzaba, aparecieron varios errores tanto visuales como eléctricos dentro de KiCad. Uno de los errores más frecuentes fue la mala conexión entre componentes. En varias ocasiones los cables parecían conectados visualmente, pero realmente no estaban unidos eléctricamente, lo que provocaba errores ERC dentro del programa. También ocurrió que algunos componentes estaban conectados a tierra o alimentación de manera incorrecta, especialmente en las líneas de VCC y GND.

Otro problema importante fue la utilización incorrecta de los `POWER_FLAG`. Al inicio no entendía bien para qué servían, por lo que KiCad detectaba errores indicando que ciertas líneas de alimentación no tenían una fuente de energía válida. Después de investigar y revisar las clases nuevamente, comprendí que los `POWER_FLAG` ayudan al programa a reconocer que una línea realmente está energizada y así eliminar advertencias falsas relacionadas con alimentación.

También aparecieron errores relacionados con componentes sin huella asignada o footprints incompatibles. Algunos switches y el speaker no tenían footprints correctos, por lo que no aparecían correctamente en la PCB o en el render 3D. Esto obligó a buscar nuevas librerías y asignar manualmente footprints más adecuados para cada componente.

En el caso del speaker, fue necesario revisar el tipo de conexión y verificar la polaridad junto al capacitor electrolítico conectado a la salida del 555. Al principio algunos componentes estaban invertidos o mal orientados, lo que generaba errores de conexión y visualización.

<img width="839" height="476" alt="errores01" src="https://github.com/user-attachments/assets/a10db200-3e57-40a1-a77f-13889afd4ef9" />

<img width="839" height="476" alt="pcb01" src="https://github.com/user-attachments/assets/5e41a205-b2f0-4730-a008-6e2817ea1aa2" />

En esta etapa del proyecto el trabajo se enfocó principalmente en mejorar la distribución de los componentes dentro de la PCB para optimizar el espacio y facilitar el ruteo de las conexiones. A medida que avanzaba el diseño, fue necesario reorganizar varias veces resistencias, capacitores y el circuito integrado para evitar cruces innecesarios y mantener un orden más claro dentro de la placa.

También se comprendió mejor cómo la posición física de cada componente afecta tanto la fabricación como el uso real del circuito. Elementos como el potenciómetro necesitaron una ubicación más estratégica debido a su tamaño y forma de manipulación.

Durante este proceso aparecieron algunos errores DRC relacionados con distancias mínimas y cercanía entre pistas, lo que obligó a realizar pequeños ajustes en la distribución general. Gracias a esto fue posible entender de mejor manera la importancia de equilibrar funcionalidad, espacio y organización dentro del diseño PCB.

Esta etapa ayudó a desarrollar una comprensión más práctica sobre cómo planificar una placa electrónica considerando no solo el circuito, sino también sus limitaciones físicas y de fabricación.

<img width="828" height="594" alt="placa01" src="https://github.com/user-attachments/assets/3248a4aa-f8c7-4906-8bcb-caed846914a2" />

<img width="828" height="594" alt="placa02" src="https://github.com/user-attachments/assets/e89781f7-4954-435b-8a8b-1eee20844c70" />

# Bitácora — Visualización 3D y estado de la PCB

En esta etapa del proyecto fue posible visualizar la PCB de manera mucho más cercana a cómo se vería físicamente una vez fabricada. Utilizando el render 3D de KiCad, se puede observar con mayor claridad la distribución final de los componentes sobre la placa, incluyendo las resistencias alineadas en la parte superior izquierda, los capacitores ubicados debajo y el circuito integrado en el centro del diseño. También destaca el componente más grande ubicado al lado derecho, correspondiente al potenciómetro, el cual ocupa gran parte del espacio disponible dentro de la PCB.

La visualización 3D ayudó bastante a entender proporciones reales y detectar detalles que no eran tan evidentes en la vista tradicional de PCB. Por ejemplo, permitió revisar mejor las distancias entre componentes y notar cómo ciertos elementos podían quedar demasiado juntos al momento de fabricar la placa físicamente.

Aunque la organización general ya se encuentra bastante más clara y ordenada, todavía falta completar gran parte del proceso de unión entre componentes mediante pistas. Esta etapa ha sido una de las más difíciles hasta ahora, ya que requiere bastante paciencia para encontrar rutas limpias sin generar cruces o errores de conexión. En varias ocasiones fue necesario reiniciar parte del trabajo porque algunas rutas quedaban demasiado desordenadas o interferían con otros componentes.

<img width="1155" height="771" alt="pruebadehuellas" src="https://github.com/user-attachments/assets/f6c1a107-e152-45d5-9356-57a6aad5ad4a" />

<img width="1155" height="771" alt="pruebadedist" src="https://github.com/user-attachments/assets/18df6f1a-5a69-47ac-9635-136403204315" />

Además, una dificultad importante durante el desarrollo ha sido el rendimiento del computador. Mientras se trabaja en KiCad, especialmente utilizando herramientas 3D o realizando múltiples cambios en la PCB, el programa a veces se cierra inesperadamente. Esto ha complicado bastante el avance del proyecto, porque en ocasiones se pierde parte del progreso realizado y es necesario volver a acomodar componentes o rehacer conexiones.

Aun así, este proceso ha permitido comprender mucho mejor cómo se construye una placa electrónica real y cómo pequeños cambios en la distribución pueden afectar directamente la facilidad del ruteo y el orden general del diseño. Poco a poco el trabajo dentro de KiCad se ha vuelto más intuitivo, especialmente al entender mejor la relación entre la organización visual y el funcionamiento práctico de la PCB.

<img width="448" height="634" alt="listadeopciones" src="https://github.com/user-attachments/assets/709bd46a-de6c-4aa4-b898-35423fd5563e" />

Otro aspecto que complicó bastante el desarrollo fue la búsqueda de componentes y footprints compatibles dentro de KiCad. En varias ocasiones algunos componentes simplemente no aparecían en las librerías predeterminadas del programa, por lo que fue necesario buscar alternativas en internet o revisar recursos compartidos en el Discord del curso. Muchas veces también hubo que descargar huellas externas y configurarlas manualmente para que funcionaran correctamente dentro del proyecto. Este proceso alargó considerablemente el tiempo de trabajo, pero también permitió entender la importancia de planificar bien las librerías y compatibilidades desde el inicio, algo que será muy importante considerar en futuros proyectos electrónicos.

<img width="448" height="634" alt="huellas" src="https://github.com/user-attachments/assets/18561a2d-5723-48bb-8bdf-c2f7a520cb40" />

- HUELLAS.

- # Análisis y Reflexión de los Capítulo 1 — Filosofía de la Fotografía

El capítulo 1 habla sobre la importancia que tienen las imágenes en la vida humana y cómo estas han sido una herramienta para entender el mundo desde hace muchísimo tiempo. El autor explica que las imágenes no son solamente algo decorativo o artístico, sino que también ayudan a las personas a interpretar la realidad, recordar momentos y transmitir ideas o emociones. Antes incluso de la escritura, las personas ya utilizaban dibujos y símbolos para comunicarse y darle sentido a lo que veían a su alrededor. Por eso, las imágenes siempre han estado muy ligadas a la forma en que pensamos y entendemos las cosas.

Algo interesante del capítulo es la comparación que hace entre las imágenes y los textos. Las imágenes permiten entender algo de manera rápida y emocional; muchas veces una sola fotografía puede transmitir sentimientos o situaciones sin necesidad de palabras. En cambio, los textos requieren un proceso más lento, porque hay que leer, analizar y seguir  un orden. El autor no dice que uno sea mejor que el otro, sino que funcionan de maneras distintas y se complementan. Gracias a esto, uno puede darse cuenta de cómo hoy en día estamos rodeados constantemente de imágenes: redes sociales, publicidad, televisión, fotografías y pantallas en general.También se hace una crítica a cómo las imágenes pueden influir demasiado en nuestra forma de ver la realidad. Muchas veces creemos que lo que vemos en una foto o en una pantalla representa completamente la verdad, cuando en realidad sigue siendo solo una representación. Esto pasa mucho actualmente con las redes sociales, donde las personas muestran versiones editadas o seleccionadas de sus vidas. El capítulo invita a pensar de manera más crítica sobre las imágenes y entender que no solo muestran la realidad, sino que también pueden cambiar la forma en que la percibimos.
