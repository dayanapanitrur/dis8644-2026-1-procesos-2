# sesion-08a
29 de abril 

# flujo de trabajo con kicad

## qué es Kicad?

KiCad es un software gratuito y de fuente abierta para diseño y fabricación de circuitos electrónicos. 

> Fuente: Montoya Moraga, A., & Serrano Acevedo, M. I. (2026). *Máquinas sonoras, electrónicas y computacionales: Estrategias y recetas*.

---

## flujo de trabajo paso a paso

1. **dibujar el esquemático**: se hace en `kicad_sch`
2. **asociar huellas a símbolos**
   - **huellas:** partes físicas de los componentes
   - **símbolos:** lo que se ve en el esquemático
3. **abrir PCB New**: para crear la PCB e interpretar el esquemático
4. **definir tamaño de las pistas**
5. **repartir componentes físicamente**
6. **rutear componentes**
7. **adornar y exportar para fabricación**

> quizás en algun momento tenga que crear mis propias huellas y símbolos ya que a veces no se encuentran en kicad

---

## atajos de teclado útiles

| tecla | acción |
|-------|--------|
| `A` | agrega un componente |
| `V` | dar valor al componente |
| `M` | mover componente |
| `R` | rotar componente |
| `X` | reflejar a lo largo del eje X (de abajo para arriba) |
| `W` | modo cable |
| `E` | propiedades (se puede cambiar la referencia) |
| `G` | agarrar el componente |

> también se puede hacer click en el valor para alejarlo del componente

### prefijos de componentes

| prefijo | componente |
|---------|------------|
| `R` | resistencia |
| `R_POT` | potenciómetro |
| `U` | circuito integrado |
| `LS` | parlante |


---
![imagenes](./imagenes/miprimerkicad.jpeg)
## recursos y referencias

- **wintwe bloom**: empresa que cerró, hacían sintes con kicad y eran muy estéticos. aprendieron a programar con google. útil para ver cómo cambiar los temas dentro de kicad.
- **the codes**: recursos y tutoriales
- **tht true holes**: componentes through-hole
- **victronics**: referencia de componentes 
