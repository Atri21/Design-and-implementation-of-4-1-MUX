# Design-and-implementation-of-4-1-MUX on CMOS 28nm technology
# Table of Contents

# Introduction
The design proposed here is the most basic CMOS implementation of 4:1 MUX. We implement this using 28nm technology in Synopsis tool. In order to fully utilize the power, area and cost advantages of CMOS over SiGe and another semiconductor technology, these circuits must be integrated on one chip. 

# Tools used
* Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
* Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
* Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Working
A multiplexer, also known as a data selector, is a device that selects between several analog or digital input signals and forwards the selected input to a single output line. The selection is directed by a separate set of digital inputs known as select lines. The proposed design has 4 input line and 2 select lines and 1 output line.
                                               
* 4 : 1 MUX symbol

     ![Screenshot (14)](https://user-images.githubusercontent.com/99316485/155881919-68b36fb5-d5b0-4aa4-9e6c-29df1e99489a.png)

* Truth Table

    ![Screenshot (54)](https://user-images.githubusercontent.com/99316485/155882011-a33695fa-7a3d-4d68-ab48-5f46255ac4dd.png)

* MUX Design
    
    ![Screenshot (16)](https://user-images.githubusercontent.com/99316485/155882118-b1487bb1-d4ce-49f8-83e8-ebf1cfbc8a3a.png)
    
* MUX Test Bench

    ![Screenshot (17)](https://user-images.githubusercontent.com/99316485/155882187-c344bb9d-8d49-460d-b64b-4a4b0d4c17b5.png)
    
* MUX Wavaeform

    ![Screenshot (13)](https://user-images.githubusercontent.com/99316485/155882299-2ec5050e-c8ed-4ad7-8d2f-be2f79786034.png)

* Generated netlist

*  Generated for: PrimeSim
*  Design library name: mux
*  Design cell name: mux_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Fri Feb 25 11:44:39 2022

.global gnd!
********************************************************************************
* Library          : mux
* Cell             : mux
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt mux a b e y i0 i1 i2 i3 vdd
xm43 y net103 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm39 net103 e vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm38 net103 net98 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm36 net98 net88 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm31 net98 net78 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm30 net98 net79 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm29 net98 net80 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm25 net78 i0 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm24 net78 net105 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm23 net78 net104 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm19 net79 i1 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm18 net79 b vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm17 net79 net104 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm13 net88 i3 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm12 net88 b vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm11 net88 a vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm6 net80 i2 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm5 net80 net105 vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm4 net80 a vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm1 net105 b vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm0 net104 a vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm44 y net103 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm41 net92 net98 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm40 net103 e net92 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm35 net81 net88 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm34 net76 net80 net81 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm33 net75 net79 net76 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm32 net98 net78 net75 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm28 net67 net104 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm27 net66 net105 net67 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm26 net78 i0 net66 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm22 net58 net104 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm21 net57 b net58 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm20 net79 i1 net57 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm16 net49 a gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm15 net48 b net49 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm14 net88 i3 net48 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm9 net37 a gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm8 net33 net105 net37 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm7 net80 i2 net33 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm3 net105 b gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm2 net104 a gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
.ends mux

********************************************************************************
* Library          : mux
* Cell             : mux_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 net24 net26 net12 y net20 net18 net16 net14 net11 mux
v1 net11 gnd! dc=1.8
c7 y gnd! c=1p
v18 net12 gnd! dc=0 pulse ( 0 1.8 0 1n 1n 80u 160u )
v17 net14 gnd! dc=0 pulse ( 1.8 0 0 1n 1n 40u 80u )
v16 net16 gnd! dc=0 pulse ( 1.8 0 0 1n 1n 20u 40u )
v15 net18 gnd! dc=0 pulse ( 1.8 0 0 1n 1n 10u 20u )
v14 net20 gnd! dc=0 pulse ( 1.8 0 0 1n 1n 5u 10u )
v13 net26 gnd! dc=0 pulse ( 1.8 0 0 1n 1n 20u 40u )
v12 net24 gnd! dc=0 pulse ( 1.8 0 0 1n 1n 40u 80u )

.tran '20u' '160u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(y) v(net12) v(net14) v(net16) v(net18) v(net20) v(net24) v(net26)

.temp 25

.option primesim_output=wdf


.option parhier = LOCAL


.end

