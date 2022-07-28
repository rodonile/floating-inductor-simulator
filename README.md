# floating-inductor-simulator
PCB design (KiCAD) of a floating inductor simulator circuit, based on the [Grueningen Synthetic Inductor Circuit](https://ieeexplore.ieee.org/document/1457733). The inductance can be changed via the trim potentiometer (RV1). The circuit with the selected components can be used to simulate inductors from 20mH to ~8H. 

Formula for determining the inductance value of the circuit:

        L = R2^2 * RV1 * C4 / R7,   given R2 = R3 = R4

The desired value range of the inductance can be tweaked by changing the resistors/caps/pots values. For example, with the values on the schematic below and with a 10kOhm RV1 trim potentiometer we are able to simulate inductances ranging from 20mH to 7.7H. 

The frequency operation range of the circuit spans from ~100Hz to ~10kHz. For signals near and outside this range the circuits starts being unstable.

The RV2 potentiometer is a series resistor that can be used to adjust the Q-factor of the circuit but has no influence on the inductance value.

## Schematics
![Alt text](./images/schematics.svg)

## Layout and 3D view

<img src="./images/layout.png" width="400" />

3D view TOP                |  3D view BOTTOM
:-------------------------:|:-------------------------:
![](./images/3d_top.png)  |  ![](./images/3d_bottom.png)

## Bill of materials (BOM)
![Alt text](./images/bom.png)

The bill of material is also available in the [ibom.html](ibom.html) file (interactive html format, to be opened with a web browser). The components I used to build the circuit are available as a [csv file](components-digikey.csv) (they were ordered from Digikey).

## Gerbers
Gerber files are available in [releases](https://github.com/rodonile/floating-inductor-simulator/releases). The board is a 4-layer PCB. Designed with JSCPCB design rules. 