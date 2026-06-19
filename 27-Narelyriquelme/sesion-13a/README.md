# sesion-13a
## Clase 9, jun

En esta Clase nos enfocamos en el cierre de la etapa de diseño de circuitos en KiCad para pasar formalmente a la producción física y al planteamiento conceptual del Proyecto 03. Revisamos el flujo técnico para exportar los archivos de fabricación hacia JLCPCB y asegurar que las placas mandadas a hacer a China no tengan errores. Además, abrimos la discusión hacia el diseño de la interfaz y la carcasa del sintetizador, analizando referentes de cultura libre y organizamos los listados de materiales para los osciladores.

### Exportación de archivos Gerber desde KiCad a JLCPCB

* El diseño definitivo de las PCB se debe trabajar sobre la versión optimizada por el profesor, dejando atrás los borradores anteriores.
* El orden físico de la placa contempla cobre arriba y abajo con su respectiva máscara de color para el recubrimiento físico.
* La exportación exige un mínimo de 7 capas fundamentales que se procesan mediante la función Trazar o Plot.
* Es crítico cuidar de manera manual que los gráficos decorativos o logos no queden encima de las etiquetas técnicas de los componentes.
* Tras el trazado se deben generar los archivos de taladrado independientes para sumar un total de 8 archivos con extensiones .GRB y .GRL.
* El proceso se finaliza previsualizando todo en el Visor Gerber integrado de KiCad para verificar la coherencia geométrica antes de comprimir en un archivo único .ZIP.
* Las capas obligatorias son:

|| Capa | descripcion |
|--------|-----|--------|
| 1 | F.Cu | cobre frontal |
| 2 | B.Cu | cobre trasero |
| 3 y 4 | F.SilkS y B.SilkS | serigrafías y dibujos|
| 5 y 6 | F.Mask y B.Mask  |máscara de soldadura que opera en negativo |
| 7 | Edge.Cuts | contorno rígido de la placa |

### Planificación del Proyecto 03 e interfaz de usuario

* El nuevo encargo exige integrar los módulos del curso en un sintetizador definitivo protegido por un contenedor o carcasa libre.
* Cajas metálicas marca Hammond representan el estándar clásico de la industria para el encapsulado de pedales y módulos sonoros.
* El diseño industrial debe conceptualizar la interfaz de usuario basándose en cómo se relacionan los mandos con las personas.
* Para la adquisición económica de componentes en línea se recomendó la plataforma Vitronics.

### Lectura Yoko Ono : Pomelo

**Capítulo 1**
La lectura inicial se siente como una invitación a desconectarse de la realidad a través de dinámicas que juegan con la imaginación y la interacción social. Me llamó mucho la atención la Pieza de nieve, que propone una forma de aislamiento muy sutil al conversar con alguien: "Al hablar con una persona, pensar que la nieve está cayendo entre ambos. Dejar de conversar cuando se piensa que la persona está cubierta de nieve". También me impactó la intensidad psicológica de la Pieza de pieza I, la cual exige un aislamiento físico y mental absoluto al instruir: "Quedarse en una pieza una semana. No tomar nada excepto agua. Hacer que alguien le hable a uno al oído a fines de la semana". Estas propuestas desafían la lógica cotidiana y abren una dimensión íntima muy profunda.

**Capítulo 2**
En este capítulo las instrucciones se vuelven más crudas, caóticas y surrealistas, evocando una fuerte sensación de inestabilidad y pensamientos intrusivos. Un claro ejemplo de este absurdo poético es la Pieza de mina de lápiz, que juega con la mente y el entorno a través de la frase: "Imaginar que se tiene la cabeza llena de minas de lápiz. Imaginar que una de ellas se rompe. Mostrar una mina de lápiz al amigo y decirle que uno se la sacó de la cabeza". De igual manera, se presenta una fuerte crítica a las estructuras del tiempo y al control con la Pieza de reloj, cuyas líneas transmiten un desorden total: "Tomar todos los relojes de la ciudad. Poner cada uno en una hora arbitraria... siempre que ningún reloj sea puesto intencionalmente en la hora correcta". Es un recorrido irracional que te atrapa por su naturaleza visual y rebelde.
