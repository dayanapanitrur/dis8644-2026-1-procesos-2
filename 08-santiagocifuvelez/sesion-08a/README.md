# sesion-08a
28 de abril del 2026

![ctrl + s](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/gif1.gif)

¡Hola profe Aaron, Misa y Emi!, espero que se encuentren bien el día en el que estén leyendo estos textos de la bitácora. (esta es la clase antes de salir al break del semestre jiji).

El día de hoy vimos KICADDDD:  
1.	Dibujar esquemático (Kicad_sch).  
2.	Asociar huellas a símbolos.  
3.	PCB new; un preview de como se verían esos componentes en el mundo real. Tangible y funcional.

Comencemos c: 

## 1.	Dibujar esquemático (Kicad_sch).  

1: Para comenzar nuestro recorrido por Kicad, debemos abrir primeramente la extensión de Kicad pro:  
![Folder donde están todas las carpetas](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img1.jpeg)

2: En archivo, crea un nuevo proyecto, guárdalo donde lo tengas bien organizado y listo.

3: Luego se abre esta superficie (pero limpia) y ya puedes comenzar a trabajar;
![img2](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img2.png)

4:	Comandos:   
•	`A = Se abre la tabla de símbolos donde puedes encontrarlos todos.`

5:	Encontrar símbolos:  
•	`R = Resistors`  
•	`C = Unpolarized capacitor`  
•	`C_p = Polarized capacitor`   
•	`Gnd = Ground (tierra)`  
•	`Vcc = Voltaje corriente continuo (Cielo)`  
•	`NE555P = Chip 555`  
•	`R_pot = Potenciómetro`  
•	`Led = Led`  
•	`Battery_cell = Batería`   
•	`Speaker = parlante`  

6:	Una vez ya armado nuestro esquema, sigue asignarle huellas:
Hay dos maneras, pero la que yo uso es la siguiente:
![img3](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img3.png)

## 2.	Asociar huellas a símbolos.  
Vamos allí, y luego se nos abre esta ventana, en la cual asignaremos las huellas a nuestro circuito para que pueda ser traspasado al mundo real y tangible:   
![img4](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img4.png)

Para esto, debemos saber las medidas de los componentes que vamos a usar, y para saber esas medidas, podemos buscar en paginas como: www.victronics.cl   
Una vez ya asignados todos los componentes; 
![img5](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img5.png)

dejamos el de la batería y el del parlante sin asignar huella, porque usualmente esas son cosas “externas”, so, ponemos un “Terminal block” (le puse el terminal al parlante luego)

![img6](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img6.png)

7:	Luego, vamos a la PCB, que será nuestra placa tangible:
![img7](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img7.png)


## 3.	PCB new; un preview de como se verían esos componentes en el mundo real. Tangible y funcional.
Y se nos abrirá este panel:  
![img8](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img8.png)

Luego le hundimos este botón para traer nuestro esquemático a la placa o actualizarlo:
![img9](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img9.png)

Nos aseguramos que no hayan errores y las configuraciones estén así (O solo “F8”):
![img10](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img10.png)

![img11](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img11.png)

8:	Luego de tener nuestra placa importada, si queremos realizar algún tipo de base o superficie que sostenga los componentes, siempre se debe hacer en la capa de “edge.cuts”.  
![img12](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img12.png)

9.	Y así se previsualizaría:
![img13](https://github.com/santiagocifuvelez/dis8644-2026-1-procesos-2/blob/main/08-santiagocifuvelez/sesion-08a/imagenes/img13.jpg)

Fin.
No olvides siempre "Ctrl + s" or "Comand + s"..., Todo el tiempo.  
Bisous!
