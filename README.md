# Design-and-implementation-of-4-1-MUX on CMOS 28nm technology
# Table of Contents
* [Introduction](https://github.com/Atri21/Design-and-implementation-of-4-1-MUX/blob/main/README.md#introduction)
* [Tools Used](https://github.com/Atri21/Design-and-implementation-of-4-1-MUX/blob/main/README.md#tools-used)
* [Working](https://github.com/Atri21/Design-and-implementation-of-4-1-MUX/blob/main/README.md#working)
* [Netlist](https://github.com/Atri21/Design-and-implementation-of-4-1-MUX/blob/main/README.md#generated-netlist)
* [Acknowledgements](https://github.com/Atri21/Design-and-implementation-of-4-1-MUX/blob/main/README.md#acknowledgements)
* [References](https://github.com/Atri21/Design-and-implementation-of-4-1-MUX/blob/main/README.md#refrences)

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

[4-1-MUX-netlist](https://github.com/Atri21/4-1-MUX-netlist/tree/main#4-1-mux-netlist)

# Author
Shiva Kumar S, Sapthagiri College Of Engineering, Bangalore

# Acknowledgements

* Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
* Synopsys Inc
* IIT Hyderabad
* https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/
* Sameer Durgoji, NIT Karnataka
* Chinmay Panda, IIT Hyderabad

# Refrences 

[1] Wei-Yu Tsai and Ching-Te Chiu “ANovel Low Gate-Count Pipeline Topologywith Multiplexer Flip-Flops for Serial LinkIEEE Transactions on Circuits and Systems:Regular Papers, VOL.59, No. 11, Nov. 2012

[2] M. Alioto and G. Palumbo, “Interconnectawaredesign of fast large fan in CMOSmultiplexers,” IEEE Trans. Circuits Syst. II,Exp. Briefs, vol. 54, no.6, pp. 484-488, Jun2007
