# pes_pd

## QFN-48 

![image](https://github.com/benedict04/pes_pd/assets/109859485/07504a6e-13b3-47af-8c82-46640bf01c34)

- chip is in the centre of the package.
- chip is connected to package through wire balls for pin connections.
- chip consists of pads where signal is sent from outside to inside
- core consists of digital logic ie macros and Foundry IP's

## Introduction to openlane

![image](https://github.com/benedict04/pes_pd/assets/109859485/48e384d2-7d4d-41e4-9d23-dd5b4cf9ed27)

### Process Design Kit
- Interface between FAB and designers
- It has process design rules such as DRC, LVS and PEX

![image](https://github.com/benedict04/pes_pd/assets/109859485/41557eaf-1ddb-453f-810d-a64102cdc5cf)

## RTL to GDS flow

![image](https://github.com/benedict04/pes_pd/assets/109859485/92a7b36b-4364-42a1-9679-e9c3d0974ce2)

- synthesis : conert RTL to circuit out of the components from standard cell library
- Floor planning/ Power Planning : 1) Chip Floor-Planning partitions chip die between different system building blocks and place the input/output pads.
                                   2) Macro Floor-Planning is looking out for dimensions, pin locations and rows definitions.
                                   3) Power Planning is constructing power network. Power is supplied through metal straps.
- Placement : Place the cells on the floorplan row, alligned with sites
- Clocktree Synthesis : To deliver clock to all sequential elements. They deliver in minimum skew and a good shape.
- Routing - Implement interconnect using available metal layers. PDK defines width and space of metal layers.
            1) Global Routing : Generating routing guides
            2) Detailed routing : Uses Global routing guides to implement the actual wiring.
- signoff : physical verifications such as DRC and LVS. Timing verifications such as Static Timimg Analysis.

## OpenLane

![image](https://github.com/benedict04/pes_pd/assets/109859485/03906a7e-f942-42ab-9118-aeaafdae8d2e)

### Design 

![image](https://github.com/benedict04/pes_pd/assets/109859485/b53edcb9-1f5e-4475-ba99-50c93928ca09)

### synthesis

![image](https://github.com/benedict04/pes_pd/assets/109859485/e4dcfd8c-7d47-4560-a99e-e0fa14d57723)

### calculating flop ratio


## Utilization Factor and aspect ratio

![image](https://github.com/benedict04/pes_pd/assets/109859485/2f49a57a-8e52-4117-a213-f1f024b59ef5)

![image](https://github.com/benedict04/pes_pd/assets/109859485/30d0e337-f3e4-47b9-9824-079b152f7259)

## preplacemenet of cells

![image](https://github.com/benedict04/pes_pd/assets/109859485/73217a11-48a8-43d1-bebd-54e2402216a2)

- Ip's or blocks has user defined locations and hence are placed in chip before automated placement-and-routing and are called pre-placed cells.

## decoupling capacitors

- while switching from logic 1 to logic 0 charge in capacitor will be discharged current will be handled by Vss.
- During switching action decoupling capacitor will send current to the charges.

![image](https://github.com/benedict04/pes_pd/assets/109859485/2691d6a5-75c0-441e-a2a2-1431d2fc56bb)

![image](https://github.com/benedict04/pes_pd/assets/109859485/2c7130bb-22a9-4d54-900b-67f6dd3f540e)

## power planning

![image](https://github.com/benedict04/pes_pd/assets/109859485/4b3556dc-3815-4f48-aa4d-a2358d3fee42)

### after inserting an inverter

![image](https://github.com/benedict04/pes_pd/assets/109859485/82b71cdb-93ad-45aa-b730-47576ef5634b)

![image](https://github.com/benedict04/pes_pd/assets/109859485/96ce83d8-305d-44a2-8143-27887348a939)

- multiple power supplies solves the problem of ground bounce and voltage drop.

## pin placement

![image](https://github.com/benedict04/pes_pd/assets/109859485/5eb4efd5-190c-414b-9c66-57e038168828)


![image](https://github.com/benedict04/pes_pd/assets/109859485/705f5573-63d1-4227-90a1-1115b8660f34)

## LABS

### floorplanning

![image](https://github.com/benedict04/pes_pd/assets/109859485/ec319ba3-ff0c-457a-b6a4-51a917098e8e)

![image](https://github.com/benedict04/pes_pd/assets/109859485/c4bcfadc-24f1-499b-868e-80bcafbdfec4)

## Netlist biniding

![image](https://github.com/benedict04/pes_pd/assets/109859485/d0e9b8eb-f0cf-40a4-8b55-d2e7c690154b)

- Library determines width, height, delay and required conditions of logic .
- It also tells at what condition flipflop send input and emits output.
- size of cells determines parameter such as delay , resistance etc.

 ### optimization of placement

 ![image](https://github.com/benedict04/pes_pd/assets/109859485/fa115097-72be-450c-99e9-ad91571c4cec)

 - We use buffers also known as repeaters to maintain signal integrity.
 - Usually when distance from sender to receiver block is more on the basis of slew analysis buffers are used.

## LABS

### Placement

![rr  Running  - Oracle VM VirtualBox 14-09-2023 15_01_09](https://github.com/benedict04/pes_pd/assets/109859485/532095d2-23bd-4d35-b176-2b67507904a6)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 15_12_08](https://github.com/benedict04/pes_pd/assets/109859485/bc62e2d7-4f02-43b5-b402-b88761f9d6ce)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 15_14_26](https://github.com/benedict04/pes_pd/assets/109859485/ffc14c20-ea0e-4bc2-8eac-69b445c30f49)

