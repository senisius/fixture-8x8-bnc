# Fixture 8x8 DIP-16 a BNC: paquetes de fabricación para JLCPCB

Placa de ensayo para un dispositivo de matriz 8x8 en encapsulado DIP-16. El dispositivo va en un zócalo DIP-16 de 0,3" en el centro de la placa. Cada uno de sus 16 pines va al vivo de un BNC hembra acodado, con 4 conectores en cada lado de la placa. Las carcasas de los BNC van al plano de GND.

- Placa de 100 × 100 mm y 2 capas, con plano de GND.
- 4 agujeros de montaje M3 (3,2 mm) en las esquinas.
- 16 BNC (J1–J16) y un zócalo DIP-16 (U1).

## Variantes

| Carpeta | Huella de los BNC | Uso |
|---|---|---|
| [`Fixture_8x8_BNC/`](Fixture_8x8_BNC/) | BNC acodado: pin central y 4 patas en un cuadrado de 8,1 mm, taladros de 1,5 mm | Solo BNC |
| [`Fixture_8x8_Dual/`](Fixture_8x8_Dual/) | Huella doble BNC / triaxial (Trompeter/Cinch CBBJR79): ranura central común, pad de guarda a GND y patas para los dos conectores | BNC o triaxial |

Cada carpeta contiene:

| Fichero | Para qué |
|---|---|
| `Fixture_8x8_*_JLCPCB_Gerbers.zip` | Gerber (cobre, máscara, serigrafía, contorno) y taladros, para subir a JLCPCB |
| `BOM_Fixture_8x8_*.csv` | Lista de piezas con referencias LCSC |
| `CPL_Fixture_8x8_*.csv` | Posición y giro de cada pieza (formato JLCPCB, cara superior) |

## Piezas (BOM)

| Ref. | Pieza | LCSC | Cant. |
|---|---|---|---|
| J1–J16 | dosinconn `DOSIN-801-0078`: BNC hembra acodado, 50 Ω, rosca de panel M12 | `C709676` | 16 |
| U1 | Zócalo DIP-16 0,3" (7,62 mm), BOOMELE `IC-16PNarrow` | `C2326` | 1 |

El diseño original usaba el cntitle `BNC-KWE-6` (`C20415789`), que se quedó sin stock en JLCPCB (noviembre de 2026). El `DOSIN-801-0078` encaja en la misma huella. Tiene el pin central y 4 patas en un cuadrado de 8,0 mm (8,1 mm en el original), con patas de Ø1,1–1,2 mm en taladros de 1,5 mm. El cuerpo mide 33,9 mm (34 mm el original) y el eje queda a 7 mm de la placa.

## Antes de pedir

- Comprobar el stock de `C709676` y `C2326` en el momento del pedido.
- Revisar en la vista previa de JLCPCB que los BNC salgan hacia fuera del borde, y el pin 1 del zócalo.

Los ficheros fuente de Altium (`.PcbDoc`, `.SchDoc`, `.PrjPcb`) y los scripts que generaron la placa no se publican, porque incrustan rutas locales del equipo.
