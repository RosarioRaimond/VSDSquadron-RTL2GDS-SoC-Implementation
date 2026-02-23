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
