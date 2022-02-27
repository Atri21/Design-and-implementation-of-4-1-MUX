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

* 4 : 1 MUX Truth Table

    ![Screenshot (54)](https://user-images.githubusercontent.com/99316485/155882011-a33695fa-7a3d-4d68-ab48-5f46255ac4dd.png)




Device Characterization
Circuit Design
Simulation Results
Performance Comparison
Conclusion
Author
Acknowledgements
References
Introduction
Mixers find wide use in communication applications especially in up and down converter analog font ends. New applications such as Radio Frequency Integrated Circuits (RFIC) require low-power, low-cost single chip designs. This repository presents the design and simulation of Gilbert cell based mixer on CMOS 28nm technology. The design has been created on Synopsis Custom Compiler software and simulated using PrimeWave environment.
![Screenshot (16)](https://user-images.githubusercontent.com/99316485/155881010-28d7fdbd-edb8-4445-ac2b-021fb75965b0.png)



Fig 1. Mixer schematic

Fig 1. shows the mixer schematic, consisting of a folded Gilbert cell. Here the local oscillator's (LO) differential input is fed to M1-M2 and M3-M4 pairs which act as transconductance amplifiers. The output current of both amplifiers is summed with opposite polarity and passed through load resistors R_L to produce the differential output voltage. The transconductance of both amplifiers can be varied by varying the currents I_1 and I_2. This is achieved with current mirror formed using FET’s M7-M9 and M8-M10 controlled using the differential pair (M5-M6). The Radio Frequency (RF) signal is applied to this differential pair M5-M6, hence modulating the gain for the LO signal. The use of current mirror results in larger output voltage swing and ease of biasing.
