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

In this session we'll have walkthrough our library.
![image](https://github.com/user-attachments/assets/19991893-cba2-4fea-82b8-b1e453779fcd)
to remove the red colour type:syn off
tt stands for typical. Process, temperature and voltage variation will determine how my silicon will work.
25 tells the temperature and 1v8 indicates the voltage.
### (ii) SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part2
esc+ :se nu to display line number.
### (iii) SKY130RTL D2SK1 L3 Lab4 Introduction to dot Lib part3
esc + 🆚
to search anything- esc+:/keyword(whatever the keyword is) for eg if keyword is xxxxxand2_0 then simply use :/.*and2_0
esc+:/area
![image](https://github.com/user-attachments/assets/878e1b41-534c-4d9d-8d7c-fe4d7557502b)
![image](https://github.com/user-attachments/assets/136d379d-0ae4-4ab4-ba7c-c8705726fddd)
wider cell more power consumption but delay wise it willbe less.
## 2-Hierarchical vs Flat Synthesis
### (i) SKY130RTL D2SK2 L1 Lab05 Hier synthesis flat synthesis part1
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
### (ii) SKY130RTL D2SK2 L2 Lab05 Hier synthesis flat synthesis part2
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

## 3- Various Flop Coding Styles and optimization
### (i)SKY130RTL D2SK3 L1 Why Flops and Flop coding styles part1
Sagar di vohti 
### (ii) SKY130RTL D2SK3 L2 Why Flops and Flop coding styles part2
Sagar di vohti
### (iii) SKY130RTL D2SK3 L3 Lab flop synthesis simulations part1
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

