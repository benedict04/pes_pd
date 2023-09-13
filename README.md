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






  
