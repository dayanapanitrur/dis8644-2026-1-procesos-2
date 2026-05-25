# sesion-09b

viernes 15 de mayo

## clase

COMPONENTE (especie) R / VALOR (10k) / HUELLA (dibujito)

edita el campo de huella: el DIP-8 de 7.62mm es el más común

no se cambia automático, hay que actualizarlo, ir al diseño de placa e ir a "actualizar placa desde esquema" y se actualiza la huella

### cómo cambiar la posición de las patitas en el sch

- editar símbolos en biblioteca de símbolos, hay que hacer un tipo fork
- NO editar símbolo de biblioteca, sino que solo editar símbolo
- se puede editar gráficamente, usando la E para editar color y relleno
- símbolos y huellas son bibliotecas! (no editar los originales o muere)
- propiedades de pin, para editar los pines (patitas) también se puede seleccionar el pin y con M mover

si arriba sale un asterisco es porque no está guardado!

en el archivo editor de símbolos nos permite crear nuestra propia biblioteca, hay que crear un lugar donde se guarden (kicad_sym) en archivo < nueva biblioteca

buscamos el símbolo en otra biblioteca que querramos usar, lo copiamos y lo pegamos en nuestra biblioteca

### botones

temporales y de tipo switch, la diferencia de prender la luz y tocar el timbre

- push button (pulsador): es temporal porque el circuito se cierra (deja pasar corriente) solo mientras lo mantenemos resionando, tiene un resorte interno que lo devuelve a su lugar al soltarlo.
- switch (interruptor): al presionarlo el mecanismo interno se traba y el circuito se queda cerrado y hay que volver a accionarlo para abrir el circuito.

![push button y switch](imagenes/botones.png)



