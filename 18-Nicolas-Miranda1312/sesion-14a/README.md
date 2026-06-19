# sesion-14a

09-06-2026

## Exportación de la PCB en formato Gerber

Para fabricar nuestra placa PCB, primero debemos exportarla en formato **Gerber**.

En este caso, es necesario exportar como mínimo las siguientes **7 capas**:

- 2 capas de cobre (Copper)
- 2 capas de serigrafía (Silkscreen)
- 2 capas de máscara de soldadura (Solder Mask)
- 1 capa de contorno de la placa (Board Outline)

Para realizar la exportación, se debe presionar el botón **Plot**, ubicado en la parte superior izquierda de KiCad.

En la ventana que aparece, se seleccionan las capas que se desean exportar y se define la carpeta donde se guardarán los archivos.

Luego se deben realizar dos acciones importantes:

1. Presionar **Plot** para generar los archivos Gerber.
2. Presionar **Generate Drill Files** para generar los archivos de perforación.

Al finalizar, se crearán varios archivos correspondientes a cada una de las capas y perforaciones de la PCB.

Es recomendable revisar el resultado utilizando el **Gerber Viewer**, ya que permite verificar que todas las capas sean coherentes y que no existan errores en el diseño. También es importante comprobar que la serigrafía no cubra los nombres o referencias de los componentes, ya que esto puede dificultar el ensamblaje de la placa.

Una vez revisados los archivos, se deben comprimir en un archivo **.zip** para enviarlos al fabricante.

---

## Cotización y revisión en JLCPCB

Posteriormente, ingresamos a JLCPCB y subimos el archivo comprimido con los Gerber.

La ventana de cotización no solo indica el precio de fabricación, sino que también funciona como una primera verificación para confirmar que los archivos fueron exportados correctamente.

Además, se puede utilizar la opción **Gerber Viewer** para inspeccionar las distintas capas y visualizar la placa en 3D. Esto permite comprobar aspectos importantes como:

- Dimensiones correctas de la PCB.
- Posición de los componentes y perforaciones.
- Apariencia general del diseño.

Finalmente, se selecciona:

- La cantidad de placas a fabricar.
- El color de la máscara de soldadura.
- El acabado superficial.

El acabado **HASL** es el estándar utilizado por la mayoría de los fabricantes. Está disponible en versiones con plomo y sin plomo; generalmente se recomienda la opción **sin plomo**, ya que es más segura para la salud y cumple con las normativas ambientales actuales.
