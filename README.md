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
    <img width="975" height="710" alt="image" src="https://github.com/user-attachments/assets/3bce6050-9f09-48e4-b64e-cc0a220a73b6" />
  </p>
  
**Simplified ASIC design flow**
  <p align="center">
    <img width="975" height="623" alt="image" src="https://github.com/user-attachments/assets/0e45bb88-cb65-4b45-9efc-b897a53f6409" />
  </p>
  
***Synthesis :*** Design RTL is converted to circuit made out elements from standard cell library. The resultant circuit is described in HDL and usually referred to as the gate level netlist. A gate level netlist Is functionally equivalent to the RTL.  
The library building blocks for the cells have regular layouts typically the cell layout of fixed heights rectangle with is variable but discrete integer multiple of a fixed value called site width. Each cell comes with different view/models.  
-	Electrical (liberty format; delay, power models), HDL (behavioral), SPICE(cdl),
-	Layout (Abstract(lef) and detailed(gdsii))
  <p align="center">
    <img width="384" height="255" alt="image" src="https://github.com/user-attachments/assets/87457edf-6acc-40a4-8194-315a4910f85d" />
  </p>
  
***Floor and Power planning :*** Depends on whether a macro or entire chip. The objective is to plan Silicon area and create robust power distribution network to power the circuit.  
Chip floor planning: Partition the chip die into different system building blocks and place the I/O pads.  
  <p align="center">
    <img width="975" height="269" alt="image" src="https://github.com/user-attachments/assets/4f093a49-9775-4bb9-a264-bbe09d810d54" />
  </p>
Macro Floor planning: Dimensions, pin locations, row definitions  
  <p align="center">
    <img width="645" height="500" alt="image" src="https://github.com/user-attachments/assets/25f2feba-3c56-4d25-bce3-cbc578ad0bcd" />
  </p>
  
***Power planning***
  <p align="center">
    <img width="975" height="398" alt="image" src="https://github.com/user-attachments/assets/3a405bf7-b3fe-4086-9840-933b1bfba65a" />
  </p>
Uses upper metal layers as they are thicker than lower metal layers hence have lower resistance.  

***Placement :*** Place the cells on the floorplan rows aligned with the sites. In 2 types; global and detailed. Finds optimal position for the cells May not be legal. The positions are legalized by making minor adjustments  to the position of the cells.
  <p align="center">
    <img width="975" height="332" alt="image" src="https://github.com/user-attachments/assets/679d4dae-dcdb-4836-97b1-d20eb722f29a" />
  </p>
  <p align="center">
    <img width="975" height="424" alt="image" src="https://github.com/user-attachments/assets/3924584f-3c7c-47db-9396-9a55103a6c40" />
  </p>
  
***Clock Tree synthesis :***
Create a clock distribution network
-	To deliver the clock to all sequential elements (e.g., FF).
-	With minimum skew (zero is hard to achieve).
-	And in good shape
-	Usually a Tree (H, X, …).
  <p align="center">
    <img width="330" height="255" alt="image" src="https://github.com/user-attachments/assets/2899e645-4216-4e91-badc-3c4178ffaec1" />
  </p>

***Routing :***
Implement the interconnect using the available metal layers, the PDK defines the thickness pitch, tracks and the minimum width.
  <p align="center">
    <img width="975" height="368" alt="image" src="https://github.com/user-attachments/assets/f993e50c-d79a-46c6-9a85-b486892751e8" />
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
    <img width="816" height="612" alt="image" src="https://github.com/user-attachments/assets/4ce0e34e-08e9-436e-aa76-2d165950073d" />
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
    <img width="975" height="599" alt="image" src="https://github.com/user-attachments/assets/6a0eab63-b6dc-4dd0-b426-14fe5c6a0bc7" />
  </p>
  
The flow starts with the design RTL and ends with the final layout in the GDSII format. To function it  needs the PDK. Open lane is based on several open source projects such as openRoad Yosys, ABC, QFlow, Fault, etc.  

***RTL synthesis:*** the RTL is fed to yosys along with design constraints. Yosys translates the RTL into a logic circuit using generic components. This circuit can be optimized and mapped into cells from SCL using ABC. ABC has to be guided during the optimization and this guidance comes in the form of ABC script. Openlane comes with several ABC scripts. With different synthesis strategies. We have strategies that targets area, timing, etc. Different strategies can be used to obtain the required objectives. Synthesis exploration utilities that can be used to generate a report that shows how the design delay and area is affected by the synthesis strategy, based on this we can pick the best synthesis strategy to continue with.  

Also openlane has design exploration utilities which can be used to sweep the design configurations and generates a report, which shows design metrics 
  <p align="center">
    <img width="975" height="533" alt="image" src="https://github.com/user-attachments/assets/3a7596ea-64dd-487f-8715-c5e69a2e2efe" />
  </p>

The design exploration utility is also used for regression testing(CI)
We run openlane on ~70 designs and compare the results to the best known ones  
  <p align="center">
    <img width="550" height="598" alt="image" src="https://github.com/user-attachments/assets/6e1f63fc-bcd9-4eed-a74e-f90c44211dae" />
  </p> 
  
**Design for Testing :** After synthesis comes the testing structure insertion, if we want our design to be ready for  testing after fabrication  we can enable this step which is optional. This step uses opensource project fault to perform 
-	Scan insertion
-	Automatic Test Pattern Generation (ATPG)
-	Test Patterns Compaction
-	Fault Coverage
-	Fault Simulation
  <p align="center">
    <img width="975" height="384" alt="image" src="https://github.com/user-attachments/assets/05176a08-b02b-4c46-bd0d-29c2d5b1fdbd" />
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
    <img width="654" height="326" alt="image" src="https://github.com/user-attachments/assets/45758b39-f8bb-4add-8595-b3907f7c878a" />

  </p> 

Two solutions:
-	Bridging attaches a higher layer intermediary
  -	Requires router awareness(not there yet)
-	Add antenna diode cell to leak away charges 
  - Antenna diodes are provided by the SCL.
  <p align="center">
    <img width="975" height="398" alt="image" src="https://github.com/user-attachments/assets/35d9b2cb-45e9-4746-a8e2-abf4d7cef7bf" />
  </p> 
  <p align="center">
    <img width="975" height="264" alt="image" src="https://github.com/user-attachments/assets/177b067d-8afc-4538-b94a-8f963dc726b0" />
  </p> 

We took a preventive approach
-	Add a Fake antenna diode next to every cell input after placement
-	Run the Antenna checker (Magic) on the routed layout
-	If the checker reports a violation on the cell input pin, replace the Fake diode cell by a real one.
Openlane has a configuration to select one of the two approaches to handle the antenna violations.
  <p align="center">
    <img width="356" height="348" alt="image" src="https://github.com/user-attachments/assets/98251fd4-9d1c-480e-a44e-f1983ccac7e7" />
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
    <img width="835" height="262" alt="image" src="https://github.com/user-attachments/assets/2f3437c1-86ec-4346-b26a-9a5045d8e8ec" />
  </p> 

FF - Flip Flops/Latches/Registers  
A1, O1 - Standard cells(AND,OR,INVERTER)  
Consider a netlist with 2 flops and 2 AND gates, with above shown connections. (A netlist describes the connectivity of an electronic design). Though the logic gates are represented using different symbols, the standard cells are rectangular with a fixed height and variable width, which is usually an integral multiple of fixed value called site width.  
Assuming a dimension of 1u x 1u, the cell will have an area of 1 sq. u. The minimum area occupied by the netlist will the total area of all the cells (wire lenght is excluded).

   <p align="center">
    <img width="764" height="460" alt="image" src="https://github.com/user-attachments/assets/edb761ef-edda-445e-9421-8e1ffb5b3158" />
  </p>

  Rearranging the cells as shown in the below picture we get a total area of 4sq. units.  
  What is 'core' and 'die' section of a chip?  
  **Core** – A core is the section of the chip where the fundamental logic of the design is placed.  
  **Die** – A die, which consists of core, is small semiconductor material specimen on which the fundamental circuit is fabricated.  
  
  <table align="center">
  <tr>
    <td align="center">
      <img width="351" height="274" alt="image" src="https://github.com/user-attachments/assets/e95f8c65-deb8-49a0-b085-4fa90c024448" />
    </td>
    <td align="center">
      <img width="311" height="265" alt="image" src="https://github.com/user-attachments/assets/d3d41a73-76ad-4380-9f4d-5432e9b862be" />
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
    <img width="1638" height="971" alt="image" src="https://github.com/user-attachments/assets/9406b910-0b3a-4eb3-8433-1924ec3928b9" />
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
      <img width="423" height="220" alt="image" src="https://github.com/user-attachments/assets/c63c4739-c38f-496f-bae7-941796dab48e" />
    </td>
    <td align="center">
      <img width="270" height="216" alt="image" src="https://github.com/user-attachments/assets/776acfca-068a-4fd0-b925-048194499c74" />
    </td>
  </tr>
</table>

   <p align="center">
    <img width="548" height="267" alt="image" src="https://github.com/user-attachments/assets/e22eac79-8a33-4bd1-9393-c2a7674b2cec" />
  </p>

There are IP’s available for eg. Memory, Clock-gating cell, comparator, Mux
-	The arrangement of these IPs in a chip is referred to as floor planning
-	These IP’s/blocks have user-defined locations, and hence are placed in chip before automated placement-and-routing are called as **_pre-placed_** cells
-	Automated placement and routing tools place the remaining logical cells in the design onto chip.

The location of the preplaced cells are decided by the design scenario, let’s say a block has most of the connections with input ports, then the block is placed closer to the input ports. Similarly, the design background/summary will decide the location of the pre-placed cells. These pre-placed cells once placed are not touched during rest of the flow, so the locations have to be decided carefully.

   <p align="center">
    <img width="604" height="385" alt="image" src="https://github.com/user-attachments/assets/1741a926-3d41-4f61-98f9-ad2dd9e8e258" />
  </p>

**Surround pre-placed with decoupling capacitors**  
***Decoupling capacitors***  
Consider the amount of switching current required for a complex circuit something like below:  

   <p align="center">
    <img width="975" height="452" alt="image" src="https://github.com/user-attachments/assets/c3b045a9-3737-496d-bd7c-629804a50099" />
  </p>

  <table align="center">
  <tr>
    <td align="center">
      <img width="511" height="233" alt="image" src="https://github.com/user-attachments/assets/0f2b1fc4-25aa-4802-9ee5-d2bb9bdf1673" />
    </td>
    <td align="center">
      <img width="426" height="232" alt="image" src="https://github.com/user-attachments/assets/2878e4fb-6166-49ef-8a47-98213bf6b717" />
    </td>
  </tr>
</table>

  <table align="center">
  <tr>
    <td align="center">
      <img width="500" height="265" alt="image" src="https://github.com/user-attachments/assets/730b0fd6-2c4d-40ae-817e-2a56ff25f018" />
    </td>
    <td align="center">
      <img width="467" height="360" alt="image" src="https://github.com/user-attachments/assets/969deab2-dadd-4bf9-806d-84d9765df434" />
    </td>
  </tr>
</table>


When the output of let’s say an AND gate in the circuit switches its output from logic 0 to logic 1, there is current demand which has to charge the capacitance at output of the AND gate to represent the logic 1. This current is supplied by the power supply. The parasitics causes voltage drop, which might lead to undefined voltage level. To solve this we add a decoupling capacitor that will supply the charge at times of such current demands.

**Power Planning**  
We have taken care of the local communication. Now we have to solve the global communication. Consider the case where we have multiple instances of the block for which we added the decoupling capacitor. All the blocks are interconnected as shown in the pictures below. If the orange line is a 16-bit bus, any switching from driver to load has to be intact which needs the charge supply.

  <table align="center">
  <tr>
    <td align="center">
      <img width="356" height="259" alt="image" src="https://github.com/user-attachments/assets/af9d85a1-2744-4126-a299-9f0138884f6a" />
    </td>
    <td align="center">
      <img width="349" height="259" alt="image" src="https://github.com/user-attachments/assets/344d78fc-c8a5-4af0-b0b6-22bab52687d5" />
    </td>
  </tr>
</table>

Consider the initial state of the 16-bit bus connected through an inverter.  
  <p align="center">
    <img width="510" height="288" alt="image" src="https://github.com/user-attachments/assets/6a85ac66-9858-44dc-a019-d3bb9014a4c1" />
  </p>
All the capacitor charged to V volts have to discharge to 0 volts through single ground tap point. This will cause a bump in ground tap point called the ground debounce. If this bounce exceeds the noise margin then the signal enters the undefined state.
  <p align="center">
    <img width="975" height="254" alt="image" src="https://github.com/user-attachments/assets/369c0254-e86a-4402-81ec-12dd456fe829" />
  </p>
All the capacitor charged to 0 volts have to charge to V volts through single Vdd tap point. This will cause lowering of voltage at Vdd tap point called the Voltage droop.    

  <p align="center">
    <img width="975" height="230" alt="image" src="https://github.com/user-attachments/assets/b02b73cf-f92c-42ec-b22d-dab7e99f981b" />
  </p>

The cause of this problem is that the the supply is coming from a single point. If there were power supply all over the place then they would've satisfied the requirement. This problem is solved by adding multiple vdd and vss supplies. To achieve this a mesh like structure is created for the vdd and vss lines so that any cell or macro requiring the supply can get it from the nearest tap points. the tap points are the intersetion points on the mesh structure. This is called ***Power Planning***.

  <table align="center">
  <tr>
    <td align="center">
      <img width="462" height="358" alt="image" src="https://github.com/user-attachments/assets/9422c952-328a-4e5c-91d0-59720349476f" />
    </td>
    <td align="center">
      <img width="464" height="303" alt="image" src="https://github.com/user-attachments/assets/a0eec697-c77c-42f6-8221-013c01fabee9" />
    </td>
  </tr>
</table>

**Pin Placement**  
For example, consider the below design that needs to be implemented.
  <p align="center">
    <img width="714" height="496" alt="image" src="https://github.com/user-attachments/assets/5fccab0b-539a-4336-9067-6e98211781d9" />
  </p>
  
The placement of I/O pins depends on the design requirements. In this case all the input ports are on the left and all the output pins are on the right. The clock pin drives a large number of cells hence it needs to have least resistance path, which is why the size of the clock pins are large compared to the other pins.  

  <table align="center">
  <tr>
    <td align="center">
      <img width="452" height="287" alt="image" src="https://github.com/user-attachments/assets/16215d4c-0738-43b6-8f2d-33814de90ffd" />
    </td>
    <td align="center">
      <img width="389" height="287" alt="image" src="https://github.com/user-attachments/assets/7fc35142-f2ee-4b40-9607-153547c4b536" />
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
   <img width="1285" height="805" alt="image" src="https://github.com/user-attachments/assets/4a01838d-31db-4bc5-9058-21241eb89a38" />
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
     <img width="1285" height="806" alt="image" src="https://github.com/user-attachments/assets/7cfc2717-d420-42c1-91ca-d22bbfa075c5" />
  </p>

First run with just the default floorplan.tcl and config.tcl(in design dir). The default value of 50% for FP_CORE_UTIL is overridden in the config.tcl. The result can be checked by opening the config.tcl in runs directory. In my case it is in


```bash

cd /home/vscode/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.24_14.30.50
gvim config.tcl

```
  <p align="center">
   <img width="1285" height="805" alt="image" src="https://github.com/user-attachments/assets/1b71d048-7ef5-4f52-8547-c4a961243584" />
   <img width="1283" height="803" alt="image" src="https://github.com/user-attachments/assets/cd2b0dc1-b1a2-4530-ad3c-74d6dae65bb9" />
  </p>

Now add the &lt;sky130&gt;config.tcl (sky130A_sky130_fd_sc_hd_config.tcl)
<p align="center">
 <img width="1285" height="803" alt="image" src="https://github.com/user-attachments/assets/9b738d8f-bb62-47e1-aef6-8e7a96ba5f3e" />
 </p>

**NOTE** : The precedence of the &lt;sky130&gt;config.tcl depends on when it is sourced. To make sure the above mentioned precedence is followed update the config.tcl as shown.  

<p align="center">
 <img width="1284" height="804" alt="image" src="https://github.com/user-attachments/assets/0cb9e2c9-8660-471d-b255-950afecb9b6e" />
 <img width="1286" height="804" alt="image" src="https://github.com/user-attachments/assets/0d2ba3c4-4eac-47c3-bc07-5f5e6191cc1b" />
 </p>

The def file is in 
```bash
/home/vscode/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.24_14.30.50/results/floorplan/picorv32a.def
```
<p align="center">
 <img width="1284" height="804" alt="image" src="https://github.com/user-attachments/assets/598e208c-30ad-40f0-8563-b8c4f3c7bd23" />
</p>

 To view using magic use the following command
 ```bash
# Enter into the run directory
cd /home/vscode/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.24_14.30.50
# Invoke the magic tool
magic -T ~/.ciel/sky130A/libs.tech/magic/sky130A.tech  lef read tmp/merged.nom.lef results/floorplan/picorv32a.def &

```

  ```math
1000\ Unit\ Distance = 1\ Micron
```
```math
Die\ width\ in\ unit\ distance = 1279175 - 0 = 1279175
```
```math
Die\ height\ in\ unit\ distance = 1289895 - 0 = 1289895
```
```math
Distance\ in\ microns = \frac{Value\ in\ Unit\ Distance}{1000}
```
```math
Die\ width\ in\ microns = \frac{1279175}{1000} = 1279.175\ Microns
```
```math
Die\ height\ in\ microns = \frac{1289895}{1000} = 1289.895\ Microns
```
```math
Area\ of\ die\ in\ microns = 1279.175 * 1289.895 = 1650001.436625\ Square\ Microns
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
     <img width="1288" height="807" alt="image" src="https://github.com/user-attachments/assets/b8142ca4-9289-4308-a827-0e1992d8b83b" />
    </td>
    <td align="center">
     <img width="1284" height="804" alt="image" src="https://github.com/user-attachments/assets/7e887a31-8b32-41ec-a4b9-735cdc37d74e" />
    </td>
  </tr>
</table>

To fit the view to screen press v.   
To select left click and right click to form a bounding box, then press ctrl+z to zoom into selection.  
To select a particular object place the mouse pointer on the object and press s. In tkcon window use what command to get the details.  

 <table align="center">
  <tr>
    <td align="center">
     <img width="1285" height="805" alt="image" src="https://github.com/user-attachments/assets/5d2b3fa3-2c5f-4ebc-9980-9ceea9275d65" />
    </td>
    <td align="center">
     <img width="1286" height="804" alt="image" src="https://github.com/user-attachments/assets/12805c6b-21ad-4b73-b170-35a9efdcb6b5" />
    </td>
  </tr>
</table>

The decap are the de coupling capacitors and the tap cells are used to avoid latchup conditions in CMOS devices. The nwell connected to vdd and substrate to gnd.
</details>
<details>
 <summary><b>Phase 3 - Timing Literacy with Ideal Clocks (OpenSTA + ECO mindset)</b></summary>
 
 ### Timing analysis with ideal clocks using openSTA

 ***Setup Timing Analysis***
 ```
Specifications:
Clock Frequency(F) = 1GHz
Clock Period (T) = 1/F = 1/1GHz =1ns
```

<p align="center">
 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/90546ba0-23aa-4d43-8c64-224cfea755f6" />
</p>

Let's assume ideal clocks, i.e. the clocks reach all the flops at the same time and there is no skew. The active edge of the clock reaches the Launch flop at 0 and the Capture flop at T. So the data from launch flop has to reach the D input of the capture flop before T for the system to work. So cobinational delay has to be less than time period. 

```
θ < T
```

Now moving from the ideal scenario to practical scenario :  
There is a delay between the data from D to Qm. This time is called setup time. This must be accounted.
```
θ < T - S
```
 <p align="center">
 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5d19048c-1a05-422d-9a42-aa5da71c3926" />
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/19019c86-a105-45d0-9b3a-ce5c0cbbb359" />  
</p>

The clock is generated by a PLL, which is expected to be ideal, i.e, we expect the edge to be at 0, T, 2T,…, but the practical scenario has some uncertainty, which means the edge can occur around 0, T, ..nT, by a margin of time called setup uncertainty.

Jitter : Temporary variation of the clock period.

<p align="center">
 <img width="1546" height="386" alt="image" src="https://github.com/user-attachments/assets/bb5e1f01-2bc2-4ab4-ad3e-94c426b3ee58" />
 <img width="1596" height="384" alt="image" src="https://github.com/user-attachments/assets/a2301980-9132-401a-8e5a-5671a56ca664" />
 <img width="975" height="308" alt="image" src="https://github.com/user-attachments/assets/f7772edc-c4b1-4712-922b-8b0d51e6f65b" />
</p>

Below images are an examples of paths from a simple design.  
<p align="center">
 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4708556e-9365-443e-9c68-f07613335f3b" />
 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4f73a1e6-9c81-43d6-8e61-502c32c7f0dc" />
 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9eb13ef1-5a8a-447b-aabb-645f86471d5e" />
</p>

**Lab**  
To run Static Timing Analysis we need a conf file. An example is shown below.  

```bash
# I have the file in
/home/vscode/Desktop/OpenLane/pre_sta.conf
```

```
# This line sets the units
set_cmd_units -time ns -capacitance pF -current mA -voltage V -resistance kOhm -distance um

# This defines the slow library for Setup
read_liberty -max /home/vscode/.ciel/sky130A/libs.ref/sky130_fd_sc_hd/lib/sky130_fd_sc_hd__ss_100C_1v60.lib

# This defines the fast library for Hold
read_liberty -min /home/vscode/.ciel/sky130A/libs.ref/sky130_fd_sc_hd/lib/sky130_fd_sc_hd__ff_n40C_1v95.lib

# This is the netlist output from synthesis
read_verilog /home/vscode/Desktop/OpenLane/designs/picorv32a/runs/RUN_2026.02.25_14.44.22/results/synthesis/picorv32a.v

# Link the deisgn to picorv32a
link_design picorv32a

# Setup the SDC for STA (Can be obtained from the base.sdc in /home/vscode/Desktop/OpenLane/scripts)
read_sdc /home/vscode/Desktop/OpenLane/designs/picorv32a/src/picorv32a.sdc

# Report the results
report_checks -path_delay min_max -fields {slew trans net cap input_pin}
report_tns
report_wns

```

<p align="center">
 <img width="1286" height="807" alt="image" src="https://github.com/user-attachments/assets/57718ecc-ef0c-4092-b7b9-aa1be37f5823" />
 <img width="1284" height="804" alt="image" src="https://github.com/user-attachments/assets/f82ae035-8d31-4e56-bb57-79594e3bc385" />
</p>

```bash

# Run STA in a new terminal
cd /home/vscode/Desktop/OpenLane

# Invoke the container
make mount

#Run STA
sta pre_sta.conf

```

[pre_sta.rpt](pre_sta.md)  Click to view the report.  

<p align="center">
 <img width="1286" height="806" alt="image" src="https://github.com/user-attachments/assets/9b4594ec-8c0e-460d-9b24-cd0de674be73" />
</p>  

To re-run synthesis with customisation, the config.tcl can be updated or the env variables can be set on the go in the terminal.  

<p align="center">
 <img width="1284" height="804" alt="image" src="https://github.com/user-attachments/assets/d01d2cb8-ae19-4ce3-8254-164e58d7b73a" />
 <img width="1286" height="806" alt="image" src="https://github.com/user-attachments/assets/d8e583cb-d40e-4985-9d77-de41f6d8c475" />
</p>


[pre_sta.rpt](pre_sta.md)  Click to view the report.  

</details>
<details>
 <summary><b>Phase 4 - CTS and Timing with Real Clocks (bridges directly to Week 4–6)</b></summary>
</details>
<details>
 <summary><b>Phase 5 - PDN Awareness (required vocabulary for ORFS and signoff thinking)</b></summary>
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
