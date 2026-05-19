# sesion-08a

Martes 28 de abril

###  ⟡ KiCad y diseño de PCB

### Conceptos generales

- Los **símbolos** representan los componentes de forma simplificada dentro del esquemático y permiten entender el funcionamiento lógico del circuito.
- Las **huellas** corresponden a la representación física de los componentes en la PCB, es decir, el espacio real que ocuparán en la placa.
- El **esquemático** funciona como un plano del circuito, mostrando cómo se conectan los componentes entre sí.
- La **PCB** es la placa física donde finalmente se montan y conectan todos los componentes electrónicos.
  
### Archivos principales de KiCad

KiCad trabaja con distintos archivos conectados entre sí mediante un archivo principal.

| Tipo de archivo | Función |
| --- | --- |
| `.kicad_pro` | Archivo principal del proyecto |
| `.kicad_sch` | Esquemático |
| `.kicad_pcb` | PCB |

---  

### Flujo para crear una PCB

#### 1. Crear esquemático
- Se dibuja el circuito lógico agregando componentes y conectándolos mediante cables.
#### 2. Asociar huellas
- Se relaciona cada símbolo con su representación física para la PCB.
#### 3. Abrir PCB Editor
- Se importa el circuito para comenzar a distribuir los componentes.
#### 4. Definir pistas
- Se seleccionan grosores según la corriente o necesidades eléctricas.
#### 5. Distribuir componentes
- Se organizan los elementos dentro de la placa.
#### 6. Rutear conexiones
- Se dibujan las pistas que unirán los componentes.
#### 7. Preparar fabricación
- Se agregan bordes, textos y detalles finales.

---

### Paso 1 

### ⟡ Esquemático

Dentro del  `.kicad_sch` se colocan componentes y se conectan usando cables.

A cada componente se le puede asignar:

- valor
- nombre
- identificador

Estos datos ayudan a identificar y entender mejor el circuito.

### Identificadores de componentes

Cada componente dentro del esquemático tiene un código para poder identificarlo fácilmente.

La letra indica el tipo de componente y el número sirve para diferenciarlo de otros iguales dentro del circuito.

### Detalles útiles

- Los potenciómetros aparecen dentro de la categoría de resistencias, por eso normalmente se encuentran como `R_pot`.
- Cuando un pin queda sin conectar de manera intencional se marca con una `X`, así el programa reconoce que no es un error.
- El término **pitch** se usa para hablar del espacio que existe entre un pin y otro.
- Los componentes se identifican mediante letras dentro del esquemático:
  
  - `R` → resistencia
  - `C` → condensador
  - `U` → circuito integrado

Por ejemplo:

- `R2` = segunda resistencia
- `C1` = primer condensador
- `U1` = primer circuito integrado
  
---

### Paso 2 

### ⟡ Asignar huellas

#### Diferencia principal

| Conceptual | Físico |
| --- | --- |
| Símbolo | Huella |

Las huellas se asignan desde **Assign Footprints**.

#### Tipos más comunes

| Tipo | Descripción |
| --- | --- |
| THT | Componentes que atraviesan la placa |
| SMD | Componentes montados sobre la superficie |

La elección depende del tamaño y características reales del componente.

---

### Huellas utilizadas

| Componente | Huella |
| --- | --- |
| Resistencia | `Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal` |
| LED | `LED_THT:LED_D5.0mm` |
| Potenciómetro | `Potentiometer_THT:Potentiometer_Alps_RK163_Single_Horizontal` |
| Condensador cerámico | `Capacitor_THT:C_Disc_D3.8mm_W2.6mm_P2.50mm` |
| Condensador electrolítico | `Capacitor_THT:CP_Radial_D5.0mm_P2.50mm` |

Para elegir correctamente las huellas es importante revisar:

- tamaño
- separación entre pines
- dimensiones físicas

Generalmente esa información aparece en el datasheet o en la página donde venden el componente.

---

### Paso 3 

### ⟡ PCB Editor

Al abrir el PCB Editor aparecen todos los componentes listos para distribuir.

Después se dibuja el borde de la PCB, ya que si no existe pueden aparecer errores. También es importante hacerlo en la capa correcta.

---

### Atajos útiles

| Acción | Atajo |
| --- | --- |
| Mover componente | `M` |
| Rotar | `R` |
| Reflejar en eje X | `X` |
| Mover grupo | `G` |
| Abrir propiedades | `E` |
| Activar cables | `W` |
| Copiar | `CTRL + C` |
| Pegar | `CTRL + V` |
| Cortar | `CTRL + X` |

---

### Trabajo en clases

En esa clase alcanzamos a trabajar hasta el paso 3 del proceso.

Hice los ejercicios de la clase junto a Benjamín, ya que no quedaban más computadores disponibles. Fuimos turnándonos durante la actividad, así que ambos pudimos experimentar y practicar las mismas cosas.

Al comienzo fue un poco confuso porque teníamos algunos errores en la configuración, por lo que no podíamos avanzar correctamente. Después, con ayuda, logramos corregirlos y continuar trabajando ദ്ദി( • ᴗ < )

#### Registro del proceso

![foto](./imagenes/esquematico.png)
![foto](./imagenes/foto1.png)
![foto](./imagenes/foto2.png)
![foto](./imagenes/foto3.png)
