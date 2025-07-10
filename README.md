# RTL-Design-and-Synthesis-
# Day 1 - Introduction to Verilog RTL design and Synthesis
## 1- Introduction to open-source simulator iverilog
### (i) SKY130RTL D1SK1 L1 Introduction to iverilog design test bench
#### What is simulator?
In RTL (Register Transfer Level) design, a simulator is a specialized software tool used to verify the functional correctness of digital hardware described in an HDL (Hardware Description Language) such as Verilog, SystemVerilog, or VHDL before the design is synthesized or implemented on hardware
In this workshop we'll use iVerilog
![image](https://github.com/user-attachments/assets/5d9b4fac-a304-4646-b7bb-eb770ff6aada)
#### What is test bench?
A test bench in RTL design is a special HDL (Hardware Description Language) module created to verify and validate the functionality of another module, known as the Device Under Test (DUT). The test bench applies a set of input signals (stimulus) to the DUT and checks whether the outputs produced by the DUT match the expected results, according to the design specification.
A test bench in RTL design is like a virtual testing environment for your digital circuit. Think of it as a small program, written in the same language as your design (like Verilog or VHDL), that helps you check if your circuit works correctly.
Here’s how it works in simple terms:
The test bench sends inputs (like test signals or data) to your circuit, which is called the Device Under Test (DUT).
It then watches the outputs that come out of your circuit to see if they are correct.
The test bench itself is not part of the final hardware—it’s just for testing in simulation, not for building into a chip.
![image](https://github.com/user-attachments/assets/1ecc12be-d8c3-4b08-9bf8-de33aa1ab9fc)
![image](https://github.com/user-attachments/assets/62be0587-a103-4bd4-9d6e-ed95c4159815)
## 2- Labs using iverilog and gtkwave
### (i) SKY130RTL D1SK2 L1 Lab1 introduction to lab
![image](https://github.com/user-attachments/assets/7f1bb6d4-a2a6-4923-93dd-45388a72d63b)
![image](https://github.com/user-attachments/assets/5f1e7a6a-7efd-433f-9746-71ccd6cd626e)
![image](https://github.com/user-attachments/assets/7e2f045f-b14f-4841-83e7-23fb61ab452a)
![image](https://github.com/user-attachments/assets/a1df0c01-71b7-4655-9a63-bf552317c6ce)
this verilog_files contains all the test bench and verilog source files which we'll be using in this lab. 
### (ii) SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1
verilog_files contains the design which we are going to load in iverilog. 
![image](https://github.com/user-attachments/assets/7bcfbb61-89db-4f99-8715-9c36cc979441)
Let's load a MUX into the simulator. iverilog iscommand to load.
![image](https://github.com/user-attachments/assets/c5310bb2-6166-40cb-bebc-6c0ee54180ce)
./a.out is going to dump the vcd file.Now we'll load this vcd file in simulator using gtkwave and input file.
![image](https://github.com/user-attachments/assets/97cbecba-7df9-425a-9f7d-42d822c61e6d)
![image](https://github.com/user-attachments/assets/32aac601-a227-407f-bf02-68fe8f722fa1)
![image](https://github.com/user-attachments/assets/0ffa09c7-aed3-46e5-8eb4-4a156ed46124)
Drag and drop the input and output as marked with arrow in the picture. then click on zoom fit as marked with squareto show the complete waveform. To check the trasition click on that specific signal and click on half arrow. it will show the transitions in the signal. From above picture it's clear that when select is 0 the output is = i0.
### (iii) SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2
type ctrl+c to get back to main line prompt.
![image](https://github.com/user-attachments/assets/4af238d0-5167-4771-a529-caa405d0f848)
design andtest bench program will open. let's look at the design. uut stands for unit under test. 
UUT is the central focus of simulation and verification in RTL design.
The testbench interacts with the UUT to validate its functionality before hardware synthesis.
Using a clear instance name like uut helps make testbenches easy to read and maintain.
![image](https://github.com/user-attachments/assets/c16c154b-5549-472b-9a4b-d9623b4a9a23)

![image](https://github.com/user-attachments/assets/54faabb2-d917-4108-838e-7cb8e24663eb)
## 3- Introduction to Yosys and Logic synthesis
### (i) SKY130RTL D1SK3 L1 Introduction to yosys
#### What is netlist?
A netlist is a text-based description of an electronic circuit that lists all the components (like transistors, resistors, capacitors, or logic gates) and details how they are connected to each other through electrical nodes or "nets". The netlist acts as the blueprint for the circuit’s connectivity, much like a recipe lists ingredients and how to combine them. It does not describe the physical arrangement of components, only their logical or electrical connections. 
COMPONENTS:
  U1 NAND_GATE
  U2 INVERTER

CONNECTIONS:
  U1.OUT -> U2.IN
  U2.OUT -> OUTPUT
This example shows two components and how their pins are connected, but not where they are placed.
![image](https://github.com/user-attachments/assets/066eb2b0-9c99-4bd5-8183-38cca28d7860)
netlist is the representation of the design in the form of cells present in .lib
![image](https://github.com/user-attachments/assets/d77ec7a1-70db-4957-96c4-9043e292f8af)
testbench will be same as RTL test bench.
### (ii) SKY130RTL D1SK3 L2 introduction to logic synthesis part1

RTL design stands for Register Transfer Level design. It is a fundamental step in digital circuit design, where the functionality of a digital system is described in terms of the flow of data between hardware registers and the logical operations performed on that data
How do i map the RTL to digital ckt?
![image](https://github.com/user-attachments/assets/a20fc049-2638-4e97-a262-071609bd0d76)
![image](https://github.com/user-attachments/assets/65c6d3b7-4e09-4314-ae80-af3e16deaef9)
![image](https://github.com/user-attachments/assets/dc19619c-75a4-442e-b4c7-0cb502d1b00c)
### (iii) SKY130RTL D1SK3 L3 introduction to logic synthesis part2
![image](https://github.com/user-attachments/assets/67fb34f5-06a8-4113-a16f-2527fecec2a4)
![image](https://github.com/user-attachments/assets/d9025444-0498-4e51-88d9-e5e31dd27ffe)
![image](https://github.com/user-attachments/assets/7d1c1c3a-9632-43e4-abcf-34eeffb549d6)
![image](https://github.com/user-attachments/assets/932bc9a1-e93c-42d3-873d-25d6e7c1e3a1)
## 4- Labs using Yosys and Sky130 PDKs
### (i) SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux Part1

first step is to invoke the yosys. for that we type yosys
![image](https://github.com/user-attachments/assets/1eea4477-d942-4f6f-9a40-1d5570456784)
after this we'll read the library. command for that is read_liberty -lib path
![image](https://github.com/user-attachments/assets/a3ea6401-dacf-4229-b9e6-45063eed9f5a)
![image](https://github.com/user-attachments/assets/46f1a803-c646-452f-88ac-400170cde71f)
![image](https://github.com/user-attachments/assets/07b5294f-9888-47ee-b5d4-870281c6f3b4)
abc is a command which is going to convert our RTL file to gate.When we type show it will show the graphical version of logic it has realised.
![image](https://github.com/user-attachments/assets/88296cac-baca-4b2c-b231-27ada0ba079f)
![image](https://github.com/user-attachments/assets/ec65a9d7-3b2c-4eb9-8d99-15ace3787848)
here we see the mux is completely realised in terms of sky130 library which we used. Let's see what it has done.
### (ii)SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux Part2
![image](https://github.com/user-attachments/assets/0040de5a-2c5e-4b0f-9653-c694c0e1a4c1)

#### Summary Box: 2-to-1 Multiplexer Circuit Diagram

| Block            | Function                                                                 |
|------------------|--------------------------------------------------------------------------|
| i0, i1           | Data inputs to the multiplexer                                           |
| sel              | Select input to choose between i0 and i1                                 |
| BUF (input)      | Buffers to strengthen and clean input signals                            |
| MUX (sky130...)  | Standard cell multiplexer; selects between i0 and i1 based on sel        |
| BUF (output)     | Buffer to strengthen and clean the output signal                         |
| y                | Output of the multiplexer circuit                                        |

- **Inputs (i0, i1, sel):** Enter the circuit and are buffered for signal integrity.
- **Multiplexer (MUX):** Chooses between i0 and i1 based on the select signal (sel).
- **Output (y):** The selected input, passed through an output buffer for a strong final signal.

This structure ensures reliable signal transmission and correct multiplexer operation.

[1] https://pplx-res.cloudinary.com/image/private/user_uploads/53671740/75231fd3-ae88-4412-8b95-eff4af6bba8b/photo-1.jpg
### (iii) SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux Part3
command to write netlist is write_verilog
![image](https://github.com/user-attachments/assets/3e4774bf-fa29-49f2-b5c1-4b25f4caa7ea)
now open it.
![image](https://github.com/user-attachments/assets/0ddb74a3-ed9d-4cd9-ab99-27bf4e264e57)
![image](https://github.com/user-attachments/assets/ee68edb4-c375-4a90-923b-7cad79db2c99)
we want the netlist in simple way so we modify the switch.
![image](https://github.com/user-attachments/assets/c062e052-27ad-4849-a5a2-b1ec2206ead7)
# Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles
## 1- Introduction to timing .libs
### (i) SKY130RTL D2SK1 L1 Lab4 Introduction to dot Lib part1











