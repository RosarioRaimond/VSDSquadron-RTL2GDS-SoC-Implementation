# VSDSquadron-RTL2GDS-SoC-Implementation

## Content
- [Week 1](#week-1)
- [Week 2](#week-2)
- [Week 3](#week-3)
- [Week 4](#week-4)
- [Week 5](#week-5)
- [Week 6](#week-6)

## Week 1
<details>
 <summary><b>Code Space setup</b></summary>     
  
  The code space can be set up by following the steps in [vsd-openlane](https://github.com/vsdip/vsd-openlane) repo.

```bash

#cd into the openlane directory
cd Desktop/OpenLane

# To check if the codespace is setup correctly and working fine
make test

```

  <p align="center">
    <img width="1280" height="804" alt="image" src="https://github.com/user-attachments/assets/8d9019e3-6872-45f3-93eb-25ad7d173ab1" />
    <img width="1282" height="803" alt="image" src="https://github.com/user-attachments/assets/73185783-747b-4d4b-974c-03895e344cdb" />
  </p>

  Yay!! the codespace is working
  
</details>

<details>
 <summary><b>Phase 1 - OpenLANE Flow Familiarity (RTL → Synthesis literacy)</b></summary>  

 ### SoC Design and OpenLANE
 **Digital ASIC Design**
Requires several elements 
-	RTL IP’s
-	EDA Tools
-	PDK Data
  <p align="center">
    <img width="492" height="409" alt="427110397-c891ef31-b8c7-4926-ae3d-d4d1a58b0619" src="https://github.com/user-attachments/assets/26c3d47c-ac52-433e-8227-be5cc18cb489" />
  </p>
  
***Opensource RTL*** – Many opensource IP’s are available online. Some of the websites where they can be found are 
Librecores.org,
Opencores.org,
Github.com (github alone has 7000 repo).

***Opensource EDA Tools*** - Early EDA tools were result of academic requirements. Examples are Magic, Spice Simulator, qflow, OpenRoad, OpenLane.

***Open PDKs*** - In early days, the design of an IC was tightly integrated with the manufacturing processes available within each company. Those who controlled the physics controlled the creative agenda. Lynn Conway and Carver Mead envisioned the need for separating the design from technology;
Pioneered the "structured" design methodology based on the λ-based rules
Since then, we started to see Pure Play Fabs and Fabless design companies.  
What is PDK?  
PDK(Process Design Kit), is the interface b/w the FAB and the designers. Collection of files used to model a fabrication process for the EDA tools used to design an IC.
- Process Design Rules : DRC, LVS, PEX
- Device Models
- Digital Standard Cell Libraries
- I/O Libraries  
They are distributed under NDA, made difficult for mass production. Google partnered with skywater and release open source PDK skywater130. This is 130nm process, it may seem old/irrelevant but most applications don't need the advanced nodes due to high cost of production. The market share is as shown below.
  <p align="center">
    <img width="839" height="538" alt="image" src="https://github.com/user-attachments/assets/0b0cd504-3875-4e8f-8eef-36fc215679b4" />
  </p>
The 6%, which amounts to 4.7B annual revenue. In terms of performance, the following examples will convince you!!
  <p align="center">
    <img src="https://github.com/user-attachments/assets/0512edec-7c5e-49c4-bbb1-2c03d4010331" width="400" />
  </p>
  
**Simplified ASIC design flow**
  <p align="center">
    <img src="https://github.com/user-attachments/assets/a389d061-817a-4f9d-9d52-58e159bb4bd9" width="600" />
  </p>
  
***Synthesis :*** Design RTL is converted to circuit made out elements from standard cell library. The resultant circuit is described in HDL and usually referred to as the gate level netlist. A gate level netlist Is functionally equivalent to the RTL.  
The library building blocks for the cells have regular layouts typically the cell layout of fixed heights rectangle with is variable but discrete integer multiple of a fixed value called site width. Each cell comes with different view/models.  
-	Electrical (liberty format; delay, power models), HDL (behavioral), SPICE(cdl),
-	Layout (Abstract(lef) and detailed(gdsii))
  <p align="center">
    <img src="https://github.com/user-attachments/assets/d0a528bb-d2c8-49f6-b613-043f60be7bd2" width="500" />
  </p>
  
***Floor and Power planning :*** Depends on whether a macro or entire chip. The objective is to plan Silicon area and create robust power distribution network to power the circuit.  
Chip floor planning: Partition the chip die into different system building blocks and place the I/O pads.  
  <p align="center">
    <img src="https://github.com/user-attachments/assets/23c4156d-25e7-47b4-bdbd-b5e42d09306b" width="700" />
  </p>
Macro Floor planning: Dimensions, pin locations, row definitions  
  <p align="center">
    <img src="https://github.com/user-attachments/assets/08e4c394-7272-48b8-b7a5-0af977cd1ef4" width="400" />
  </p>
  
***Power planning***
  <p align="center">
    <img src="https://github.com/user-attachments/assets/9c0dbb16-c8ac-4d28-8bbd-73a5a6ceeded" width="700" />
  </p>
Uses upper metal layers as they are thicker than lower metal layers hence have lower resistance.  

***Placement :*** Place the cells on the floorplan rows aligned with the sites. In 2 types; global and detailed. Finds optimal position for the cells May not be legal. The positions are legalized by making minor adjustments  to the position of the cells.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/0abc6ab1-dc3a-4682-b8af-68870e81d7b7" width="700" />
  </p>
  <p align="center">
    <img src="https://github.com/user-attachments/assets/4d74bf75-38af-41f1-ba3c-a41e592372d0" width="700" />
  </p>
  
***lock Tree synthesis :***
Create a clock distribution network
-	To deliver the clock to all sequential elements (e.g., FF).
-	With minimum skew (zero is hard to achieve).
-	And in good shape
-	Usually a Tree (H, X, …).
  <p align="center">
    <img src="https://github.com/user-attachments/assets/cf8cc3b3-7155-48b2-86db-2cdc239f3b3d" width="400" />
  </p>

***Routing :***
Implement the interconnect using the available metal layers, the PDK defines the thickness pitch, tracks and the minimum width.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/3b747a06-deee-4f07-9fee-5633242501e6" width="700" />
  </p>
  
Skywater130 :
This PDK defines 6 routing layers, lowest called local interconnect layer (TitaniumNitride layer), the following layers are all Aluminum.  
Metal tracks form a routing grid  
Routing grid is huge  
Divide and Conquer
-	Global Routing: Generates the routing guides
-	Detailed Routing: Uses the routing guides to implement the actual wiring

***Signoff :***
Once done with routing we can construct the final layout, which undergoes verification that includes,  
- Physical Verification
  - Design rule checking(DRC)
  - Layout v/s Schematic(LVS)
- Timing Verification
  - Static Timing Analysis(STA)

**OpenLANE :** Can I build a chip using this flow?  
This flow can be used with commercial EDA Tools. The problem is tougher when using opensource EDA
- Tools qualification
- Tools calibration
- Missing tools
Open lane is a reference ASIC flow by efabless public repo on github. Started as an open-source flow for a true open source tape-out experiment.
striVe si a family of open everything SoCs
-	Open PDK, Open EDA, Open RTL
  <p align="center">
    <img src="https://github.com/user-attachments/assets/e0aa7596-5719-4460-bdef-64bda9d8f657" width="700" />
  </p>
  
**Main goal of OpenLane:**
- Produce a clean GDSII with no human intervention (no-human-in-the-loop). Clean means:
  -	No LVS violations
  -	No DRC violations
  -	Timing violations? WIP!
- Tuned for SkyWater 130nm Open PDK  
  -	Also supports XFAB180 and GF130G
- Containerized  
  -	Functional out of the box
  -	Instructions to build and run natively will follow
- Can be used to harden macros and chips  
- Two modes of operation:
  -	Autonomous or Interactive
- Design Space Exploration  
  - Find the best set of flow configurations.  
- Large number of design examples  
  -	43 designs with their best configurations
  -	More will be added soon

**Open lane ASIC design flow:**
  <p align="center">
    <img src="https://github.com/user-attachments/assets/d010effc-3531-428e-a6ae-88a7d2265748" width="700" />
  </p>
  
The flow starts with the design RTL and ends with the final layout in the GDSII format. To function it  needs the PDK. Open lane is based on several open source projects such as openRoad Yosys, ABC, QFlow, Fault, etc.  

***RTL synthesis:*** the RTL is fed to yosys along with design constraints. Yosys translates the RTL into a logic circuit using generic components. This circuit can be optimized and mapped into cells from SCL using ABC. ABC has to be guided during the optimization and this guidance comes in the form of ABC script. Openlane comes with several ABC scripts. With different synthesis strategies. We have strategies that targets area, timing, etc. Different strategies can be used to obtain the required objectives. Synthesis exploration utilities that can be used to generate a report that shows how the design delay and area is affected by the synthesis strategy, based on this we can pick the best synthesis strategy to continue with.  

Also openlane has design exploration utilities which can be used to sweep the design configurations and generates a report, which shows design metrics 
  <p align="center">
    <img src="https://github.com/user-attachments/assets/9370cd07-6a8f-442c-9ed9-e713d4118fc9" width="700" />
  </p>

The design exploration utility is also used for regression testing(CI)
We run openlane on ~70 designs and compare the results to the best known ones  
  <p align="center">
    <img src="https://github.com/user-attachments/assets/9587a278-7c1d-428a-80ab-d4d7e984c997" width="400" />
  </p> 
  
**Design for Testing :** After synthesis comes the testing structure insertion, if we want our design to be ready for  testing after fabrication  we can enable this step which is optional. This step uses opensource project fault to perform 
-	Scan insertion
-	Automatic Test Pattern Generation (ATPG)
-	Test Patterns Compaction
-	Fault Coverage
-	Fault Simulation
  <p align="center">
    <img src="https://github.com/user-attachments/assets/d8e67882-5d3d-4372-8649-3d411676f05d" width="700" />
  </p> 
  
Adds extra logic, scan chain and data controller- access to scan chain  

**Physical Implementation :** Also called automated PnR (Place and Route). We use openRoad app.    
-	Floor/Power Planning
-	End Decoupling Capacitors and Tap cells insertion
-	Placement: Global and Detailed 
-	Post placement optimization
-	Vlock Tree Synthesis(CTS)
-	Routing : Global and Detailed.

**Logic equivalence checking(LEC)** using yosys: since the netlist generated from synthesis modigied by the optimizations, Logic equivalence check must be performed to ensure the functional equivalence
Everytime the netlist is modified, verification must be performed
-	CTS modifies the netlist
-	Post Placement optimizations modifies the netlist
LEC is used to formally confirm that the function did not change after modifying the netlist.

**Antenna Rules Violation**  
When a metal wire segment is fabricated, it can act as an antenna
-	Reactive ion etching causes charge to accumulate on the wire
-	Transistor gates can be damaged during the fabrication process.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/1bca6465-139a-4da4-85be-13713941ba8e" width="500" />
  </p> 

Two solutions:
-	Bridging attaches a higher layer intermediary
  -	Requires router awareness(not there yet)
-	Add antenna diode cell to leak away charges 
  - Antenna diodes are provided by the SCL.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/7d32d847-8396-481f-89a8-9fa4c2b1c5a8" width="600" />
  </p> 
  <p align="center">
    <img src="https://github.com/user-attachments/assets/7b556867-3538-4233-85f2-c857cc1a7f92" width="600" />
  </p> 

We took a preventive approach
-	Add a Fake antenna diode next to every cell input after placement
-	Run the Antenna checker (Magic) on the routed layout
-	If the checker reports a violation on the cell input pin, replace the Fake diode cell by a real one.
Openlane has a configuration to select one of the two approaches to handle the antenna violations.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/cb27ab3e-be0b-42a0-bd16-5f75802f8496" width="500" />
  </p> 
  
**Signoff :** STA, DRC, LVS
-	RC Extraction: DEF2SPEF
-	STA: OpenSTA (OpenROAD)
-	Magic si used for Design Rules Checking and the SPICE Extraction from Layout
-	Magic and Netgen are used for LVS
  -	Extracted SPICE by Magic vs Verilog netlist.

  ### Get familiar to open-source EDA tools
  [Directory Structure](directory_structure.md)  Click at your own risk :)

To run your own design, follow the same directory structure as shown in /.openlane-designs/picorv32a. At minimum, your design folder should contain:
- config.tcl – design configurations and environment settings
- src/ – RTL source files (sdc and verilog)

run the flow using:
  
```bash
# cd into the openlane directory
cd Desktop/OpenLane

# To setup the enviroment to run custom design use
make mount

# Launch the OpenLANE flow in interactive mode(-interactive switch is used to view the intermediate results)
./flow.tcl -interactive

# Import the required package
package require openlane 1.0.2

# To prep the design use the following command
prep -design <design_name>
prep -design picorv32a

#After executing check that the runs directory is created in the picorv32a(<design_name>) directory
cd ~/Desktop/OpenLane/designs/picorv32a

```
  <p align="center">
    <img width="1285" height="804" alt="image" src="https://github.com/user-attachments/assets/1381fdf1-3801-4308-8e58-1120f9308452" />
    <img width="1287" height="806" alt="image" src="https://github.com/user-attachments/assets/408723ea-5353-4253-a637-16f3f96a350b" />
    <img width="1285" height="804" alt="image" src="https://github.com/user-attachments/assets/64a3a1c5-9f18-4301-aa4c-0fc409bf32a2" />
    <img width="1285" height="803" alt="image" src="https://github.com/user-attachments/assets/301be9af-9c3f-433a-988b-810a681a136b" />
    <img width="1285" height="804" alt="image" src="https://github.com/user-attachments/assets/c6a064e0-154c-4c5e-b110-9d63d6dca149" />
  </p> 

The parameters used in the flow have a default value, if the user has not specified the value, then default value will be used. The user can define custom values in config.tcl file in the designs/picorv32a directory

  <p align="center">
    <img width="1284" height="804" alt="image" src="https://github.com/user-attachments/assets/ff81802c-5149-444b-9fd1-c641f1987bb2" />
  </p> 
  
<details>
 <summary> Directory structure </summary>
 <p>Inside ~/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.23_14.06.07/ </p>
 
```bash
.
├── OPENLANE_COMMIT
├── PDK_SOURCES
├── cmds.log
├── config.tcl
├── config_in.tcl
├── logs
│   ├── cts
│   ├── floorplan
│   ├── placement
│   ├── routing
│   ├── signoff
│   └── synthesis
│       ├── 1-synthesis.errors
│       ├── 1-synthesis.log
│       ├── 1-synthesis.warnings
│       ├── 2-sta.errors
│       ├── 2-sta.log
│       └── 2-sta.warnings
├── openlane.log
├── reports
│   ├── cts
│   ├── floorplan
│   ├── placement
│   ├── routing
│   ├── signoff
│   └── synthesis
│       ├── 1-synthesis.AREA_0.chk.rpt
│       ├── 1-synthesis.AREA_0.stat.rpt
│       ├── 1-synthesis_dff.stat
│       ├── 1-synthesis_pre.stat
│       └── 1-synthesis_pre_synth.chk.rpt
├── results
│   ├── cts
│   ├── floorplan
│   ├── placement
│   ├── routing
│   ├── signoff
│   └── synthesis
│       ├── picorv32a.sdf
│       └── picrv32a.v
├── runtime.yaml
└── tmp
    ├── cts
    |   ├── cts-fastest.lib
    |   ├── cts-fastest.lib.exclude.list
    |   ├── cts-slowest.lib
    |   ├── cts-slowest.lib.exclude.list
    |   ├── cts.lib
    │   └── cts.lib.exclude.list
    ├── floorplan
    ├── layers.list
    ├── merged.max.lef
    ├── merged.min.lef
    ├── merged.nom.lef
    ├── placement
    ├── routing
    │   └── config.tracks
    ├── signoff
    └── synthesis
        ├── 1-sky130_fd_sc_hd__tt_025C_1v80.no_pg.lib
        ├── 1-trimmed.no_pg.lib
        ├── hierarchy.dot
        ├── merged.lib
        ├── post_techmap.dot
        ├── synthesis.sdc
        ├── trimmed.lib
        └── 

```
 <p>The config.tcl here is the final configuration that was used for the run. If you modify any of the variable mid flow, it will be updated in this file. This is a good checkpoint to verify effect of the changes. The cmds.log file takes a record of all the commands used in the flow. </p>
 
</details>

```tcl

# Run synthesis(This will run the yosys and ABC)
run_synthesis

```

  <p align="center">
    <img width="1285" height="806" alt="image" src="https://github.com/user-attachments/assets/00b256e7-5720-4019-8259-34da5244280f" />
  </p> 
  
```bash
/home/vscode/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.23_14.06.07/reports/synthesis/1-synthesis.AREA_0.stat.rpt
```
  <p align="center">
   <img width="1289" height="809" alt="image" src="https://github.com/user-attachments/assets/e7e83e35-36db-4627-9fd7-77492bb533cb" />
   <img width="1287" height="807" alt="image" src="https://github.com/user-attachments/assets/023457b0-f9f5-4d99-809c-b2d6a53ab4c0" />
  </p> 

```bash
/home/vscode/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.23_14.06.07/logs/synthesis/2-sta.log
```
  <p align="center">   
   <img width="1291" height="807" alt="image" src="https://github.com/user-attachments/assets/b22ed49a-da49-4f52-b665-85b2c0f03762" />
   </p> 

```math
Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}  
            = \frac{1613}{15762}  
            = 0.1023347290952925  
```
<br />

```math

Percentage\ of\ DFF's = Flop\ Ratio * 100  
                      = 0.1023347290952925 *100  
                      = 10.23 % 

```
<br />

[OpenLANE Resource](https://github.com/efabless/openlane2)  
[Youtube link1](https://www.youtube.com/watch?v=EczW2IWdnOM)  
[Youtube link2](https://www.youtube.com/watch?v=Vhyv0eq_mLU)
</details>  

<details>
 <summary><b>Phase 2 - Floorplan Fundamentals (macro awareness for Caravel blocks)</b></summary>  
 
 **Defining width and height of core and die**  
   <p align="center">
    <img src="https://github.com/user-attachments/assets/494732a5-2e6c-4eee-bc99-8e373c45f20c" width="700" />
  </p> 

FF - Flip Flops/Latches/Registers  
A1, O1 - Standard cells(AND,OR,INVERTER)  
Consider a netlist with 2 flops and 2 AND gates, with above shown connections. (A netlist describes the connectivity of an electronic design). Though the logic gates are represented using different symbols, the standard cells are rectangular with a fixed height and variable width, which is usually an integral multiple of fixed value called site width.  
Assuming a dimension of 1u x 1u, the cell will have an area of 1 sq. u. The minimum area occupied by the netlist will the total area of all the cells (wire lenght is excluded).

   <p align="center">
    <img src="https://github.com/user-attachments/assets/e234f2ac-08d6-4c8f-8509-6a4288e88ea3" width="500" />
  </p>

  Rearranging the cells as shown in the below picture we get a total area of 4sq. units.  
  What is 'core' and 'die' section of a chip?  
  **Core** – A core is the section of the chip where the fundamental logic of the design is placed.  
  **Die** – A die, which consists of core, is small semiconductor material specimen on which the fundamental circuit is fabricated.  
  
  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/d3a092a3-f599-4677-8d75-5de02c4c2f40" width="300"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/fe1ef751-9bc3-4caa-b7cb-976619f6cf10" width="300"/>
    </td>
  </tr>
</table>

  Place all the logical cells inside the core. The logical cells occupy the complete area of the core. So in this case the utilization 
  is 100%.  

```math
Utilization\ Factor = \frac{Area\ Occupied\ by\ Netlist}{Total\ Area\ of\ Core}
                    = \frac{4\ sq.\ units}{2\ *\ 2\ sq.\ units}
                    = 1

```
```math
Aspect\ Ratio = \frac{Height}{Width}
                    = \frac{2}{2}
                    = 1

```
<br> </br>
   <p align="center">
    <img src="https://github.com/user-attachments/assets/5d2e276f-f793-4fad-bc93-1e5ef5630793" width="500" />
  </p>

```math
Utilization\ Factor = \frac{Area\ Occupied\ by\ Netlist}{Total\ Area\ of\ Core}
                    = \frac{4\ sq.\ units}{4\ *\ 2\ sq.\ units}
                    = 0.5

```
```math
Aspect\ Ratio = \frac{Height}{Width}
                    = \frac{2}{4}
                    = 0.5

```

Whenever the aspect ratio is 1, it means the shape of the die is a square otherwise it is a rectangle.

 **Define Locations of preplaced cells**  
 ***Preplaced cells :*** Let’s say there is combinational logic that performs a specific task and circuit is pretty huge (50k to 100k gates).  We need not implement it every time it is used in the design. It is implemented as a separate block as IP. This IP can be directly used in our design as many times as required without implementing it multiple times.  
 
In the combinational circuit we can again split to blocks as shown below. The two blocks are implemented separately. Each block will have its own set of inputs and outputs. The two blocks can be now treated as blackboxes after defining the set of inputs and outputs of each block. Each block can be implemented independently.

  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c5f03532-9716-4f21-b70e-5b48abd679af" width="350"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/179283ba-de18-4f2b-ac39-6156b092c88a" width="350"/>
    </td>
  </tr>
</table>

   <p align="center">
    <img src="https://github.com/user-attachments/assets/7da8674f-99be-40c4-a7da-efabcb8500b9" width="500" />
  </p>

There are IP’s available for eg. Memory, Clock-gating cell, comparator, Mux
-	The arrangement of these IPs in a chip is referred to as floor planning
-	These IP’s/blocks have user-defined locations, and hence are placed in chip before automated placement-and-routing are called as **_pre-placed_** cells
-	Automated placement and routing tools place the remaining logical cells in the design onto chip.

The location of the preplaced cells are decided by the design scenario, let’s say a block has most of the connections with input ports, then the block is placed closer to the input ports. Similarly, the design background/summary will decide the location of the pre-placed cells. These pre-placed cells once placed are not touched during rest of the flow, so the locations have to be decided carefully.

   <p align="center">
    <img src="https://github.com/user-attachments/assets/944cfdab-f9b5-441a-ae8f-288f9e0c26c8" width="500" />
  </p>

**Surround pre-placed with decoupling capacitors**  
***Decoupling capacitors***  
Consider the amount of switching current required for a complex circuit something like below:  

   <p align="center">
    <img src="https://github.com/user-attachments/assets/0950a219-5a81-4309-bc58-fee414ceee00" width="500" />
  </p>

  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/0202ac38-864b-47b6-b666-00cef07e9f8b" width="350"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/1b725a8d-2178-4986-bd7e-99160eda681e" width="350"/>
    </td>
  </tr>
</table>

  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/e815ced8-5154-4eac-bc51-6a88df52a985" width="350"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/1279009b-f499-47a6-8a7a-7d276af3c146" width="350"/>
    </td>
  </tr>
</table>


When the output of let’s say an AND gate in the circuit switches its output from logic 0 to logic 1, there is current demand which has to charge the capacitance at output of the AND gate to represent the logic 1. This current is supplied by the power supply. The parasitics causes voltage drop, which might lead to undefined voltage level. To solve this we add a decoupling capacitor that will supply the charge at times of such current demands.

**Power Planning**  
We have taken care of the local communication. Now we have to solve the global communication. Consider the case where we have multiple instances of the block for which we added the decoupling capacitor. All the blocks are interconnected as shown in the pictures below. If the orange line is a 16-bit bus, any switching from driver to load has to be intact which needs the charge supply.

  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/675ac3cd-bb8a-4dce-a7ba-c915390b575d" width="350"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/6cbfd7c6-74cf-4e86-8e16-0daa802fca5d" width="350"/>
    </td>
  </tr>
</table>

Consider the initial state of the 16-bit bus connected through an inverter.  
  <p align="center">
    <img src="https://github.com/user-attachments/assets/585e79cb-10c8-413e-be9f-c360c4f2d04d" width="500" />
  </p>
All the capacitor charged to V volts have to discharge to 0 volts through single ground tap point. This will cause a bump in ground tap point called the ground debounce. If this bounce exceeds the noise margin then the signal enters the undefined state.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/ef9b3129-aa4a-41cb-b4c4-44214c247933" width="500" />
  </p>
All the capacitor charged to 0 volts have to charge to V volts through single Vdd tap point. This will cause lowering of voltage at Vdd tap point called the Voltage droop.    

  <p align="center">
    <img src="https://github.com/user-attachments/assets/b575a1c5-b02a-4798-bf3e-f53e78bc82f6" width="500" />
  </p>

The cause of this problem is that the the supply is coming from a single point. If there were power supply all over the place then they would've satisfied the requirement. This problem is solved by adding multiple vdd and vss supplies. To achieve this a mesh like structure is created for the vdd and vss lines so that any cell or macro requiring the supply can get it from the nearest tap points. the tap points are the intersetion points on the mesh structure. This is called ***Power Planning***.

  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/518ab0a1-ebee-48b8-85d9-3df80adf8f3e" width="400" />
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/89faf0c8-3f8b-4948-b80e-19373a769ea2" width="450" />
    </td>
  </tr>
</table>

**Pin Placement**  
For example, consider the below design that needs to be implemented.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/1b42e965-36a9-4ccc-b82a-96de1dfcebfb" width="500" />
  </p>
  
The placement of I/O pins depends on the design requirements. In this case all the input ports are on the left and all the output pins are on the right. The clock pin drives a large number of cells hence it needs to have least resistance path, which is why the size of the clock pins are large compared to the other pins.  

  <table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/aca7b7e3-7169-447b-84fa-c2dbec77b571" width="450" />
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/6f2ce085-4eaa-44e1-9fe0-74ee02bdf909" width="400" />
    </td>
  </tr>
</table>

The area where the pins are placed has to be blocked for the automated place and route tool hence a logical cell placement blockage is inserted in this area.

**Lab2**  
In the below directory, there are config.tcl files for each step. This is like the default setting that will be used if any configuration is not specified for any particular step.  

```bash
cd ~/Desktop/OpenLane/configuration/
```
  <p align="center">
   <img width="715" height="350" alt="image" src="https://github.com/user-attachments/assets/a64d6616-f50b-4728-affe-75fece608cee" />
   <img width="1284" height="803" alt="image" src="https://github.com/user-attachments/assets/3cd60a0d-7560-4524-8ce2-1f214cec2a15" />
  </p>

```bash
less ~/Desktop/OpenLane/docs/source/reference/configuration.md
```

The configuration.md file in this directory gives a brief description of the different types of options/switches available like FP_CORE_UTIL(sets the core utilization, 50% by default).  
Order of precedence for the configuration is  
configurations/&lt;step&gt;.tcl -> config.tcl(inside the design dir) -> &lt;sky130&gt;config.tcl  



```bash
#command to run floorplan
run_floorplan
```
  <p align="center">
     <img width="1285" height="806" alt="image" src="https://github.com/user-attachments/assets/67681832-e7c2-49b8-b7c6-6ccc1023acf5" />
  </p>

  ```math
1000\ Unit\ Distance = 1\ Micron
```
```math
Die\ width\ in\ unit\ distance = 660685 - 0 = 660685
```
```math
Die\ height\ in\ unit\ distance = 671405 - 0 = 671405
```
```math
Distance\ in\ microns = \frac{Value\ in\ Unit\ Distance}{1000}
```
```math
Die\ width\ in\ microns = \frac{660685}{1000} = 660.685\ Microns
```
```math
Die\ height\ in\ microns = \frac{671405}{1000} = 671.405\ Microns
```
```math
Area\ of\ die\ in\ microns = 660.685 * 671.405 = 443587.212425\ Square\ Microns
```

  
  ```bash
  # Change directory to path containing generated floorplan def
  cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/17-03_12-06/results/floorplan/
  
  # Command to load the floorplan def in magic tool
  magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
  ```

 <table align="center">
  <tr>
    <td align="center">
     <img width="1920" height="935" alt="vsd10" src="https://github.com/user-attachments/assets/f7621886-891f-4ce6-af12-12dcb359f832" />
    </td>
    <td align="center">
     <img width="1920" height="935" alt="vsd11" src="https://github.com/user-attachments/assets/e905243c-5783-407b-bd84-5e871d7731d0" />
    </td>
  </tr>
</table>
</details>


## Week 2
<details>
 <summary><b>Chip Floor planning considerations</b></summary>
</details>

## Week 3
<details>
 <summary><b>Chip Floor planning considerations</b></summary>
</details>

## Week 4
<details>
 <summary><b>Chip Floor planning considerations</b></summary>
</details>

## Week 5
<details>
 <summary><b>Chip Floor planning considerations</b></summary>
</details>

## Week 6
<details>
 <summary><b>Chip Floor planning considerations</b></summary>
</details>
