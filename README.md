# RTL-Design-and-Synthesis-
# Day 1 - Introduction to Verilog RTL design and Synthesis
##  Introduction to open-source simulator iverilog
### SKY130RTL D1SK1 L1 Introduction to iverilog design test bench
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
##  Labs using iverilog and gtkwave
###  SKY130RTL D1SK2 L1 Lab1 introduction to lab
![image](https://github.com/user-attachments/assets/7f1bb6d4-a2a6-4923-93dd-45388a72d63b)
![image](https://github.com/user-attachments/assets/5f1e7a6a-7efd-433f-9746-71ccd6cd626e)
![image](https://github.com/user-attachments/assets/7e2f045f-b14f-4841-83e7-23fb61ab452a)
![image](https://github.com/user-attachments/assets/a1df0c01-71b7-4655-9a63-bf552317c6ce)
this verilog_files contains all the test bench and verilog source files which we'll be using in this lab. 
### SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1
verilog_files contains the design which we are going to load in iverilog. 
![image](https://github.com/user-attachments/assets/7bcfbb61-89db-4f99-8715-9c36cc979441)
Let's load a MUX into the simulator. iverilog iscommand to load.
![image](https://github.com/user-attachments/assets/c5310bb2-6166-40cb-bebc-6c0ee54180ce)
./a.out is going to dump the vcd file.Now we'll load this vcd file in simulator using gtkwave and input file.
![image](https://github.com/user-attachments/assets/97cbecba-7df9-425a-9f7d-42d822c61e6d)
![image](https://github.com/user-attachments/assets/32aac601-a227-407f-bf02-68fe8f722fa1)
![image](https://github.com/user-attachments/assets/0ffa09c7-aed3-46e5-8eb4-4a156ed46124)
Drag and drop the input and output as marked with arrow in the picture. then click on zoom fit as marked with squareto show the complete waveform. To check the trasition click on that specific signal and click on half arrow. it will show the transitions in the signal. From above picture it's clear that when select is 0 the output is = i0.
### SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2
type ctrl+c to get back to main line prompt.
![image](https://github.com/user-attachments/assets/4af238d0-5167-4771-a529-caa405d0f848)
design andtest bench program will open. let's look at the design. uut stands for unit under test. 
UUT is the central focus of simulation and verification in RTL design.
The testbench interacts with the UUT to validate its functionality before hardware synthesis.
Using a clear instance name like uut helps make testbenches easy to read and maintain.
![image](https://github.com/user-attachments/assets/c16c154b-5549-472b-9a4b-d9623b4a9a23)

![image](https://github.com/user-attachments/assets/54faabb2-d917-4108-838e-7cb8e24663eb)
## Introduction to Yosys and Logic synthesis
###  SKY130RTL D1SK3 L1 Introduction to yosys
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
### SKY130RTL D1SK3 L2 introduction to logic synthesis part1

RTL design stands for Register Transfer Level design. It is a fundamental step in digital circuit design, where the functionality of a digital system is described in terms of the flow of data between hardware registers and the logical operations performed on that data
How do i map the RTL to digital ckt?
![image](https://github.com/user-attachments/assets/a20fc049-2638-4e97-a262-071609bd0d76)
![image](https://github.com/user-attachments/assets/65c6d3b7-4e09-4314-ae80-af3e16deaef9)
![image](https://github.com/user-attachments/assets/dc19619c-75a4-442e-b4c7-0cb502d1b00c)
### SKY130RTL D1SK3 L3 introduction to logic synthesis part2
![image](https://github.com/user-attachments/assets/67fb34f5-06a8-4113-a16f-2527fecec2a4)
![image](https://github.com/user-attachments/assets/d9025444-0498-4e51-88d9-e5e31dd27ffe)
![image](https://github.com/user-attachments/assets/7d1c1c3a-9632-43e4-abcf-34eeffb549d6)
![image](https://github.com/user-attachments/assets/932bc9a1-e93c-42d3-873d-25d6e7c1e3a1)
## Labs using Yosys and Sky130 PDKs
### SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux Part1

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
### SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux Part2
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
### SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux Part3
command to write netlist is write_verilog
![image](https://github.com/user-attachments/assets/3e4774bf-fa29-49f2-b5c1-4b25f4caa7ea)
now open it.
![image](https://github.com/user-attachments/assets/0ddb74a3-ed9d-4cd9-ab99-27bf4e264e57)
![image](https://github.com/user-attachments/assets/ee68edb4-c375-4a90-923b-7cad79db2c99)
we want the netlist in simple way so we modify the switch.
![image](https://github.com/user-attachments/assets/c062e052-27ad-4849-a5a2-b1ec2206ead7)
# Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles
##  Introduction to timing .libs
### SKY130RTL D2SK1 L1 Lab4 Introduction to dot Lib part1

In this session we'll have walkthrough our library.
![image](https://github.com/user-attachments/assets/19991893-cba2-4fea-82b8-b1e453779fcd)
to remove the red colour type:syn off
tt stands for typical. Process, temperature and voltage variation will determine how my silicon will work.
25 tells the temperature and 1v8 indicates the voltage.
### SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part2
esc+ :se nu to display line number.
### SKY130RTL D2SK1 L3 Lab4 Introduction to dot Lib part3
esc + 🆚
to search anything- esc+:/keyword(whatever the keyword is) for eg if keyword is xxxxxand2_0 then simply use :/.*and2_0
esc+:/area
![image](https://github.com/user-attachments/assets/878e1b41-534c-4d9d-8d7c-fe4d7557502b)
![image](https://github.com/user-attachments/assets/136d379d-0ae4-4ab4-ba7c-c8705726fddd)
wider cell more power consumption but delay wise it willbe less.
## 2-Hierarchical vs Flat Synthesis
### SKY130RTL D2SK2 L1 Lab05 Hier synthesis flat synthesis part1
![image](https://github.com/user-attachments/assets/0da7fe9f-9573-4aa5-ac32-7293cec873d9)
module 1 is or gate. module 2 is and gate. multiple module is instantiating the sub module 1 & 2.
![image](https://github.com/user-attachments/assets/2fc1056c-9156-4e04-b373-072abed148fb)
![image](https://github.com/user-attachments/assets/6f844e34-d616-47ac-8905-24b4cd2c258a)
after this launch yosys.
![image](https://github.com/user-attachments/assets/8751ae3e-815e-4101-a41d-8b0f02438162)
![image](https://github.com/user-attachments/assets/fdd31f74-c644-4d6f-88d4-626e2960318b)
![image](https://github.com/user-attachments/assets/430bdfd5-1500-43ef-b381-8905d8fad671)
![image](https://github.com/user-attachments/assets/a55e859a-fca0-4bd8-844a-97178814b986)
![image](https://github.com/user-attachments/assets/56852e6d-70de-44fc-ba54-3eb45827852d)
![image](https://github.com/user-attachments/assets/fe9be37d-5d31-4831-b9ac-02122d8d1a87)
![image](https://github.com/user-attachments/assets/ca16428d-3677-4f3c-a13e-f67bc7c3c53a)
ideally we expect And and OR gate to show but it's not like that.
![image](https://github.com/user-attachments/assets/06e82f92-b2dc-4e94-aab8-3b9c48ed8f89)
![image](https://github.com/user-attachments/assets/45ff7089-2fe7-4192-9d3f-fff89cbf5fc9)
we expected to infer OR gate downward of AND gate. But due to Demorgan's theorem 
![image](https://github.com/user-attachments/assets/c7cb4386-31a1-45c0-8c57-a1175ab691eb)
stacked pmos is always bad because pmos has poor mobility. 
### SKY130RTL D2SK2 L2 Lab05 Hier synthesis flat synthesis part2
![image](https://github.com/user-attachments/assets/1e9fa8e4-54db-4bbf-ac96-bad151a0a583)
![image](https://github.com/user-attachments/assets/6595c05f-8ea6-43f8-a947-858f6a538896)
![image](https://github.com/user-attachments/assets/f9995c08-0005-452d-955f-c3e666b075ab)
now exit yosys and again open yosys.
![image](https://github.com/user-attachments/assets/2bab6162-acbc-4016-ac71-cee512cc6daa)
![image](https://github.com/user-attachments/assets/78f9c310-3199-4b09-a309-2b018a75fab3)
![image](https://github.com/user-attachments/assets/247967b1-314e-4eed-943c-7fc28541b31a)
![image](https://github.com/user-attachments/assets/a4ba2cac-c515-42f9-b4a8-a2283d6edfea)
![image](https://github.com/user-attachments/assets/8ad0696c-49ca-4fcb-b631-d4bdc494e584)
We see only 1 AND gate in the diagram. we are not seeing submodule 2.

## Various Flop Coding Styles and optimization
### SKY130RTL D2SK3 L1 Why Flops and Flop coding styles part1
We will study here how to code a flop and what are the different possible flops available.
Why do we need Flops, We know when there is a combinational circuit and there is input signal given there will be "Glitch" at the output. For many combinational circuits there will be further more glitches.And for continuous combinational circuits the output will never settle down, it will be always glitchy. To avoid this we need an element to store the value, it is called "FLOP".

We will use the flops in between the combinational circuit to stabilize the output even after the glitches, the output of the flop will remain constant. This is the main purpose of using flops in digital circuit.
Also we need to initialize the flops for that we have 'Set' and 'Reset' which can be Synchronous and Asynchronous.

<img width="1028" height="537" alt="image" src="https://github.com/user-attachments/assets/8dccbd5b-c6ae-4bcb-8f88-f50d0fdb2daf" />

### SKY130RTL D2SK3 L2 Why Flops and Flop coding styles part2
<img width="1037" height="493" alt="image" src="https://github.com/user-attachments/assets/79819ed8-65f0-46d4-901b-fb899e2a5b98" />

Understanding D Flip-Flop with Asynchronous and Synchronous Reset

##  Understanding D Flip-Flop with Asynchronous and Synchronous Reset

Let’s break down the Verilog code for a D Flip-Flop (`dff_asyncres_syncres`) that supports both **asynchronous** and **synchronous** resets.

###  Module Declaration

```verilog
module dff_asyncres_syncres (...);
```
- Declares a module named `dff_asyncres_syncres`.

###  Inputs and Outputs

- **Inputs:**
  - `clk` – Clock signal
  - `async_reset` – Asynchronous reset signal
  - `sync_reset` – Synchronous reset signal
  - `d` – Input data to the flip-flop

- **Output:**
  - `q` – Output of the flip-flop (declared as `reg` since it’s assigned in an `always` block)

###  Always Block Trigger

```verilog
always @(posedge clk or posedge async_reset)
```
- This block is **sensitive to**:
  - A **rising edge of the clock** → for synchronous actions
  - A **rising edge of `async_reset`** → for immediate (asynchronous) reset
- Used in designs that require both async and sync control

###  Reset and Data Logic

```verilog
if (async_reset)
    q  `sync_reset` > data assignment                           |

This structure is commonly used in digital design where an immediate reset (such as power-up reset) is critical, along with a controlled (clocked) reset for system behavior.


### SKY130RTL D2SK3 L3 Lab flop synthesis simulations part1


![image](https://github.com/user-attachments/assets/092ef44f-224f-45a8-a3eb-ec2ba519ce03)
![image](https://github.com/user-attachments/assets/ec086fae-c919-42f5-8452-e60890eea172)

![image](https://github.com/user-attachments/assets/77891de2-cc9e-4618-a47c-aec6634de09e)


### (iv) SKY130RTL D2SK3 L4 Lab flop synthesis simulations part2
Now let's synthesize the following D flipflops

D FlipFlop with Asynchronous reset
D FlipFlop with Synchronous reset
D FlipFlop with Synchronous and Asynchronous reset
D FlipFlop with Asynchronous set

1) D FlipFlop with Asynchronous reset
Why We Use dfflibmap in Synthesis Flow?

When performing logic synthesis using tools like Yosys, we typically use a standard cell library (.lib file) that contains both combinational and sequential cells (like D flip-flops). However, in many design flows, flip-flops are provided in a separate library from the main logic gates.

To handle this, we use the Yosys command:

dfflibmap -liberty ../lib/your_flipflop_library.lib
What dfflibmap Does?

It maps generic D flip-flop constructs (like always @(posedge clk) in RTL) to specific standard cells in the library.
This is essential for correct technology mapping — otherwise, the tool may not know which flip-flop cell to use.
It ensures timing-aware synthesis using the correct sequential elements.
![image](https://github.com/user-attachments/assets/8b898372-2a8a-4bab-beae-454e1033434c)
![image](https://github.com/user-attachments/assets/88cacab1-ef82-4c82-b38e-5913a734b96c)
![image](https://github.com/user-attachments/assets/e8c3f90d-1051-4629-bb32-baacd98d5ded)
![image](https://github.com/user-attachments/assets/f0aa10bb-8ce1-4503-ae20-1ef0e06c851f)
What we Wrote in Verilog:

In your Verilog code, you wrote:
if (reset)

    q <= 0;
    
This means:

👉 "When reset is high (1), set q to 0."

This is called active-high reset — it works when the signal is 1.

What’s in the Standard Cell Library:

But the flip-flops in the standard cell library are designed like this:

👉 "When reset is low (0), set q to 0."

This is called active-low reset — it works when the signal is 0.
The Problem:

we wrote an active-high reset,
but the hardware cells available only support active-low reset.
So they don’t match.

What the Tool Does:
To fix this mismatch, the synthesis tool automatically adds an inverter like this

reset --> [Inverter] --> reset_n --> Flip-Flop (active-low reset)

Now, when your reset signal is 1:

 the inverter turns it into 0,
 which correctly triggers the flip-flop with an active-low reset.

![image](https://github.com/user-attachments/assets/2698a3e1-2ebf-42c3-ab8b-096e33dfe4fd)
![image](https://github.com/user-attachments/assets/df9a4900-29a0-4a81-9713-2638f3766323)
What is dfflibmap in Yosys?

dfflibmap is a command used during synthesis in Yosys to map flip-flops in your RTL design to actual flip-flop cells available in the standard cell library.

Why is it Important?
1. Connects RTL to Real Hardware
In your Verilog, you write generic D flip-flops like:

always @(posedge clk) begin

  if (reset)
  
    q <= 0;
    
  else
  
    q <= d;
    
end

"dfflibmap finds matching flip-flops from the standard cell library"

The dfflibmap command goes to your library file (like sky130_fd_sc_hd__tt_025C_1v80.lib),

and looks for flip-flops that can do the same job — for example, a D flip-flop triggered on a rising edge.

dfflibmap finds matching flip-flops from the standard cell library (like sky130_fd_sc_hd__dfxtp_1) and replaces the generic one with it.
 What is Tech Mapping?
"Technology mapping" means:
➡ Taking your high-level logic (like a & b, if-else, or flip-flops)

➡ And replacing it with real, physical logic gates and cells that exist in a standard cell library (like the SKY130 library).

What Does abc Do?
abc is the tool in Yosys that:

Optimizes your logic

Replaces combinational logic (AND, OR, NOT, MUX, etc.)

With real gates from the library (like NAND2, NOR3, etc.)

But here's the catch:

❌ abc can only handle combinational logic.
✅ It does not understand flip-flops (sequential logic).

Problem Without dfflibmap
If your code has a D flip-flop like this:

always @(posedge clk)
  q <= d;

Yosys knows it's a flip-flop, but abc can’t do anything with it —
It will skip it, because abc doesn't know how to map flip-flops.

What dfflibmap Does:
dfflibmap solves this by:

Looking inside the standard cell library

Finding a real flip-flop cell (like sky130_fd_sc_hd__dfxtp_1)

Replacing your Verilog flip-flop (from the always block)
with the actual hardware flip-flop cell

Now the flip-flop part is already mapped to real hardware.

So abc can now:

Safely ignore the flip-flops (they are already mapped)

Focus on mapping and optimizing the remaining combinational logic.

#### D FlipFlop with Synchronous reset

![image](https://github.com/user-attachments/assets/b27fc2b3-a173-4c96-b8fb-07c6b646563a)
![image](https://github.com/user-attachments/assets/b429cee9-1a12-4b84-b370-703278097aa5)

### (v) SKY130RTL D2SK3 L5 Interesting optimisations part1


![image](https://github.com/user-attachments/assets/7d7839d0-7f1b-4035-9708-ea952cb23417)
![image](https://github.com/user-attachments/assets/b3c3ca1c-dd80-4323-9b98-309d9917b22e)

![image](https://github.com/user-attachments/assets/532bbe13-aebe-4f91-a6fb-36a1fd1bf170)
![image](https://github.com/user-attachments/assets/a030acdc-53e8-4ea5-a214-871f1a559d00)
![image](https://github.com/user-attachments/assets/4bbeb23c-e093-42b7-a15c-13bd58119ef0)
![image](https://github.com/user-attachments/assets/1c78997b-4fe7-466c-90f5-d865ab7ca239)

![image](https://github.com/user-attachments/assets/80cabd66-1ba0-431a-92b2-e6f7d1c5dde3)

So instead of generating a multiplier, the tool simply wires the bits accordingly — no actual multiplier hardware is required.

This is a classic strength reduction optimization applied during synthesis.

### (vi) SKY130RTL D2SK3 L6 Interesting optimisations part2

<img width="900" height="568" alt="image" src="https://github.com/user-attachments/assets/777df45f-91ac-444f-9e33-3ba94872f64c" />

Multiplication by 

2^n= shift left by n bits

Left Side:
a * 9 = a * (8 + 1)
→ broken into:
y = (a << 3) + a;

This avoids using a multiplier circuit and instead uses:

One shift

One adder

Which are cheaper and faster in RTL.

Right Side Illustration:
Shows the structure:

a000   → a shifted by 3 → a * 8

a * 9 = a * (8 + 1)
      = (a * 8) + a
      
Multiplying by 8 is very easy in hardware — just shift a to the left by 3 bits (same as adding 3 zeros to the right).

So:
a * 8 → shift a left by 3 bits → like a000

Then just add a to that shifted value.

Example:
Let’s say a = 3'b101 (which is 5 in decimal):

a * 8 = 5 * 8 = 40

Add a again: 40 + 5 = 45

y = a * 9 = 45

But you did it using:

1 shift

1 addition

No big multiplier needed!

Why This is Useful in RTL Design:
In digital hardware (like chips or FPGAs):

Multipliers take more space and power

Shifts and additions are fast and easy


<img width="1298" height="727" alt="image" src="https://github.com/user-attachments/assets/0811372c-8498-4a3b-ab43-2f96306f3758" />

Reading and Analyzing the Design

Top module: \mul2
Yosys is analyzing your Verilog file and finds that the top module is called mul2.

Printing Design Stats

Number of wires: 2
Number of wire bits: 7
Number of public wires: 2
Number of public wire bits: 7
Number of memories: 0
Number of cells: 0

This shows:

we have 2 wires, using a total of 7 bits

No memories, no processes

0 cells means no logic gates or flip-flops have been added yet.

Found and reported 0 problems means No syntax or structural issues in your design. 

ABC Mapping (Technology Mapping)

yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
This command tries to map your logic to real gates (NAND, AND, etc.) using the standard cell library.

BUT...

Extracted 0 gates and 0 wires to a netlist network with 0 inputs and 0 outputs.
Don't call ABC as there is nothing to map.

This means:
Yosys couldn’t find any actual logic (like adders, multipliers, or gates) to map.
So there’s nothing for ABC to optimize or translate into hardware.

<img width="1395" height="507" alt="image" src="https://github.com/user-attachments/assets/def7f527-d1d0-458f-b284-9d29b5b535db" />

<img width="1837" height="1042" alt="image" src="https://github.com/user-attachments/assets/d0f51613-887e-479f-954c-c64d8f6e23d8" />

<img width="1841" height="1030" alt="image" src="https://github.com/user-attachments/assets/f479e617-759e-41c2-b285-2c2fc2dd4b7e" />

 What's Being Shown in the .dot Graph Window?
This is a graphical representation of your RTL logic.

🔹 Design Name: mult8
Input: a

Output: y

Logic in middle: 2x 2:0 - 5:0

 What does 2x 2:0 - 5:0 mean?
This is shorthand for:
y = a * 8

Explanation:

a[2:0] → a 3-bit input

a * 8 → means shifting a left by 3 bits (since 2³ = 8)

So your logic is simply:
assign y = a << 3;
And:

y[5:0] → 6-bit output

 This confirms what Yosys is showing: you're multiplying a 3-bit number a by 8 to get a 6-bit number y.

 Why “Number of cells = 0” in the terminal?
Because shifting left (a << 3) is a wiring operation, not actual computation:

Hardware doesn't need gates for it

It's just connecting the right bits to the right output pins

So Yosys does not create any logic gates (AND, OR, MUX, etc.).

<img width="1840" height="930" alt="image" src="https://github.com/user-attachments/assets/85d87b7c-d3a9-4fb4-9d11-f80deb826cc8" />

<img width="1791" height="958" alt="image" src="https://github.com/user-attachments/assets/4b56ce33-eb35-460b-bc43-715879c7c214" />

💡 What’s happening here?
🔹 input [2:0] a;
This declares a 3-bit input named a.
Example: if a = 3'b101, it represents the number 5.


🔹 output [5:0] y;
This declares a 6-bit output named y.
Why 6 bits? Because you're multiplying a (3 bits) by 8, which can produce up to a 6-bit result.

🔹 assign y = {a, a};
This is the key line. It's using Verilog concatenation.

{a, a}

This means:
→ take the bits of a and stick them next to themselves.
So if a = 3'b101 (which is 5 in decimal), then:

{a, a} = {3'b101, 3'b101} = 6'b101101 = 45 (decimal)

But this isn’t a real multiplication.

Instead, it’s just doubling the bits.

But here, Yosys is smart — it optimized your code y = a * 8 to y = {a, 3'b000} (which is the same as shifting a left by 3 bits), and further simplified it to:

y = {a, a};

This was safe because it gets the same result for what your logic wanted — a multiplication by 8.

## Day 3 - Combinational and sequential optmizations

## 1- Introduction to optimizations

### (i) SKY130RTL D3SK1 L1 Introduction to optimisations part1

#### Combinational Logic Optimization

# Combinational Logic Optimisation Explained

## What Is Combinational Logic Optimisation?

Combinational logic optimisation is the process of refining digital circuits to achieve the most efficient design. The main goals are to reduce the **area** (the number of gates or components used) and **power consumption** of the logic circuit, making it more cost-effective and energy-efficient.

## Key Concepts

### 1. Squeezing the Logic
- **Purpose:** To minimize the number of gates and the complexity of the logic.
- **Benefits:** 
  - **Area savings:** Fewer components are needed, reducing the physical size of the circuit.
  - **Power savings:** Less hardware means lower power consumption.

### 2. Constant Propagation
- **Definition:** This is a direct optimisation technique where constant values (0 or 1) are substituted into the logic circuit wherever possible.
- **How it works:** If a part of the circuit always receives a constant input, it can be simplified or removed entirely, making the design more efficient.

### 3. Boolean Logic Optimisation
- **Goal:** To simplify Boolean expressions that define the logic circuit.
- **Techniques:**
  - **Karnaugh Map (K-Map):** A graphical tool used to simplify Boolean expressions by grouping terms to eliminate variables.
  - **Quine-McCluskey Method:** A tabular method that systematically reduces Boolean functions to their simplest form, suitable for computer implementation.

## Why Optimise?

- **Improved Performance:** Simpler circuits can operate faster.
- **Lower Cost:** Fewer components mean reduced manufacturing costs.
- **Energy Efficiency:** Optimised logic uses less power, important for battery-powered and large-scale systems.

## Summary Table

| Optimisation Technique  | Description                                      | Benefit                  |
|------------------------|--------------------------------------------------|--------------------------|
| Squeezing the Logic    | Minimizing logic gates and complexity            | Area & power savings     |
| Constant Propagation   | Replacing variables with constants               | Direct simplification    |
| K-Map                  | Graphical Boolean simplification                 | Easy for small circuits  |
| Quine-McCluskey        | Systematic tabular Boolean simplification        | Suitable for automation  |

By applying these optimisation techniques, digital designers can create circuits that are faster, smaller, and more energy-efficient.
<img width="1286" height="707" alt="image" src="https://github.com/user-attachments/assets/6408bfaf-b2cd-4bb1-b2fe-c399aec88971" />

Constant Propagation Example Explained
This image demonstrates constant propagation, a digital logic optimization technique that simplifies circuits when some inputs are fixed at constant values.

Original Logic Circuit
Inputs: A, B, C

<img width="610" height="82" alt="image" src="https://github.com/user-attachments/assets/b00b607a-ebc5-415c-b7cc-939bf612d996" />

Gate Structure:

First, A and B are ANDed.

The result is ORed with C.

The output is inverted (NOT gate).

Applying Constant Propagation
Given: A is tied to 0 (grounded).
 <img width="507" height="122" alt="image" src="https://github.com/user-attachments/assets/96c64ead-6fed-4f1b-9995-573191da0c4b" />

Result: The entire circuit simplifies to a single NOT gate with input C.

Impact on Circuit Design

Transistor Count: Reduced from 6 to 2.

Area & Power: Both are reduced due to fewer components.

Simplicity: The logic is easier to analyze and faster to operate.

<img width="1288" height="717" alt="image" src="https://github.com/user-attachments/assets/8d466dab-cee9-4181-8f1d-2ee3d36dc447" />

Key Takeaways
Complex logic can often be reduced to simple gates using Boolean algebra.

The original nested conditional logic is equivalent to just an XOR gate between a and c.

Benefits of optimisation:

Fewer gates: Only one XOR gate needed.

Lower power and area: Simpler hardware implementation.

Faster operation: Less propagation delay.

### (ii) SKY130RTL D3SK1 L2 Introduction to optimisations part2

<img width="1326" height="752" alt="image" src="https://github.com/user-attachments/assets/68b0c861-013a-468b-87e2-4bc73c698842" />

This diagram demonstrates how constant propagation in sequential circuits allows for significant simplification. When certain inputs are fixed, the entire logic path can often be replaced with a constant output, making the circuit more efficient.


What Is Happening in the Circuit?
1. Constant Propagation in Sequential Logic
The D flip-flop's D input is tied to a constant value (grounded, meaning D = 0).

Reset (RST) is also shown as active, which forces the output 
Q to 0.

This means, regardless of the clock, the flip-flop will always output 0.

2. Logic Gate Simplification
The output 

<img width="475" height="171" alt="image" src="https://github.com/user-attachments/assets/8d889350-7709-45a4-9713-8434600f2d0d" />

### (iii) SKY130RTL D3SK1 L3 Introduction to optimisations part3

<img width="1298" height="740" alt="image" src="https://github.com/user-attachments/assets/dd24b794-5664-4ab1-b5f6-c35f6f0b3e18" />

| Technique                | Key Features / Description                             | Applications                 | Advantages                         | Challenges / Disadvantages        |
|--------------------------|--------------------------------------------------------|------------------------------|-------------------------------------|-----------------------------------|
| State Optimization       | Removes unused or redundant FSM states                 | Finite state machines (FSMs) | Simplifies logic, reduces area      | May not be feasible for all FSMs  |
| Cloning (Physical Aware) | Duplicates logic for optimal physical placement        | Large-scale digital circuits | Reduces wire delay, improves speed  | Increases area if overused        |
| Retiming                 | Moves registers to balance combinational delays        | Sequential digital circuits  | Enables higher clock frequency      | Requires careful timing analysis  |

Technique Explanations
State Optimization:
This process analyzes the state transition diagram of a finite state machine (FSM) to eliminate unnecessary or equivalent states. The result is a simpler FSM with fewer logic gates, which reduces the area and power consumption of the circuit.

Cloning (Physical Aware):
Cloning involves duplicating logic elements or registers and placing them closer to where they are needed in the physical layout of a chip. This minimizes the length of interconnect wires, reducing signal delay and improving the overall speed of the circuit. However, excessive cloning can increase the chip area.

Retiming:
Retiming is the process of repositioning registers (flip-flops) within a sequential circuit to balance the delays of combinational logic between them. This can significantly improve the maximum clock frequency by minimizing the longest (critical) path, but it requires detailed timing analysis to ensure functional correctness.

These techniques are essential for optimizing digital designs, making them faster, more efficient, and cost-effective.

## 2- Combinational logic optimizations 

### (i) SKY130RTL D3SK2 L1 Lab06 Combinational Logic Optimisations part1

<img width="1837" height="1021" alt="image" src="https://github.com/user-attachments/assets/c427222a-8a65-4366-8155-3271d4a0e7b8" />
Listing files with opt in the name:
ls *opt*

This command lists all files in the current directory whose names contain opt.

📄 You got:

counter_opt2.v, multiple_module_opt2.v, opt_check2.v, etc.

Testbenches like: tb_opt_check3.v

<img width="1831" height="951" alt="image" src="https://github.com/user-attachments/assets/11dee40f-2c06-48fc-8f7c-0c37034ed6a8" />

 Step-by-Step Breakdown
1. Started Yosys
   This opens the Yosys shell, where you can run synthesis commands interactively.

2. Load Liberty File
   
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

This loads the standard cell library (like a catalog of real hardware components).

 Output says: Imported 418 cell types

 These are logic gates, flip-flops, etc., available for your synthesized design.

3. Load Verilog RTL Design

read_verilog opt_check.v

Loads your RTL file named opt_check.v.

Parses it and generates an internal RTL representation.

 Output: Successfully finished Verilog frontend.
4. Run Synthesis
synth -top opt_check

<img width="1871" height="971" alt="image" src="https://github.com/user-attachments/assets/fd5b2f98-3d6a-4c47-9c49-7c353cb46e89" />

 "opt_clean -purge" is like saying:
“Delete everything that’s not being used — no mercy!”


<img width="1830" height="935" alt="image" src="https://github.com/user-attachments/assets/2733133a-3415-4ad4-aa79-70eec2cdb6e7" />
<img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/c4953632-54e4-487e-9210-0f89857ab094" />

from above image we were expecting AND gate. Same can be seen in gvim. 

Now let's read another verilog file.

<img width="1828" height="977" alt="image" src="https://github.com/user-attachments/assets/67d31528-50f7-4ed6-86c9-bf43ffffdc37" />

<img width="1838" height="942" alt="image" src="https://github.com/user-attachments/assets/a4dd248f-542d-4086-927a-2257b4a18201" />
we were expecting OR gate and we got the same.
<img width="978" height="495" alt="image" src="https://github.com/user-attachments/assets/49d06874-bda1-43cf-a87e-9f7aa1bbe927" />

### (ii) SKY130RTL D3SK2 L2 Lab06 Combinational Logic Optimisations part2

<img width="1300" height="587" alt="image" src="https://github.com/user-attachments/assets/9a4e7eab-8284-4dbf-9169-1b61d280a93e" />

<img width="1839" height="1013" alt="image" src="https://github.com/user-attachments/assets/4a4414da-dfe3-4ea1-aa4b-d807c4d5a774" />

we were expecting 3 input AND gate and we got the same.

## 3- Sequential logic optimizations
### (i) SKY130RTL D3SK3 L1 Lab07 Sequential Logic Optimisations part1

<img width="1821" height="350" alt="image" src="https://github.com/user-attachments/assets/0f22de63-5632-475b-8c7a-d9e7b808b3cd" />

 gvim dff_const1.v -o dff_const2.v
This command opens two files side-by-side in gvim (a graphical version of Vim):

dff_const1.v (the source file)

dff_const2.v (another file for comparison or editing)

The -o option means "open horizontally split windows" so you can view and compare/edit them together.

Why is this useful?
When working on variations of D flip-flop designs, it helps to:

Reuse structure from a previous version (dff_const1.v)

Modify it slightly to create a new version (dff_const2.v)

Compare logic for debugging or analysis

<img width="1827" height="915" alt="image" src="https://github.com/user-attachments/assets/25ce9860-654c-4dc1-8013-3d2a7666d054" />

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/f4fa89bd-e31c-4e0a-95f6-6768ce72adbe" />


<img width="1913" height="1078" alt="image" src="https://github.com/user-attachments/assets/16f27a89-ac40-44d7-804a-24ce6adc4549" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a375776b-47ed-47de-9cbc-e1114d2cdcb1" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/aa8932c8-dd44-4c86-80a3-594f2ab09269" />

Let's see what happens when we synthesize it.
dfflibmap is not a Verilog command; it’s a step in the design process.

It makes sure your design uses real, manufacturable flip-flops.

This step is necessary before you can physically make your chip.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/32160b89-40a6-449f-b326-7fa296fe0f55" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bb0a711c-c715-400b-82a8-533045b0bdd8" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e40f75cb-3bdc-4b38-95d0-7ce2e9faf86a" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1c4104c9-eb50-4a29-b8a0-c60e0de82fe1" />


### (ii) SKY130RTL D3SK3 L2 Lab07 Sequential Logic Optimisations part2

Sagar divohti

### (iii) SKY130RTL D3SK3 L3 Lab07 Sequential Logic Optimisations part3

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d80372b1-41db-4005-aa23-4181293fc868" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d72d25b1-0d2d-42d8-a064-a29f2ad6ae5c" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2ce28da4-fb11-4b7a-8e17-01e04a1c308c" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cbaf4144-c213-4866-b6de-722abbdf0d86" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/247710ea-bf54-4707-a97d-3efce87a7e29" />
The previous case when we did the show without the abc. we saw both simply connected to reset. 
Our expectation was the below diagram and we go the same.
<img width="1272" height="543" alt="image" src="https://github.com/user-attachments/assets/383a4ce0-eeaf-43c5-875a-05f1d7383908" />

## 4- Sequential optimzations for unused outputs

### (i) SKY130RTL D3SK4 L1 Seq optimisation unused outputs part1
we'll seeunused output optimization

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1c8133e1-4f12-4125-8206-0fe00d1b691f" />

<img width="1305" height="741" alt="image" src="https://github.com/user-attachments/assets/d392294e-5515-46f8-93f5-900b3320c605" />
the above ckt is our demand.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5f0ae897-5f7e-4039-b9f4-b60e21ae79c4" />
inabove picture we can see it is inferring only one d flip flop.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/484597ae-f4dd-43c9-9418-e126511a0cf5" />
we cn see there is only oneflip flop in above picture.


### (ii) SKY130RTL D3SK4 L2 Seq optimisation unused outputs part2

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3571c96a-fd34-4f3b-a43f-38351d3499f8" />

follow the same steps to open gvim of Counter_opt2

<img width="1160" height="566" alt="image" src="https://github.com/user-attachments/assets/b78920b2-066b-4129-945c-f16161ef00b3" />
complete from sagar di vohti

# Day 4 - GLS, blocking vs non-blocking and Synthesis-Simulation mismatch

## 1- GLS, Synthesis-Simulation mismatch and Blocking/Non-blocking statements

### (i) SKY130RTL D4SK1 L1 GLSConceptsAndFlowUsingIverilog

Introduction to Gate Level Simulation (GLS)
When we write RTL code, we verify its functional correctness using a testbench. This process is known as RTL simulation.

In Gate Level Simulation, we run the same testbench, but instead of simulating the RTL code, we simulate the netlist — the gate-level version of the design generated after synthesis.

Why GLS is Needed
Logical Verification After Synthesis Although the netlist is functionally equivalent to the RTL, synthesis tools may perform optimizations. GLS ensures that no logical errors were introduced during synthesis.

Timing Verification RTL simulation is functional but does not model actual delays. GLS helps verify that the timing constraints are met, especially when run with delay annotation (typically from SDF files). This ensures that the circuit works as expected at the target clock frequency.

Key Points
Testbench Compatibility: Since the netlist has the same ports as the RTL, it fits directly into the RTL testbench without changes.

Timing-Accurate Simulation: With delay annotation, GLS reflects the real-world delays caused by gates, wires, and interconnects.

Summary
Gate Level Simulation is the step where:

We validate the post-synthesis design.
Ensure logical correctness.
Check timing with annotated delays.
All using the same testbench written for RTL.
It serves as the final check before proceeding to physical design or fabrication.

### Gate Level Simulation (GLS) using Icarus Verilog (iverilog)

<img width="3840" height="2160" alt="image" src="https://github.com/user-attachments/assets/c87e7edc-aff8-4ebe-a760-78467a4fa48d" />

Components in the Setup:
Design This is the synthesized netlist, which contains only logic gates.

Gate Level Verilog Models These define the behavior of standard cells (like AND, OR, DFF, etc.). They are essential because the netlist uses gate-level primitives, and iverilog needs to understand their functionality during simulation.

Testbench Provides stimulus to the design and checks the outputs. The same testbench used for RTL simulation can be reused, since the netlist ports match those of the RTL.

iverilog Compiles the testbench, the synthesized gate-level netlist, and the gate-level Verilog models. It generates a VCD file (Value Change Dump), which records the transitions of signals during simulation.

gtkwave This tool is used to visualize the signal waveforms from the VCD file. It helps in analyzing the behavior of the design over time.

Key Note (from the Diagram)
If the gate-level models are delay-annotated, then Gate Level Simulation can be used for timing validation, in addition to logic verification.

Important Point
The netlist alone is not sufficient for simulation — it does not describe the internal behavior of gates.
Gate-level models must be included so that iverilog can understand and simulate the logic elements used in the netlist.

Conclusion
Gate Level Simulation using iverilog ensures:

Functional correctness after synthesis.
Timing verification (if delays are annotated).
A clear path from RTL to hardware by simulating exactly what was synthesized.

### (ii) SKY130RTL D4SK1 L2 Synthesis Simulation Mismatch

Synthesis-Simulation Mismatch

Missing Sensitivity List

Blocking vs non blocking assignments

Non standard verilog coding

1) Missing Sensitivity List
Issue Overview:
This is a common source of simulation and synthesis mismatch in Verilog designs. The simulator responds to activity or changes on signals. If a signal is not listed in the sensitivity list of an always block, then changes in that signal will not trigger re-evaluation of the block during simulation.

<img width="2010" height="2050" alt="image" src="https://github.com/user-attachments/assets/9b54b2e9-f882-4dc7-8bc9-495c46538e92" />

module mux (
    input i0, input i1,
    input sel,
    output reg y
);

always @(sel)  // Incorrect sensitivity list
begin
    if (sel)
        y = i1;
    else
        y = i0;
end

endmodule

In this code:

The always block is only sensitive to sel.

If i0 or i1 changes while sel remains constant, the block is not re-evaluated.

As a result, y does not reflect the changes in i0 or i1, even though it should.

This causes the output y to appear static or incorrectly held, which resembles latch-like behavior.

It behaves as a latch instead of MUX.


Simulator vs Synthesis Behavior:

Simulator behaves based on signal changes. Since i0 and i1 are not in the sensitivity list, their changes are ignored.

Synthesis tools, however, infer the correct multiplexer logic because they analyze the complete logic structure.

This results in a mismatch: the synthesized hardware behaves correctly, but the simulated output does not.

Corrected Code:

always @(*)  // Correct sensitivity list

begin

    if (sel)
    
        y = i1;
        
    else
    
        y = i0;
        
end

Using @(*) instructs the simulator to automatically include all right-hand side signals (sel, i0, i1) in the sensitivity list.

This ensures that the always block is evaluated whenever any of the involved signals change, leading to correct and expected simulation behavior.

### (iii) SKY130RTL D4SK1 L3 Blocking And NonBlocking Statements In Verilog

Blocking (=) vs Non-blocking (<=) Assignments in Verilog
1. Inside an always block:
Blocking (=): Executes statements sequentially — each statement blocks the next until it's done. This models combinational logic or procedural code flow.

Non-blocking (<=): All right-hand side (RHS) expressions are evaluated in parallel at the start of the time step, and the values are assigned to the left-hand side (LHS) at the end of the time step. This models sequential logic (flip-flops).

2. Caveats with Blocking Assignments in Sequential Logic
Let’s analyze two versions of the code provided:

Correct Use of Blocking (Modeling Two DFFs):

module code (
    input clk,
    input reset,
    input d,
    output reg q
);

reg q0;

always @(posedge clk, posedge reset)
begin
    if (reset)
    begin
        q0 = 1'b0;
        q = 1'b0;
    end
    else
    begin
        q = q0;
        q0 = d;
    end
end

endmodule

In the else block:

q = q0; is executed first

Then q0 = d; is executed

Since q gets the previous value of q0, this mimics two separate flip-flops:

q0 stores d

q stores the previous q0

This correctly models two D flip-flops.


Incorrect Ordering – Leads to Single Flip-Flop:

module code (
    input clk,
    input reset,
    input d,
    output reg q
);

reg q0;

always @(posedge clk, posedge reset)
begin
    if (reset)
    begin
        q0 = 1'b0;
        q = 1'b0;
    end
    else
    begin
        q0 = d;
        q = q0;
    end
end

endmodule

In this version:

q0 = d; is executed before

q = q0; — now q just copies d because q0 was already updated.

So both q and q0 carry the same value → only one flip-flop inferred.

This leads to incorrect synthesis where only one DFF is inferred, despite needing two.

Best Practice:
Use non-blocking (<=) for sequential logic (in always @(posedge clk) blocks).
Use blocking (=) only for combinational logic (in always @(*) blocks).

This ensures clarity in simulation and synthesizes accurate and intended hardware.

### (iv) SKY130RTL D4SK1 L4 Caveats With Blocking Statements

Version 1 – With Non-blocking Assignments

module code (
    input clk,
    input reset,
    input d,
    output reg q
);

reg q0;

always @(posedge clk or posedge reset)
begin
    if (reset)
    begin
        q0 <= 1'b0;
        q <= 1'b0;
    end
    else
    begin
        q <= q0;
        q0 <= d;
    end
end

endmodule


Explanation:

When non-blocking assignments (<=) are used, both q <= q0; and q0 <= d; are evaluated in parallel. The right-hand side (RHS) values are captured first, and the assignments happen at the end of the clock edge.

Therefore:

q receives the previous value of q0
q0 receives the new value of d
This infers two D flip-flops:

One for storing d (q0)
One for storing q0 (q)
This properly represents a two-stage pipeline.

### Version 2 – Reversed Assignment Order

module code (
    input clk,
    input reset,
    input d,
    output reg q
);

reg q0;

always @(posedge clk or posedge reset)
begin
    if (reset)
    begin
        q0 <= 1'b0;
        q <= 1'b0;
    end
    else
    begin
        q0 <= d;
        q <= q0;
    end
end

endmodule

Explanation:

Although the order of statements is reversed, non-blocking assignments ensure correctness.

Both RHS expressions are evaluated before any assignment:

q0 gets the current value of d
q gets the previous value of q0
This again infers two flip-flops, and the behavior is consistent with expected pipeline logic.

Conclusion:
Using non-blocking assignments (<=) in sequential logic:

Ensures the right number of flip-flops are inferred.

Maintains logical correctness regardless of statement order.

Prevents unintended synthesis mismatches.

Leads to clean simulation results and consistent behavior across design tools.

This is the recommended style for writing clocked logic in Verilog.

### synthesis-simulation mismatch

The code you provided illustrates a synthesis-simulation mismatch caused by using blocking assignments (=) in the wrong order.

Objective:
Implement the logic: y = (a | b) & c That is, the output of an OR gate with inputs a and b is connected to one input of an AND gate, and c is the other input.

### Version 1 – Incorrect Order (Causes Mismatch)

module code (
    input a, b, c,
    output reg y
);

reg q0;

always @(*)
begin
    y = q0 & c;   // Uses old value of q0
    q0 = a | b;   // New value computed after y
end

endmodule

Problem:
y is computed before q0 is updated.

Since blocking assignments execute sequentially, q0 still holds the previous value when used in y = q0 & c.

In simulation, this behaves as though q0 is a register or flip-flop, even though there's no clock — this is not synthesizable as intended.

Synthesis tools will still treat q0 as combinational, leading to a mismatch between simulation and synthesized hardware.


### Version 2 – Correct Order

module code (
    input a, b, c,
    output reg y
);

reg q0;

always @(*)
begin
    q0 = a | b;   // Compute q0 first
    y = q0 & c;   // Then use q0 to compute y
end

endmodule

Explanation:
Here, q0 is assigned before it is used to compute y.

Since this is combinational logic and uses blocking assignments in the correct order, the circuit will simulate and synthesize correctly.

The synthesized circuit will now have:

One OR gate computing q0 = a | b

One AND gate computing y = q0 & c

This matches the intended logic y = (a | b) & c.

Best Practice: When using blocking assignments in combinational always @(*) blocks, always ensure the data dependencies are ordered correctly. Alternatively, avoid intermediate variables if not needed, or write the logic in a single expression.

## Labs on GLS and Synthesis-Simulation Mismatch

### (i) SKY130RTL D4SK2 L1 Lab GLS Synth Sim Mismatch part1

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4a5df2fa-b409-42c4-9659-2e2f66c8bb6f" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d5d04673-173a-458f-8fc5-1b0802e97ace" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/778640be-d980-43ac-9da3-ebaa3b6faa4a" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/209d39cd-4227-40e7-ba65-4a61fe3e2011" />

Invoke yosys after gtkwake command.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e096dfd3-3b3c-4577-9944-fb81f3079134" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b1c1fb1d-d7cb-469b-818b-47e1c3b208f1" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8e2a664f-3fbd-42b2-aab8-fbfcf0ffb8d2" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/94f8fcca-cd24-47d4-87cd-797fd06ce34d" />


### (ii) SKY130RTL D4SK2 L2 Lab GLS Synth Sim Mismatch part2

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f0e6776a-c02f-4562-83dd-3e35722ef194" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f26da0c3-c172-4784-b563-319d522f1a65" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e34905ed-9eda-4c47-8038-31726e815348" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5ce632b3-5c46-4a69-ae02-57c14c0b0ad9" />

<img width="1037" height="512" alt="image" src="https://github.com/user-attachments/assets/d9d004be-6477-459d-934e-213991b912b3" />

The GLS shows a proper functionality of an MUX, but still our simulation and GLS are not the same hence we see a Simulation Mismatch. I'm attaching below our previous simulation so that we can easily see the difference.

<img width="1031" height="530" alt="image" src="https://github.com/user-attachments/assets/51874aae-885f-436a-b756-bb337caaeedf" />

### Simulating, Synthesizing and Gate Level Synthesis of good_mux and comparing the waveforms

<img width="1032" height="521" alt="image" src="https://github.com/user-attachments/assets/8621e67e-8257-4575-8bcd-636fdd615730" />


<img width="1028" height="515" alt="image" src="https://github.com/user-attachments/assets/372f03fd-87fb-4fd7-9339-7f9d15243eb2" />

<img width="1031" height="507" alt="image" src="https://github.com/user-attachments/assets/4a3cf08b-daf1-4b40-bd26-5d02a46cbc8b" />

<img width="1022" height="473" alt="image" src="https://github.com/user-attachments/assets/b6fcf64b-b938-4789-9d70-f39584039e99" />

<img width="1020" height="498" alt="image" src="https://github.com/user-attachments/assets/a2d78a3f-b5d7-47ac-b0b2-d2affe150d63" />

<img width="1032" height="492" alt="image" src="https://github.com/user-attachments/assets/396d33a8-0c6a-424e-b362-7c471d100d7d" />

<img width="1026" height="487" alt="image" src="https://github.com/user-attachments/assets/f6081cac-8675-4352-87cc-bbb960e5d960" />

<img width="1031" height="512" alt="image" src="https://github.com/user-attachments/assets/80cd2762-e60c-46f1-98d7-94fcefb7e453" />

<img width="1027" height="512" alt="image" src="https://github.com/user-attachments/assets/23711b74-0140-4442-bc36-573a64be9981" />

<img width="1032" height="511" alt="image" src="https://github.com/user-attachments/assets/c49397d3-0f0a-43a4-921b-219d0b780f8b" />


## Labs on synth-sim mismatch for blocking statement

## (i) SKY130RTL D4SK3 L1 Lab Synth sim mismatch blocking statement part1

#### Incorrect Version (Simulation-Synthesis Mismatch)

<img width="1035" height="491" alt="image" src="https://github.com/user-attachments/assets/1d2d4a67-6dcc-4b57-a9ec-b7cd2b0260e5" />

module blocking_caveat ( 
    input a, b, c,
    output reg d 
);

reg x; 

always @(*)

begin

    d = x & c;   //  Uses old value of x
    
    x = a | b;   // x is updated *after* d is computed
    
end

endmodule

<img width="1033" height="535" alt="image" src="https://github.com/user-attachments/assets/8c9f10ae-77c0-4516-bb49-fd6c63a69b72" />

Problem:

In a blocking assignment (=), the operations are executed in order, like software instructions.

Here, d is assigned before x is updated, so it uses the old or garbage value of x.

In simulation, this will cause d to produce incorrect results.

In synthesis, the tool might optimize and connect the logic correctly, causing a mismatch between simulation and real hardware.

#### Correct Version (Proper Combinational Logic)

module blocking_caveat ( 
    input a, b, c,
    output reg d 
);

reg x; 

always @(*)

begin

    x = a | b;   //  Compute x first
    
    d = x & c;   //  Then use x to compute d
    
end

endmodule


Why This is Correct:

x is computed before being used in d.

This ensures that d always uses the updated value of x.

Simulation behavior will match synthesis, and the logic will behave as intended.

Now let's simulate the module blocking_caveat and see if the output is as expected.

### Simulation and Synthesis of blocking_caveat followed by GLS

<img width="1032" height="507" alt="image" src="https://github.com/user-attachments/assets/b85765b8-50d7-48fd-90fc-5d9e63ee1678" />

<img width="1027" height="498" alt="image" src="https://github.com/user-attachments/assets/09c59090-f53f-4777-abcf-95f2dfcfe27c" />

The marked point in the waveform is not following d = (a | b) & c; because x, which is (a | b), is storing old values.

Now, let's do the synthesis, generate our netlist and perform GLS and verify the results.

<img width="1036" height="493" alt="image" src="https://github.com/user-attachments/assets/91ea30d4-fcc5-4496-964c-275000ae3059" />

<img width="1017" height="511" alt="image" src="https://github.com/user-attachments/assets/835235e6-91b9-4748-ac8a-d5792d76e59f" />


<img width="1026" height="428" alt="image" src="https://github.com/user-attachments/assets/f62ba9f0-9808-4f19-82dd-be817a367432" />

<img width="1022" height="500" alt="image" src="https://github.com/user-attachments/assets/fcf15129-f369-4c10-8965-6978843a9658" />

<img width="1037" height="502" alt="image" src="https://github.com/user-attachments/assets/80b97d2e-0eac-4394-9d83-ef94a7b4796c" />

<img width="1025" height="513" alt="image" src="https://github.com/user-attachments/assets/6514e2ff-de06-4826-8577-03d38adea898" />

<img width="1027" height="498" alt="image" src="https://github.com/user-attachments/assets/70010bc0-f77c-404e-b2ca-d0be9e5270a8" />


The marked point in the waveform is following d = (a | b) & c

I'm attaching below our previous simulation so that we can easily see the difference.

<img width="1028" height="477" alt="image" src="https://github.com/user-attachments/assets/a61acfd5-4ee3-453b-9af5-bf08ab55856b" />

So we can clearly Synthesis simulation mismatch due to blocking statements.

# Optimization in Synthesis

## If Case constructs
### (i) Sky130RTL D5SK1 L1 IF CASE Constructs part1

Here we will see about 'IF' and 'CASE' statements and danger with 'CASE' statements.

if:
It gives the priority logic

Evaluates sequentially: top-to-bottom priority

Syntax:
if (condition)
 begin
     statement;
 end
else (condition)
 begin
     statement;
 end

 <img width="437" height="356" alt="image" src="https://github.com/user-attachments/assets/3a1dbf7a-3f61-44db-bafb-f56746bba960" />

Danger/Caution with 'if': Called as "Inferred latches" We don't intend to put a latch, but this happens because of bad coding. Comes with incomplete "if" statement.

e.g.
if (condition1)
    y=a;
else if (condition2)
    y=b;
end
# There is no "else" condition specified
Now if condition1 not happens and condition2 also not happens then the hardware will remain incomplete. Therefore the tool will try to Latch. It is very dangerous and should be avoided.
<img width="373" height="340" alt="image" src="https://github.com/user-attachments/assets/f53032e2-5e3c-41b4-902b-68d9ef958bf1" />

### (ii) Sky130RTL D5SK1 L2 IF CASE Constructs part2

Let us take an example of a Counter;
always @ (posedge clk, posedge reset)
 begin
   if (reset)
          count <= 3'b00;
   else if (en)
          count <= count + 1;
 end
# although it is incomplete code but it is correct

Let' look at the hardware. (Always look for the harware).
When the 'enable' pin is ON, the counter is count+1 but when it is OFF, counter latches the value to previous value. So this is intended behaviour.

Inferred Latches is fine for Sequential Circuits, but not fine for Combinational circuits.

<img width="421" height="347" alt="image" src="https://github.com/user-attachments/assets/317b121a-49fa-4117-b6ab-cde39d4e243a" />

### Case :
'if' and 'case' are assigned inside always block; they should be assigned under reg value.

Used to implement multi-way branching, like a switch-case in C.

Good for implementing multiplexers, state machines, and decoders.

All case branches are evaluated simultaneously (unlike if).

You should always include a default case to avoid unintended latch inference.

 always @(sel or c1 or c2)
begin
  case (sel)
      2'b00: out = c1;
      2'b01: out = c2;
      default: out = 1'b0;
  endcase
end

<img width="291" height="277" alt="image" src="https://github.com/user-attachments/assets/53892139-20f1-4d50-b0cc-f4530246da60" />

Caveats with case:
1) Incomplete case --> Lead to "Inferred Latches" e.g.
   reg [1:0] sel ; 
always @(*) 
begin
 case (sel)
     2'b00: begin
         out = c1;
     end
     2'b01: begin
         out = c2;
     end
 endcase
end
# rest of the pins will be latched to the output

<img width="307" height="267" alt="image" src="https://github.com/user-attachments/assets/13ce8976-9358-45dd-a57d-2d2aba1d52c0" />

To avoid this we write code case with default
reg [1:0] sel ;
always @(*) 
begin
 case (sel)
     2'b00: begin
         out = c1;
     end
     2'b01: begin
         out = c2;
     end
     default: begin
         out = 1'b0;
     end
 endcase
end
 with deafult we avoid inferred latches

When using a case statement in Verilog to assign values to multiple outputs, you must assign values to all outputs in every case branch.
If any output is missing an assignment, the synthesis tool may infer a latch to "remember" the previous value. This is usually unintended and can cause incorrect hardware behavior.

 Bad Example (Partial Assignment – Latch Inferred)
 
always @(*) begin
  case (sel)
  
    2'b00: begin
    
      out1 = 1;
      
      // Missing assignment for out2
    end
    
    2'b01: begin
    
      out1 = 0;
      
      out2 = 1;
      
    end
    
    default: begin
    
      out1 = 0;
      
      // Missing assignment for out2 again
      
    end
    
  endcase
end


Problem:
out2 is not assigned in all the cases.

Synthesis tool will create a latch to preserve the previous value of out2 — this is not desired in combinational logic.

✅ Good Example (Fully Assigned – No Latch)

*reg [1:0] sel;
reg x, y;

always @ (*)

 begin
 
    case (sel)
    
        2'b00: begin
        
           x = a;
           
           y = b;
           
        end
        
        2'b01: begin
        
           x = c;
           
        end
        
        default: begin
        
           x = d;
           
           y = b;
           
        end
        
    endcase
    
 end*
 
We have assigned the value for select line '0', but when select line is '1' only value for x is assigned and not y.

Partial assignment leads to inferred latches.

<img width="312" height="370" alt="image" src="https://github.com/user-attachments/assets/850411f4-364c-419f-85ad-1e4325c73de2" />

## Labs on "Incomplete If Case"

### (i) Sky130RTL D5SK2 L1 Lab Incomplete IF part1

We will see how the synthesis and simulator behaves when there is "incomplete if and case".

Our files required here are inside *incomp*

<img width="1031" height="430" alt="image" src="https://github.com/user-attachments/assets/376d376a-fdf7-47ae-b07a-f790e2f9a8a0" />

We will open all the files; gvim *incomp* -o and start with "incomplete if";

<img width="1035" height="491" alt="image" src="https://github.com/user-attachments/assets/7eee8c16-6705-41b2-9f6b-198cbcdf1f12" />

Let us look at the harware, here if always translates into a 'Mux'. So here select line is i0, if we i0 is '1' output is 1 but else part is missing so i0 = 0, it will be latched.
<img width="356" height="257" alt="image" src="https://github.com/user-attachments/assets/05ec5230-50f1-4b5c-829f-b597a4f129c7" />

The behaviour of this mux is similar to D-latch which latch enable as i0. It's a poselatch. Whenever i0 is present i1 is seen on y, whenever absent it latches on to it's value.

<img width="253" height="192" alt="image" src="https://github.com/user-attachments/assets/43dab7a3-c604-4e3d-9481-5ac052ea8804" />

Simulation

iverilog incomp_if.v tb_incomp_if.v

./a.out

gtkwave tb_incomp_if.vcd

<img width="1031" height="462" alt="image" src="https://github.com/user-attachments/assets/26875659-b8f1-4558-be48-6aa8e91203d4" />

Synthesis

yosys

read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

read_verilog incomp_if.v

synth -top incomp_if

abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

show

<img width="980" height="469" alt="image" src="https://github.com/user-attachments/assets/f1ec753a-b941-4cc9-8c54-21c6ea0fd221" />

<img width="502" height="416" alt="image" src="https://github.com/user-attachments/assets/4175488d-be8e-4147-a362-0da07a870308" />

### (ii) Sky130RTL D5SK2 L2 Lab Incomplete IF part2

Considering the hardware, it has two mux where else past is missing, so it will latch as shown below.

<img width="477" height="267" alt="image" src="https://github.com/user-attachments/assets/e970ca4d-6a85-4702-8f7c-c1423cb1c5c2" />

It will represent a D-latch where EN is when any of i0 and i2 can exist, so it will be ORed. At the input there will be a combined circuit of the multiplexer with values of i0, i1, i2 and i3.

<img width="732" height="347" alt="image" src="https://github.com/user-attachments/assets/2d6a9fbd-3aa1-469e-923e-2f5a390b7448" />

<img width="1002" height="482" alt="image" src="https://github.com/user-attachments/assets/e7dec92b-c7cd-44d3-af4c-4754e2292622" />

We can see whenever i0 = 1--> Output 'y' is following i1.

When i0 = 0 --> it looks towards i2:

When i2 is low --> output is constant

when i2 is high --> output starts following i3

Now let's synthesize:

<img width="1027" height="413" alt="image" src="https://github.com/user-attachments/assets/d82daf35-b737-4282-a13c-cf9bf76e663a" />

## Lab on "Incomplete overlapping case"

### (i) Sky130RTL D5SK3 L1 Lab Incomplete overlapping Case part1

Here we will discuss about the "case" statements labs in detail.

Let's open all the required files; gvim comp_case.v -o incomp_case.v -o partial_case_assign.v -o bad_case.v.

<img width="1032" height="508" alt="image" src="https://github.com/user-attachments/assets/bafadffe-803f-4f40-b665-1dd48b00170b" />

First, we will look into incomp_case.v

<img width="1032" height="492" alt="image" src="https://github.com/user-attachments/assets/34dfbb3f-05d1-4c78-8b23-dbf3c10e46ef" />

According to the code it is clear that if 'select' is '00', i0 will be selected and for select line '01' i1 will be selected. But for '10' and '11' there is no input and also default statement is missing, so it will latch. Also the enabling condition for latch is sel[1]'.

<img width="337" height="272" alt="image" src="https://github.com/user-attachments/assets/431a5792-d418-47f8-8074-a4158703d1fe" />

The logic we are expecting is a D-latch, when the select[1] is '0' the output is same as input, but when selct[1] is '1' the output is latched.

<img width="721" height="352" alt="image" src="https://github.com/user-attachments/assets/305bd7fa-fe1c-4ce9-a4a4-f00ca007bcde" />

Let us do the functional simulation:

iverilog incomp_case.v tb_incomp_case.v

./a.out

gtkwave incomp_case.vcd

<img width="1027" height="496" alt="image" src="https://github.com/user-attachments/assets/f702c667-03fe-4ed1-860b-92362d5bb2fa" />

When select is '00' y is following i0

When select is '01' y is following i1

The moment select is becoming '11' or '10', y is latching to that value.

Let us now to the synthesis:

yosys

read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

read_verilog incomp_case.v

synth -top incomp_case

abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

show

<img width="1037" height="502" alt="image" src="https://github.com/user-attachments/assets/9f195b64-5f98-4340-b2a8-089a3a6e0f10" />


<img width="1032" height="410" alt="image" src="https://github.com/user-attachments/assets/dc36dfdf-2745-473d-88ce-8bbb7b30226f" />

### (ii) Sky130RTL D5SK3 L2 Lab Incomplete overlapping Case part2

Now we will look into the complete case; comp_case.v file. We can see here everything is same except that we added default.

<img width="1031" height="501" alt="image" src="https://github.com/user-attachments/assets/896d5b7a-5181-4865-9e2f-7a56cb90094b" />

Simulation We can see when select is '10' or '11' it is exactly following i2. There is no latching action.

<img width="994" height="477" alt="image" src="https://github.com/user-attachments/assets/84e56f7c-3d82-4c67-b1fd-1d2b3a7eee40" />


Upon synthesis we can see that there is no latch present.

<img width="996" height="422" alt="image" src="https://github.com/user-attachments/assets/28ddb71f-9ccf-42bf-98b2-d35ee41c7b92" />

Let us look at the partial_case_assign.v file as well.

<img width="1037" height="497" alt="image" src="https://github.com/user-attachments/assets/dc071a75-8c26-4ee0-8edb-b61f0d67c5ce" />

### (iii) Sky130RTL D5SK3 L3 Lab Incomplete overlapping Case part3

let us synthesis partial_case_assign.v
<img width="1028" height="497" alt="image" src="https://github.com/user-attachments/assets/b892da16-fbf0-43e4-8ac2-5e9d285b1da2" />
We can see here in the path of 'y' there is no latch but in the path of 'x' there is a latch.

<img width="1031" height="457" alt="image" src="https://github.com/user-attachments/assets/d3b695b6-fa89-430f-af83-8dad46f7e6ef" />

Let us see bad_case.v file.
In 'case' statements there can be execution of two logics at the same time which casues mismatch if there is a bad case.

<img width="1035" height="492" alt="image" src="https://github.com/user-attachments/assets/a3e13466-8e26-43c7-ba8c-f59bdeb15597" />


Here, for 2'b10 i2 is assigned and for input 2'b1? i3 is assigned. So simulator will try to execute both at the same time. Simulations will be getting confused with each other.

<img width="1032" height="503" alt="image" src="https://github.com/user-attachments/assets/a304cff2-6c7a-430c-8f29-6b767daa04c7" />

We can clearly see when the select is '11' the output is getitng latched, the simulator is not able to decide the output, it is getting confused whar to execute.

### (iv) Sky130RTL D5SK3 L4 Lab Incomplete overlapping Case part4

Since the code is code is complete, we will not ahve an inferred latch here but we are having problem with execution as it is a bad case.

Let us Synthesize the code:

  yosys

  read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

  read_verilog bad_case.v

  synth -top bad_case

  abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

  write_verilog -noattr bad_case_net.v

  show

  After synthesis we can observe that there are no latches as we expected.

  <img width="1027" height="501" alt="image" src="https://github.com/user-attachments/assets/8f53a2b3-7200-4df9-9627-63d65c0ff261" />

 read the standard cell models, netlist and the test bench
iverilog ../my_lib/verilog_model_primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v bad_case_net.v tb_bad_case.v

./a.out

gtkwave tb_bad_case.vcd

<img width="1033" height="398" alt="image" src="https://github.com/user-attachments/assets/f8a28a9f-a73c-467c-b9a1-d742273c2ca0" />

Now we can see that at select line '11' it is not constant and behaving as i3. Hence there is no latching action here.


<img width="1033" height="506" alt="image" src="https://github.com/user-attachments/assets/13bfffab-c988-4e87-a78b-1d4676915566" />

## for loop and for generate

### Sky130RTL D5SK4 L1 For Loop and For Generate part1


## Difference Between `for` Loop (Behavioral) and `generate for` Loop (Structural) in Verilog

Here’s a comparison in tabular form:

| Feature                  | `for` Loop (Behavioral)                              | `generate for` Loop (Structural)                    |
|--------------------------|------------------------------------------------------|-----------------------------------------------------|
| Usage Context            | Inside procedural blocks (`always`, `initial`, etc.) | At the module level, outside procedural blocks      |
| Purpose                  | Repeats actions sequentially at simulation time      | Instantiates multiple blocks/wires at elaboration   |
| Interpretation           | Executes statements on each loop iteration           | Expands code during compilation/elaboration         |
| Synthesis                | May or may not be synthesizable (depends on logic)   | Always synthesizable for creating repetitive logic  |
| Example Code             | `for (i=0; i<N; i=i+1) a[i] = b[i] & c[i];`          | `genvar i; generate for (i=0; i<N; i=i+1) ... endgenerate` |
| When Runs                | During simulation (run-time)                         | During elaboration (before simulation/synthesis)    |
| Use Case                 | Manipulating variables, writing testbenches, etc.    | Generating repeated hardware structures (e.g., adders, registers) |
| Variable Type            | Uses regular integers (e.g., `integer i;`)           | Uses `genvar` special variable type                 |

### Key Points

- **Behavioral `for` loops** describe actions performed in time and are used *within* procedural (sequential) code blocks.
- **`generate for` loops** define actual structural hardware duplication during elaboration, creating multiple instances of logic in the hardware design.

This distinction is fundamental in writing correct and synthesizable Verilog code and is essential for digital hardware design.

Example: For Loop

2:1 mux

always @(*) begin

 case (sel)
 
    1'b0 : y = i0;
    
    1'b1 : y = i1;
    
 endcase
 
end



4:1 mux

 always @(*) begin
 
  case (sel)
  
     3'b00 : y = i0;
     
     3'b01 : y = i1;
     
     3'b10 : y = i2;
     
     3'b11 : y = i3;
     
  endcase
  
 end



 32:1 mux
 
always @(*) begin

 case (sel)
 
    5'b00000 : y = i0;
    
    5'b00001 : y = i1;
    
    5'b00010 : y = i2;
    
    5'b00011 : y = i3;
    
    .
    
    .
    
    .
    
    5'b1111 : y = i31;
    
 endcase
 
end


But we can't write big codes like this, this is where the power of "Blocking statements" comes into picture. A blocking statement in Verilog is a type of procedural assignment that executes sequentially, just like C-style code. It uses the = assignment operator.

Let us take the example of 32:1 mux;

#### assumption: input 32:1 bus

integer i

always @ (*)

 begin
 
   for(i = 0; i < 32; i = i+1) begin
   
     if(i==sel)
     
     y = inp[i];
     
  end
  
end

Therefore it is easy and short to implement 32:1 mux or even bigger muxes using for loop.

### Sky130RTL D5SK4 L2 For Loop and For Generate part2

Example: 1:8 DEMUX Using Behavioral for Loop
Let's consider a 1:8 demultiplexer (DEMUX) example.

Inputs:

ip → Input signal

sel (3 bits) → Select line

Outputs:

op_bus[7:0] → 8-bit output bus

Here’s how we can implement it using a behavioral for loop:

integer i;

always @(*) begin

    op_bus = 8'b0; // Clear all outputs
    
    for (i = 0; i < 8; i = i + 1) begin
    
        if (i == sel)
        
            op_bus[i] = ip;  // Pass input to selected output
            
    end
    
end

This loop runs during simulation and behaves like software, assigning values to outputs based on the select input.

Using generate for Loop in Structural Design
Now imagine you want to instantiate a block of hardware (like a module or cell) 500 times. Writing that manually 500 times is not practical.

To solve this, Verilog provides a generate for loop, which is used for structural replication of hardware during compilation (elaboration).

Key Points:
It is used to generate multiple instances of hardware units.

Uses a genvar (not integer) as the loop variable.

The loop is written outside always blocks.

Common in repetitive hardware structures like arrays of registers, adders, MUXes, etc.

genvar j;

generate

  for (j = 0; j < 500; j = j + 1) begin : block_name
    my_module U (.in(data_in[j]), .out(data_out[j]));
    
  end
  
endgenerate

<img width="410" height="346" alt="image" src="https://github.com/user-attachments/assets/c6d00c13-e293-48b4-915a-8636db642b7c" />


### Sky130RTL D5SK4 L3 For Loop and For Generate part3

We will be looking at the files mux_generate.v.

<img width="1036" height="492" alt="image" src="https://github.com/user-attachments/assets/e8381620-2fdc-4bd4-b462-5a89b95d5414" />

It is 4:1 multiplexer with 4 inputs, 2 bit select line and an output. We are making a bus i_int().

Certainly! Here's an improved and slightly more polished **tabular version** of your explanation, with clearer formatting and simplified wording:

| **Code Line**                        | **Explanation**                                                                 |
|-------------------------------------|---------------------------------------------------------------------------------|
| `module mux_generate ...`           | Declares the module `mux_generate` with 4 inputs (`i0` to `i3`), a 2-bit select line `sel`, and one output `y`. |
| `wire [3:0] i_int;`                 | Declares a 4-bit wire to bundle all 4 inputs into a single bus for easier handling. |
| `assign i_int = {i3, i2, i1, i0};`  | Combines the inputs into `i_int`, where `i3` is the most significant bit (MSB) and `i0` is the least significant bit (LSB). |
| `integer k;`                        | Declares the loop variable `k`, used in the upcoming `for` loop.               |
| `always @(*)`                       | Defines a combinational block that triggers whenever any input changes.        |
| `for (k = 0; k < 4; k = k + 1)`     | Iterates over all 4 bits of the `i_int` bus (from `i0` to `i3`).               |
| `if (k == sel)`                     | Compares the loop index `k` with the selected value `sel`. If they match, the corresponding input is selected. |
| `y = i_int[k];`                     | Assigns the selected input from `i_int[k]` to output `y`.                      |

<img width="841" height="358" alt="image" src="https://github.com/user-attachments/assets/871dd722-7f2c-4999-8f9e-d1f2e020a484" />

iverilog mux_generate.v tb_mux_generate.v

./a.out

gtkwave mux_generate.vcd

<img width="1028" height="477" alt="image" src="https://github.com/user-attachments/assets/1a2b50bd-9bf4-47fd-80f8-cfd6bc387e4d" />

We observe that the output y correctly follows the selected input based on the value of the sel line:

When sel = 2'b00, y = i0

When sel = 2'b01, y = i1

When sel = 2'b10, y = i2

When sel = 2'b11, y = i3

This behavior confirms the correct functionality of a 4:1 multiplexer, and this principle is essential when scaling to larger-bit multiplexers in complex circuits.

For Synthesis using Yosys:

yosys

read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

read_verilog mux_generate.v

synth -top mux_generate

abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib

show

Explaination:

read_liberty: Loads the standard cell library (used during mapping).

read_verilog: Loads your Verilog design (mux_generate.v).

synth -top mux_generate: Synthesizes the design with mux_generate as the top module.

abc: Performs technology mapping using your specified liberty file.

show: Displays the synthesized gate-level schematic.

<img width="1008" height="493" alt="image" src="https://github.com/user-attachments/assets/55be5659-c9bd-4004-b0fe-8129fdefd282" />

### Sky130RTL D5SK5 L2 Lab For and For Generate part2

Certainly! Here's a cleaner and more formal reframing of your content:

## 📘 Next Example: Demultiplexers

In this example, we will explore two different ways to implement a **Demultiplexer (DEMUX)** in Verilog.

### 🔧 To begin, open both files for comparison:

```bash
gvim demux_case.v -o demux_generate.v
```

This command opens the two files side-by-side using `gvim`:

- `demux_case.v` – Implements the DEMUX using a **`case` statement**
- `demux_generate.v` – Implements the DEMUX using a **`for` loop**

These files will help you understand the **difference in style and structure** between using a case-based approach vs. a loop-based (scalable) approach for implementing digital logic.


<img width="1021" height="483" alt="image" src="https://github.com/user-attachments/assets/4fa48562-51d9-4f03-9d88-84375c51d10c" />



We will use the power of "Blocking statements". we have assigned all the outputs to '00' as y_int = 8'b0 and the input line is routed to output depending upon the select line.

The initialization step y_int = 8'b0 is very important as it will also avoid "Inferred latches".
The "case" statement code is bulky and may increase if the required mux or demux is of higher bits.
Whereas in case of "For Loop", the code is small comparatively.

Now let us try out the simulation and synthesis for both "case" and "for loop":

<img width="1032" height="472" alt="image" src="https://github.com/user-attachments/assets/106cd6fa-9bba-4a6c-87bd-7b280555a7d4" />

We can see here, for the select line to be selected the output follows input i rest it is zero.
Similarly, we will get for "for loop" simulation.

<img width="1028" height="462" alt="image" src="https://github.com/user-attachments/assets/4f8d14a7-8eb0-47ab-babe-0b2402a071bc" />

### Sky130RTL D5SK5 L3 Lab For and For Generate part3

Sure! Here's a clear and well-structured reframed version of your content:

##  Understanding `for generate` in Verilog

To understand the usefulness of the **`for generate`** construct, let's consider a simple example — a **4-bit Ripple Carry Adder**.

When adding two 4-bit numbers `a` and `b`, we need **4 Full Adders (FAs)**, one for each bit position.

- Each **Full Adder** takes **3 inputs**:  
  - One bit from `a`  
  - One bit from `b`  
  - Carry-in from the previous stage

- It produces **2 outputs**:  
  - **Sum** bit for the current position  
  - **Carry-out** to the next stage

Instead of manually instantiating 4 full adders, we can use a **`generate for` loop** to **replicate the Full Adder module multiple times**, improving scalability and reducing repetitive code.

This approach is especially useful for designing larger adders (e.g., 8-bit, 16-bit, or more), where manual instantiation becomes cumbersome.


<img width="731" height="372" alt="image" src="https://github.com/user-attachments/assets/451f0921-8b41-409c-8aad-61aabdd1c8a9" />

There are two ways of executing this:

Instantiating FA 4 times
For generate

