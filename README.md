
# 32-Bits-Sequential-MAX-Circuit

**Task**

This repo describes the design of a sequential MAX circuit for eight unsigned 4-bit numbers (X0..X7). The circuit takes these eight inputs and outputs the maximum among the eight numbers. The report outlines the design approach and provides a transistor-level schematic for the core sorting element.

**Block Diagram**
![image](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/ee5330bd-1eab-4891-8d4b-211680d38c4e)

_Counter Circuit_

The counter unit counts the number of clock cycles (at each rising edge), the unit is built using a 1 bit register, that is constructed using D flip flop. 

_Truth Table_

![image](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/c55dcb61-1ac2-4f9b-a4ff-eea1492bbdf2)

![counter diagram](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/c0a2a0a9-c39c-4f3e-b546-7ba461d2e894)
