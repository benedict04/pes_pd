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

# DAY 2

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

# DAY 3

## cell design flow

![image](https://github.com/benedict04/pes_pd/assets/109859485/d4782a48-dabc-4c21-8c39-c5f2b8ca84e1)

![image](https://github.com/benedict04/pes_pd/assets/109859485/361de1f0-68a4-4a83-81e2-aaf120ae127f)

## General timing characterisation

![image](https://github.com/benedict04/pes_pd/assets/109859485/35685071-34b2-4886-a23f-8dc55988de23)

![image](https://github.com/benedict04/pes_pd/assets/109859485/469510da-98d4-465e-8750-505b4b7ccff9)


## Spice Simulation

![image](https://github.com/benedict04/pes_pd/assets/109859485/f647353c-6bf5-4c2b-ac47-5dadead42915)

![image](https://github.com/benedict04/pes_pd/assets/109859485/cd25ef57-20b1-40e1-be2c-12aec347e43a)

![image](https://github.com/benedict04/pes_pd/assets/109859485/98c4bef9-2417-4229-a392-a7a33d463ce4)


## Labs 

![image](https://github.com/benedict04/pes_pd/assets/109859485/3633ab62-b42e-44d2-b8be-9bd1503583d8)

### 16 Mask CMOS Fabrication
The 16-mask CMOS process consists of the following steps:
1. Selection of subtrate: Secting the body/substrate material
2. Creating active region for transistors: Isolation between active region pockets by SiO2 and Si3N4 deposition followed by photolithography and etching
3. N-well and P-well formation: Ion implanation by Boron for P-well and by Phosphorous for N-well formation
4. Formation of gate terminal: NMOS and PMOS gates formed by photolithography techniques
5. LDD (lightly doped drain) formation: LDD formed to prevent hot electron effect
6. Source & drain formation: Screen oxide added to avoid channelling during implants followed by Aresenic implantation and annealing
7. Local interconnect formation: Removal of screen oxide by HF etching. Deposition of Ti for low resistant contacts
8. Higher level metal formation: CMP for planarization followed by TiN and Tungsten deposition. Top SiN layer for chip protection

## Labs to create standard cell design

![rr  Running  - Oracle VM VirtualBox 14-09-2023 16_40_45](https://github.com/benedict04/pes_pd/assets/109859485/409a97d2-8075-4348-9f9a-9b3f45cafaad)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 17_12_11](https://github.com/benedict04/pes_pd/assets/109859485/3e1cc8aa-4b31-4857-972d-4c70d768dd8c)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 17_21_17](https://github.com/benedict04/pes_pd/assets/109859485/ae60757e-3a11-4066-91f3-9c4243ac0185)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 17_21_55](https://github.com/benedict04/pes_pd/assets/109859485/c9e2157f-510a-493f-a403-cffa0bc9a96c)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 17_35_03](https://github.com/benedict04/pes_pd/assets/109859485/6bf7379d-9c69-407e-96da-cf15d5bb4644)

![rr  Running  - Oracle VM VirtualBox 14-09-2023 17_45_27](https://github.com/benedict04/pes_pd/assets/109859485/c41199a6-4cee-40b2-96fa-0e50c53e9fdd)

### Introduction to Magic Options and DRC rules
**Magic**
+ Magic is a venerable VLSI layout tool, written in the 1980's at Berkeley by John Ousterhout, now famous primarily for writing the scripting interpreter language Tcl. 
+ Due largely in part to its liberal Berkeley open-source license, magic has remained popular with universities and small companies.
+ The open-source license has allowed VLSI engineers with a bent toward programming to implement clever ideas and help magic stay abreast of fabrication technology.
+ However, it is the well thought-out core algorithms which lend to magic the greatest part of its popularity.
+ Magic is widely cited as being the easiest tool to use for circuit layout, even for people who ultimately rely on commercial tools for their product design flow.

**DRC rules**
+ DRC (Design Rule Check) rules are a set of guidelines and constraints used in the field of semiconductor and integrated circuit (IC) design to ensure that the physical layout of a chip or circuit adheres to the manufacturing process's design rules.
+ These rules are essential for maintaining manufacturability and ensuring that the final ICs can be fabricated without defects.
+ The design rules used by Magic's design rule checker come entirely from the technology file.

  # DAY 4

  ## LABS

### convert std magic layout to std lef

![image](https://github.com/benedict04/pes_pd/assets/109859485/a2fd981b-e7c4-4107-b488-5a97a8495299)

#### Setting grid values using above file info

![image](https://github.com/benedict04/pes_pd/assets/109859485/ed980681-806f-4131-871e-3407832445ee)

#### Layout view after setting grid info

![image](https://github.com/benedict04/pes_pd/assets/109859485/324f69b3-9d65-479c-9f3d-4c53fc49f3c5)

## LEF Generation

![image](https://github.com/benedict04/pes_pd/assets/109859485/8b4d77c0-af39-4226-807b-edce960a3bf0)

![image](https://github.com/benedict04/pes_pd/assets/109859485/67c7a953-af33-43f7-a9f1-5f961757725e)

### Generated lef file

![image](https://github.com/benedict04/pes_pd/assets/109859485/76b956aa-103e-486b-9afe-8c7f886a612d)

```
cp sky130_vsdinv.lef /home/vsduser/Desktop/work/tools/openlane_working_dir/designs/picorv32a/src/
cp sky130_fd_sc_hd__* /home/vsduser/Desktop/work/tools/openlane_working_dir/designs/picorv32a/src/
config.tcl
```

#### Steps to execute

- design run
- synthesis

  ![image](https://github.com/benedict04/pes_pd/assets/109859485/b715b9bf-d249-4ef5-9871-2e127bd8706d)

 ![image](https://github.com/benedict04/pes_pd/assets/109859485/f0f2b79b-ba59-47b0-b9d2-45054766710b)

#### enable buffer sizing 

![image](https://github.com/benedict04/pes_pd/assets/109859485/815df172-7084-4bb7-9553-8f31a6c4b3d0)

#### now run synthesis again

### invoking magic to check layout


