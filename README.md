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

![image](https://github.com/benedict04/pes_pd/assets/109859485/c21f5eaa-a81b-4567-97ed-9ee18b9d6156)

# DAY 5
# Final steps for RTL2GDS using tritonRoute and openSTA
## Routing and design rule check (DRC)
### Maze routing
Maze routing is a technique used in electronic design to efficiently connect components on a chip's layout. Lee's algorithm, also known as Lee's BFS algorithm, is a popular method for finding the shortest path in a grid-based maze by exploring it layer by layer.

### DRC
- DRC stands for "Design Rule Checking." It is a crucial step in the integrated circuit (IC) design and electronic design automation (EDA) process. DRC involves verifying that the layout of a semiconductor device or IC adheres to the specified design rules and constraints.

- These design rules are a set of guidelines and constraints defined by semiconductor manufacturers and design teams to ensure the proper functioning of the chip and its manufacturability. DRC checks for violations of these rules, which can include criteria related to minimum feature size, spacing between components, wire widths, and other physical and electrical properties.

- By performing DRC, designers can identify and rectify potential issues early in the design process, helping to prevent costly errors and ensuring that the final IC design meets the required specifications and can be successfully manufactured.

## Power Distribution Network and routing
### Power Distribution Network
Once we've created our clock tree network and confirmed the successful post-routing STA checks, the next step is to proceed with generating the power distribution network.

`gen_pdn` in OpenLANE:

![image](https://github.com/benedict04/pes_pd/assets/109859485/bf4239cf-ad38-458a-925b-1192002dc837)

![image](https://github.com/benedict04/pes_pd/assets/109859485/227fd916-0de5-40d0-b731-06b809926b82)

+ The PDN feature within OpenLANE will create:
   - Power ring global to the entire core
   - Power halo local to any preplaced cells
   - Power straps to bring power into the center of the chip
   - Power rails for the standard cells
+ We see that there is a change in the DEF.

### Global and Detailed Routing 
+ OpenLANE uses TritonRoute as the routing engine for physical implementations of designs. Routing consists of two stages:
   - Global Routing - Routing guides are generated for interconnects on our netlist defining what layers, and where on the chip each of the nets will be reputed.
   - Detailed Routing - Metal traces are iteratively laid across the routing guides to physically implement the routing guides.

+ To run routing in OpenLANE:
  `run_routing`
+ If DRC errors persist after routing the user has two options:
  - Re-run routing with higher QoR settings.
  - Manually fix DRC errors specific in tritonRoute.drc file.

## TritonRoute Features
TritonRoute is a place-and-route tool used in the semiconductor industry to automate the process of creating physical designs for integrated circuits (ICs). TritonRoute is often used in conjunction with other Electronic Design Automation (EDA) tools in the design flow to generate the physical layout of an IC.

### Honors pre-processed route guides
- **TritonRoute:** TritonRoute is an Electronic Design Automation (EDA) tool used in semiconductor IC design to automate the process of creating physical layouts.

- **Route Guides:** Route guides are predefined or user-defined paths that specify how interconnects (wires) should be routed on an IC, helping ensure proper signal timing and power efficiency.

- **Pre-processing:** Pre-processing involves preparing the IC design and routing environment before actual routing occurs, which can include analyzing the design and identifying routing areas.

- **Honoring Route Guides:** This TritonRoute feature involves the tool following specified or pre-processed route guides during the routing process, ensuring that routing adheres to design intentions and constraints.

- **Automatic Routing:** TritonRoute may automatically route interconnects while respecting specified route guides.

- **Constraint Adherence:** The tool enforces constraints such as wire length, width, and layer assignments based on the specified route guides.

- **Dynamic Adjustment:** It may dynamically adjust routing paths to optimize the design while still honoring route guides.

- **Efficiency and Timing:** The feature optimizes routing paths for factors like wirelength, congestion, and signal timing while adhering to route guides.

- **Variability:** Specific capabilities and usage of this feature may vary between TritonRoute versions and other EDA tools.

- **Documentation and Support:** Users would typically consult TritonRoute's documentation or seek support for guidance on effectively using the "Honors pre-processed route guides" feature in their IC design projects.

### Inter-guide Connectivity
- **Route Guides:** Predefined or user-specified paths for interconnect routing on an IC.

- **Inter-guide Connectivity:** TritonRoute establishes connections between different route guides.

- **Use Cases:** Useful for complex layouts where connections are needed between separate route guides, e.g., connecting logic blocks, memory cells, or input/output pads.

- **Optimization:** TritonRoute optimizes inter-guide connections to meet design goals, such as minimizing wirelength, reducing congestion, and maintaining signal integrity.

### Intra- & Inter-layer Routing
- **Intra-layer Routing:** Routing wires within a single layer of the IC while adhering to design constraints and route guides.

- **Inter-layer Routing:** Routing wires that traverse multiple layers of the IC, including vertical connections (vias) between layers.

- **Layer Considerations:** TritonRoute considers layer-specific resources, metal types, and spacing rules during routing.

- **Signal Integrity:** Ensures that interconnects maintain their electrical characteristics when transitioning between layers.

- **Timing and Congestion:** Optimizes routing for timing requirements and congestion management, facilitating efficient communication between IC components.

### TritonRoute method to handle connectivity
- **Design Input:** TritonRoute starts with the initial IC design, including logical components and constraints.

- **Route Guides:** Predefined or user-specified paths dictate how wires should be routed.

- **Initial Placement:** TritonRoute performs an initial placement of components on the IC layout.

- **Routing Algorithm:** It employs routing algorithms considering timing, wirelength, congestion, layer specifics, and signal integrity.

- **Inter-Layer Routing:** Handles connections between different metal layers using vias.

- **Obstacle Avoidance:** Avoids physical obstacles like wires and components during routing.

- **Constraint Adherence:** Ensures routing paths adhere to route guides and design rules.

- **Optimization:** Optimizes routing for goals like wirelength minimization and congestion reduction.

- **Post-Processing:** Performs post-routing tasks such as compliance checks and report generation.

- **Output:** Provides the finalized physical IC layout with detailed routing.

### Routing Topology Algorithm
A routing topology algorithm is a critical component of Electronic Design Automation (EDA) tools used in semiconductor design, specifically during the routing phase of integrated circuits (ICs). Its primary function is to determine the logical structure or topology of how interconnections (wires) should be routed on the chip's layout. Here's an explanation of this algorithm:

- **Input and Initialization:** The algorithm takes as input the logical netlist of the design, which describes how the various components and blocks are connected, as well as the initial placement of these components on the chip.

- **Topology Generation:** Based on the input, the algorithm generates a routing topology. This topology defines how signals will flow from one component to another, considering factors like timing constraints, signal integrity, and power consumption.

- **Path Planning:** The algorithm plans the paths that wires will follow to connect components while adhering to the generated topology. This includes selecting the routing layers (metal layers) and determining the routing direction.

- **Congestion and Obstacle Avoidance:** It takes into account congestion levels on the chip layout and avoids physical obstacles like existing wires, components, and any routing blockages.

- **Optimization:** Routing topology algorithms often include optimization techniques to minimize wirelength, reduce signal delay, and distribute the routing evenly across the chip.

- **Layer Assignment:** It assigns each interconnect to the appropriate metal layer, considering the design's requirements and constraints for signal performance.

- **Via Insertion:** In multi-layer designs, the algorithm inserts vias (vertical connections) where needed to connect wires between different metal layers.

- **Routing Rules Adherence:** The algorithm ensures that routing adheres to design rules, such as minimum and maximum wire widths, spacing, and layer stack-up.

- **Iteration:** The routing process may involve multiple iterations to refine and improve the routing solution.

- **Final Routing:** Once the algorithm determines the optimal routing paths, it generates the detailed routing for the entire IC design.

### Final Files List Post-Route:
After the routing phase is completed in an EDA tool like TritonRoute, a set of final files and reports are generated to document and verify the results of the routing process. These files are essential for design validation and handoff to the manufacturing stage. Here's a list of some common final files generated post-route:

- **Routed Layout:** This is the final layout of the IC with all interconnections and routing paths in place.

- **Design Rule Check (DRC) Reports:** Reports that confirm compliance with design rules, such as minimum spacing, width, and other manufacturing constraints.

- **Layout vs. Schematic (LVS) Reports:** These reports compare the physical layout to the original schematic to ensure that they match.

- **Timing Reports:** Detailed timing analysis reports to verify that signal timing requirements have been met.

- **Power Reports:** Information on power consumption and distribution in the routed design.

- **Congestion Maps:** Visual representations of congestion levels on the chip to help identify potential issues.

- **Layer Stack-Up Files:** Documentation of the metal layer stack-up, including information on the types and order of metal layers used.

- **VIA Lists:** Lists of vias used in the design for inter-layer connections.

- **Routing Logs:** Detailed logs of the routing process, including any warnings or errors encountered.


