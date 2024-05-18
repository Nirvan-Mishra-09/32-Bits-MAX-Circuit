
# 32-Bits-Sequential-MAX-Circuit

**Task**

This repo describes the design of a sequential MAX circuit for eight unsigned 4-bit numbers (X0..X7). The circuit takes these eight inputs and outputs the maximum among the eight numbers. The report outlines the design approach and provides a transistor-level schematic for the core sorting element.

**Block Diagram**
![image](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/ee5330bd-1eab-4891-8d4b-211680d38c4e)

**Counter Circuit**

The counter unit counts the number of clock cycles (at each rising edge), the unit is built using a 1 bit register, that is constructed using D flip flop. 

_Truth Table_

Truth Table for D Flip Flop

![Truth Table for D Flip Flop](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/c55dcb61-1ac2-4f9b-a4ff-eea1492bbdf2)

Truth Table for 2 bit counter

![Truth Table for 2 bit counter](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/be84f948-dcc9-4002-af34-3123519268f5)


_Counter Circuit in Cadence Virtuoso_

![counter diagram](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/c0a2a0a9-c39c-4f3e-b546-7ba461d2e894)

_Counter Waveform_

![counter_waveform](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/8567cc75-8fe5-41ed-9426-d42ffc38ef9b)

**Data Selector Circuit**

The data selector module is essential to the data selection process because it provides inputs to the sorter unit. It receives two inputs, Q0 and Q1, which are obtained from the counter output and operate on a clock cycle basis. The sorter unit then carefully examines these inputs to determine which one has a higher value. The output of the higher value is then forwarded by the sorter unit.

![image](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/24fccd99-0727-47e2-bcae-f442250635ff)

Circuit for boolean expression "a":

![a](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/40e2107b-2fe6-4bbc-8f12-6fa8ae4eb80f)

Circuit for boolean expression "b":

![b drawio](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/e726bbbe-e172-4d6c-afec-c1b100888bf1)

_Data Selector_

![data_selector](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/ff5b25fe-41bc-415b-834b-1d3aeb6b242c)

**Memory File**

A 4-bit memory file constructed with D flip-flops (DFFs) operates as a fundamental component in digital systems, facilitating the storage and retrieval of binary data. Each DFF within the memory file represents one bit of the overall memory capacity. When reset is high (1), all D flip-flops within the memory file are set to 0. When the reset signal is asserted, it triggers the DFFs to reset to their default state, setting all bits to 0. Subsequently, as data is inputted into the memory file each D flip-flop stores one bit of the binary data. For instance, let’s denote the D flip-flops as DFF0, DFF1, DFF2, and DFF3, representing the four bits of the memory file. The data input lines are labeled D0, D1, D2, and D3 respectively, and the output lines are Q0, Q1, Q2, and Q3. When new data is presented to the memory file, it’s synchronized with the clock signal, causing the D flip-flops to latch the input data. Upon the rising edge of the clock, the data on the D input of each flip-flop is transferred to its output, thereby preserving the stored information until the next clock cycle.

_Memory Schematic_

![Memory_schematic](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/91e0b255-bb92-42b0-bd8b-506de485b9f2)

_1 bit DFF_

![dff_block drawio](https://github.com/Nirvan-Mishra-09/32-Bits-Sequential-MAX-Circuit/assets/127642231/8aee98d3-992d-4a23-ad80-25a560e43962)
