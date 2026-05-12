# sesion-08b

12-05-2026

## Apuntes de clase

Después del repaso seguimos explorando ajustes más específicos sobre las huellas

(KiCad es un editor de texto que renderiza nuestras peticiones)

Con doble clic en los símbolos puedo asociar nombres y huellas, luego sería replicar este mismo símbolo para que se duplique con los valores agregados a este

El componente de origen puede ser igual, pero en términos de valores es distinta y con la “V” puedo cambiarle el nombre, pero con la “E” es más completo

Y pasamos al paso 3, donde nos quedamos en la semana pasada

Empezamos a diseñar como componentes físicos, pasamos del “mapa” a territorio

Siempre abrir el kicad PRO de “PROYECTO”

El botón “Verde” es cambiar al **editor de placas**

Tengo que traerme las partes del esquema a la placa 3D

Con el botón de “actualizar placa desde esquema”, al pasarlo me dice si pueden haber errores al importar

Al actualizar placa se traen las formas del mapa, con eso se traen las formas tridimensionales

Con Alt + 3 se ven flotando los materiales **render** en el espacio tridimensional

Queremos dibujar un contorno

En la grilla usamos la de 5000 mm

Se puede usar la herramienta de dibujar líneas

Para dibujar contornos de la placa tengo que estar en la capa Edge.Cuts (origen 50-50)

Pero con la herramienta rectángulo puedo tener los bordes redondos con doble clic

Usaremos 7 capas:

1 de contorno: Edge.Cuts
2 de cobre, adelante y atrás: F.Cu, B.Cu
2 de silkscreen
2 de mask

### Pistas en la tarjeta

Placa de fibra de vidrio y tiene una película de fibra de cobre donde se puede pasar una línea de cobre donde yo defina en las **pistas**

Vamos a setear los anchos de nuestras pistas

En las pistas, más de 0.3 mm es un buen mínimo

Colocamos 0.4 mm y 0.8 mm en las pistas

Se colocan los chips simétricamente con las líneas guía en User 1

Y colocamos los capacitores debajo de los chips

Luego la salida a la derecha de la placa

Los 9V de batería los colocamos arriba

Terminal block de 5 mm de espaciado

Luego colocamos el LED con criterio de LEDs hacia el mismo lado para fácil de soldar al anverso de la placa

1 resistencia al lado del LED **Esto más como decisiones de experiencia de usuario.**

Puedo poner en las capas las pistas en **F.Cu** o **B.Cu**, solo las dejamos visibles y nos aseguramos de que esté en F.Cu

Con la herramienta de “X” colocamos las pistas

Concepto de vía: pequeño cable que salta una pista si bloquea **con la letra V mientras se rutea la pista** (Aparece un punto en la esquina del cable) tienen 2 tamaños

La vía es como una dona, tiene 2 dimensiones, se puede ajustar en la sección de parámetros del KiCad

Si hacemos clic en una vía y aprieto la “E” puedo abrir más parámetros

Herramienta para que dibuje zonas rellenas para poder que todo el mundo en la placa sea Ground

Nombre de red es sinónimo de **cable**, luego puede no quedar perfecto, pero sí tiene que quedar dentro toda la placa y con la letra “B” hace el trabajo de rellenar la placa

El botón igual de la izquierda permite dejar de ver el relleno para ajuste visual personal: “Dibujar relleno de zonas”

Para colocarlo en la caja puedo usar hoyitos de montaje. En KiCad se llama MountingHole y el perno favorito del profe es M3

Las capas por excelencia para dibujar son las capas Silkscreen

Tener ojo en la capa del texto para que se vea bien

Por último se puede colocar un SVG o DXF de alguna imagen: Archivo > Importar > Gráficos. Puedo poner que esté en la capa Silkscreen o Back

Se puede al importar ajustar la opción de escalar para que quepa en la placa

Se puede definir el borde de la placa para que tenga forma y, si es posible, que tenga las conexiones

Encargo: de forma personal hacer 2 placas del sintetizador pasado
