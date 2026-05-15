# sesion-09a

12 de mayo

https://github.com/misaaaaaa/multiples-musicas

**pivotear en torno a productores, y a sellos matador records, quemasucabeza, warp rick rubin, gil norton, arca**

**REPASO KICAD**

comandos kicad=

*a= agregar simbolos*
*esc=hheramienta seleccion*
*m=mover coponente*
*v=valor componente*
*g=agarrar componente*
*ctrl + S= guardar*
e=editar revisar hoja de vida de componente
f=revisar huella asignada
cmd + d= duplicar componente 
alt + 3= visor 3d

para dibujar contorno de la placa, hacerlo en la capa *edge.cuts*
*tomas catrileo revisar su bitacora por diseño de placas*

usaremos 7 capas:
1 de contorno: Edge.Cuts
2 de cobre, adelante y atrás: F.Cu, B.Cu
2 de silkscreen
2 de mask


| Componente | Huella KiCad | Uso típico |
|---|---|---|
| Resistencia | `Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P7.62mm_Horizontal` | Resistencias through-hole |
| Potenciómetro horizontal | `Potentiometer_THT:Potentiometer_Alps_RK163_Single_Horizontal` | Potenciómetro de panel |
| Potenciómetro vertical | `Potentiometer_THT:Potentiometer_WH148_Vertical` | Potenciómetro típico de audio |
| Potenciómetro logarítmico | `Potentiometer_THT:Potentiometer_WH148_Vertical` | Control de volumen/audio |
| Capacitor cerámico | `Capacitor_THT:C_Disc_D5.0mm_W2.5mm_P5.00mm` | Capacitores no polarizados |
| Capacitor electrolítico pequeño | `Capacitor_THT:CP_Radial_D5.0mm_P2.50mm` | Capacitores polarizados |
| Capacitor electrolítico mediano | `Capacitor_THT:CP_Radial_D6.3mm_P2.50mm` | Capacitores polarizados grandes |
| LED 5 mm | `LED_THT:LED_D5.0mm` | LEDs estándar |
| Integrado DIP-8 | `Package_DIP:DIP-8_W7.62mm` | NE555, LM386, etc. |
| CD4017 | `Package_DIP:DIP-16_W7.62mm` | Contador decimal 4017 |
| Bornera 2 pines | `TerminalBlock:TerminalBlock_bornier-2_P5.08mm` | Conexión de parlante o alimentación |
| Header 2 pines | `Connector_PinHeader_2.54mm:PinHeader_1x02_P2.54mm_Vertical` | Conexiones simples |
| Header 1 pin | `Connector_PinHeader_2.54mm:PinHeader_1x01_P2.54mm_Vertical` | Entrada o señal individual |
| Header 4 pines | `Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical` | Salidas Step1-Step4 |
