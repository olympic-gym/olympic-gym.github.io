---
layout: post
title:  "SIM forensics"
date:   2021-02-28 00:2:00 +0200
subtitle: "Forensics analysis on SIM card"
background: "/img/bg1.png"
---

## Table of Content
[Overview](#overview)   
[Hardware](#hardware)   
[Acquiring Data](#acquiring-data)   
[Data Analysis](#data-analysis)   
## Overview
SIM stands for Subscriber Identity Module which is a piece of hardware with Integrated Circuit (IC) builtin. Each SIM card contains Unique identification number, network operator code, personal user key (PUK), security code and encryption algorithms. SIM can store 250 contancts and 52 messages. SIM data capacities range from 8KB to 256KB
## Hardware
<img src="/img/SIM Forensics/index.jpg" alt="X-ray image" width="800" height="440">
### Components   
1. Processor   
2. RAM   
3. ROM   
4. EEPROM   
5. File system   
<img src="/img/SIM Forensics/sim_card_hardware.jpg" alt="SIM card pins" width="800" height="440">
6. Pins   
a. Vcc: The supply voltage pin of the SIM. Modern SIM cards supports the 5V, 3V, 1.8V DC power.   
b. RESET: used to reset the SIM card signal and communications. Using this pin will make the SIM in default mode resetting all the current signals. The RESET pin is activated by the mobile devices or the SIM card upon required. Generally, SIM users are given less permission to use this function.   
c. Clock: It provides the SIM with a clock signal for its processor. The clock is derived or inherited from the mobile or the hardware.   
d. GND/Ground: It is the standard reference voltage. We usually called ground the low voltage point. As SIM is small electronic hardware with Integrated Circuit, it also has a common reference point, and hence this pin is named the ground. GND now completes the circuit for the proper functioning of the SIM card.   
e. Vpp: Earlier, this pin is used to carry the extra voltage required to write or erase the data in the memory of the SIM card, but now it is not entirely useful as the Vcc does this work.   
f. Input/Output: It is used to read and write the SIM card data from mobile phones. It is a half-duplex communication pin acting as a data transfer pin.   
## Acquiring Data
As forensics analyst
## Data Analysis
