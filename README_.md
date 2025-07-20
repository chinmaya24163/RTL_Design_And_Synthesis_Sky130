# RTL_Design_and_Synthesis
## Table of contents
- [Day 1 - Introduction to Verilog RTL design and Synthesis](#Day-1---Introduction-to-Verilog-RTL-design-and-Synthesis)
  - [Introduction to open-source simulator iverilog](#Introduction-to-open-source-simulator-iverilog)
    - [SKY130RTL D1SK1 L0 Introduction to iverilog design test bench](#SKY130RTL-D1SK1-L1-Introduction-to-iverilog-design-test-bench)
  - [Labs using iverilog and gtkwave](#Labs-using-iverilog-and-gtkwave)
    - [SKY130RTL D1SK2 L1 Lab1 introduction to lab](#SKY130RTL-D1SK2-L1-Lab1-introduction-to-lab)
    - [SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1](#SKY130RTL-D1SK2-L2-Lab2-Introduction-iverilog-gtkwave-part1)
    - [SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2](#SKY130RTL-D1SK2-L3-Lab2-Introduction-iverilog-gtkwave-part2)
  - [Introduction to Yosys and Logic synthesis](#Introduction-to-Yosys-and-Logic-synthesis)
    - [SKY130RTL D1SK3 L1 Introduction to yosys](#SKY130RTL-D1SK3-L1-Introduction-to-yosys)
    - [SKY130RTL D1SK3 L2 introduction to logic synthesis part1](#SKY130RTL-D1SK3-L2-introduction-to-logic-synthesis-part1)
    - [SKY130RTL D1SK3 L3 introduction to logic synthesis part2](#SKY130RTL-D1SK3-L3-introduction-to-logic-synthesis-part2)
  - [Labs using Yosys and Sky130 PDKs](#Labs-using-Yosys-and-Sky130-PDKs)
    - [SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux Part1](#SKY130RTL-D1SK4-L1-Lab3-Yosys-1-good-mux-Part1)
    - [SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux Part2](#SKY130RTL-D1SK4-L2-Lab3-Yosys-1-good-mux-Part2)
    - [SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux Part3](#SKY130RTL-D1SK4-L3-Lab3-Yosys-1-good-mux-Part3)
- [Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles](#Day-2---Timing-libs,-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-styles)
  - [Introduction to timing .libs](#Introduction-to-timing-.libs)
    - [SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part1](#SKY130RTL-D2SK1-L2-Lab4-Introduction-to-dot-Lib-part1)
    - [SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part2](#SKY130RTL-D2SK1-L2-Lab4-Introduction-to-dot-Lib-part2)
    - [SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part3](#SKY130RTL-D2SK1-L2-Lab4-Introduction-to-dot-Lib-part3)
  - [Hierarchical vs Flat Synthesis](#Hierarchical-vs-Flat-Synthesis)
    - [SKY130RTL D2SK2 L1 Lab05 Hier synthesis flat synthesis part1](#SKY130RTL-D2SK2-L1-Lab05-Hier-synthesis-flat-synthesis-part1)
    - [SKY130RTL D2SK2 L2 Lab05 Hier synthesis flat synthesis part2](#SKY130RTL-D2SK2-L2-Lab05-Hier-synthesis-flat-synthesis-part2)
    - [SKY130RTL D2SK3 L3 Lab flop synthesis simulations part1](#SKY130RTL-D2SK3-L3-Lab-flop-synthesis-simulations-part1)
    - [SKY130RTL D2SK3 L4 Lab flop synthesis simulations part2](#SKY130RTL-D2SK3-L4-Lab-flop-synthesis-simulations-part2)
    - [SKY130RTL D2SK3 L5 Interesting optimisations part1](#SKY130RTL-D2SK3-L5-Interesting-optimisations-part1)
    - [SKY130RTL D2SK3 L6 Interesting optimisations part2](#SKY130RTL-D2SK3-L6-Interesting-optimisations-part2)
- [Day 3 - Combinational and sequential optimizations](#Day-3---Combinational-and-sequential-optimizations)
  - [Introduction to optimizations](#Introduction-to-optimizations)
    - [SKY130RTL D3SK1 L1 Introduction to optimisations part1](#SKY130RTL-D3SK1-L1-Introduction-to-optimisations-part1)
    - [SKY130RTL D3SK1 L2 Introduction to optimisations part2](#SKY130RTL-D3SK1-L2-Introduction-to-optimisations-part2)
    - [SKY130RTL D3SK1 L3 Introduction to optimisations part3](#SKY130RTL-D3SK1-L3-Introduction-to-optimisations-part3)
  - [Combinational logic optimizations](#Combinational-logic-optimizations)
    - [SKY130RTL D3SK2 L1 Lab06 Combinational Logic Optimisations part1](#SKY130RTL-D3SK2-L1-Lab06-Combinational-Logic-Optimisations-part1)
    - [SKY130RTL D3SK2 L2 Lab06 Combinational Logic Optimisations part2](#SKY130RTL-D3SK2-L2-Lab06-Combinational-Logic-Optimisations-part2)
  - [Sequential logic optimizations](#Sequential-logic-optimizations)
    - [SKY130RTL D3SK3 L1 Lab07 Sequential Logic Optimisations part1](#SKY130RTL-D3SK3-L1-Lab07-Sequential-Logic-Optimisations-part1)
    - [SKY130RTL D3SK3 L2 Lab07 Sequential Logic Optimisations part2](#SKY130RTL-D3SK3-L2-Lab07-Sequential-Logic-Optimisations-part2)
    - [SKY130RTL D3SK3 L3 Lab07 Sequential Logic Optimisations part3](#SKY130RTL-D3SK3-L3-Lab07-Sequential-Logic-Optimisations-part3)
  - [Sequential optimzations for unused outputs](#Sequential-optimzations-for-unused-outputs)
    - [SKY130RTL D3SK4 L1 Seq optimisation unused outputs part1](#SKY130RTL-D3SK4-L1-Seq-optimisation-unused-outputs-part1)
    - [SKY130RTL D3SK4 L2 Seq optimisation unused outputs part2](#SKY130RTL-D3SK4-L2-Seq-optimisation-unused-outputs-part2)
- [Day 4 - GLS, blocking vs non-blocking and Synthesis-Simulation mismatch](#Day-4---GLS,-blocking-vs-non-blocking-and-Synthesis-Simulation-mismatch)
  - [GLS, Synthesis-Simulation mismatch and Blocking/Non-blocking statements](#GLS,-Synthesis-Simulation-mismatch-and-Blocking/Non-blocking-statements)
    - [SKY130RTL D4SK1 L1 GLS Concepts And Flow Using Iverilog](#SKY130RTL-D4SK1-L1-GLS-Concepts-And-Flow-Using-Iverilog)
    - [SKY130RTL D4SK1 L2 Synthesis Simulation Mismatch](#SKY130RTL-D4SK1-L2-Synthesis-Simulation-Mismatch)
    - [SKY130RTL D4SK1 L3 Blocking And NonBlocking Statements In Verilog](#SKY130RTL-D4SK1-L3-Blocking-And-NonBlocking-Statements-In-Verilog)
    - [SKY130RTL D4SK1 L4 Caveats With Blocking Statements](#SKY130RTL-D4SK1-L4-Caveats-With-Blocking-Statements)
  - [Labs on GLS and Synthesis-Simulation Mismatch](#Labs-on-GLS-and-Synthesis-Simulation-Mismatch)
    - [SKY130RTL D4SK2 L1 Lab GLS Synth Sim Mismatch part1](#SKY130RTL-D4SK2-L1-Lab-GLS-Synth-Sim-Mismatch-part1)
    - [SKY130RTL D4SK2 L2 Lab GLS Synth Sim Mismatch part2](#SKY130RTL-D4SK2-L2-Lab-GLS-Synth-Sim-Mismatch-part2)
  - [Labs on synth-sim mismatch for blocking statement](#Labs-on-synth-sim-mismatch-for-blocking-statement)
    - [SKY130RTL D4SK3 L1 Lab Synth sim mismatch blocking statement part1](#SKY130RTL-D4SK3-L1-Lab-Synth-sim-mismatch-blocking-statement-part1)
    - [SKY130RTL D4SK3 L2 Lab Synth sim mismatch blocking statement part2](#SKY130RTL-D4SK3-L2-Lab-Synth-sim-mismatch-blocking-statement-part2)
- [Day 5 - Optimization in synthesis](#Day-5---Optimization-in-synthesis)
  - [If Case constructs](#If-Case-constructs)
    - [SKY130RTL D5SK1 L1 IF CASE Constructs part1](#SKY130RTL-D5SK1-L1-IF-CASE-Constructs-part1)
    - 




  
    




# Day 1 - Introduction to Verilog RTL design and Synthesis
## Introduction to open-source simulator iverilog
---
### SKY130RTL D1SK1 L0 Introduction to iverilog design test bench
---

A **simulator** is a tool used to verify the functionality of a digital design. In RTL (Register Transfer Level) design, the simulator ensures the design behaves according to its specifications by applying a set of input signals, known as stimuli.

In this course, we are using **Icarus Verilog (iverilog)** as our simulation tool.

### What is a Design?

A **design** refers to the Verilog code or a collection of Verilog modules that describe the intended behavior of a digital circuit. It represents the logic that fulfills a specific functionality or specification.

### What is a Test Bench?

A **test bench** is a simulation environment created to verify the correctness of a design. It generates input signals (test vectors), applies them to the design, and monitors the outputs to ensure the circuit works as expected.

### How Does a Simulator Work?

A simulator is event-driven, meaning it reacts only to changes in signal values. Here's how it operates:

* When an input changes, the simulator evaluates the logic and updates the outputs.
* If there are no input changes, the outputs remain unchanged.

This allows for efficient and accurate simulation of digital behavior over time.

### Design and Test Bench Setup

A complete test environment typically consists of a **design module** with one or more **primary inputs** and **primary outputs**, and a **testbench module**, which includes:

* A **stimulus generator** to apply input signals to the design.
* A **stimulus observer** to Check and validate the output behavior.

**Note:** The testbench itself does not have any primary inputs or outputs. It operates entirely within the simulation environment to drive and observe the design.

![Screenshot 2025-07-09 130655](https://github.com/user-attachments/assets/c85f95a3-6840-47e1-9fe2-c673c71d2915)

Iverilog-based simulation flow:

The design and test bench are provided as inputs to iverilog. As mentioned earlier, the simulator monitors changes in input signals and updates the output accordingly. The output generated by the simulator is a `.vcd` file, which stands for Value Change Dump format.

To view this output waveform, we use **GTKWave**.

![Screenshot 2025-07-09 132236](https://github.com/user-attachments/assets/39f77655-dfcb-4376-a798-04ee26d51e25)

---
## Labs using iverilog and gtkwave
---
### SKY130RTL D1SK2 L1 Lab1 introduction to lab
---
### Toolflow and File Setup for Labs

We will now set up the necessary toolflow and file structure to run the labs.

#### Step 1: Create a Directory

Create a directory named `VLSI` and navigate into it:

```bash
mkdir VLSI
cd VLSI
````

#### Step 2: Clone the Required Repositories

Clone the following repositories from GitHub:

* **sky130RTLDesignAndSynthesisWorkshop**

```bash
git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
```

* **vsdflow**

```bash
git clone https://github.com/kunalg123/vsdflow.git
```

After this, your directory structure should look like:

```
VLSI/
├── sky130RTLDesignAndSynthesisWorkshop/
└── vsdflow/
```

This completes the initial setup required for running the labs.

![Screenshot 2025-07-09 143022](https://github.com/user-attachments/assets/e5cceec9-36a3-498b-a280-3b4e9be97b39)

![Screenshot 2025-07-09 143738](https://github.com/user-attachments/assets/9b16df58-5cf3-4465-b7b4-6700127203ad)

The contents of sky130RTLDesignAndSynthesisWorkshop directory are shown below

![Screenshot 2025-07-09 144919](https://github.com/user-attachments/assets/2f697cc0-57fc-4b92-9117-602ef47dccdd)

The `lib` directory contains the standard cell library that we will use for synthesis.
The `verilog_model` directory contains the Verilog models of all the standard cells present in the `.lib` file.

![Screenshot 2025-07-09 145308](https://github.com/user-attachments/assets/34e65092-a36f-4a94-9ced-8a46ed362db3)

![Screenshot 2025-07-09 145557](https://github.com/user-attachments/assets/915a4bdd-e194-45c5-a634-aec0d4b11516)

The `verilog_files` folder contains all our lab experiments, including both the source files and the testbench files.

![Screenshot 2025-07-09 145515](https://github.com/user-attachments/assets/e37cadf1-25dd-4c3a-8d8a-15160cb84add)

---
### SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1
---

### Tool Installation

Install the following tools required to run the labs:

#### 1. Install **Icarus Verilog** (`iverilog`)

```bash
sudo apt-get install iverilog
```

#### 2. Install **GTKWave**

```bash
sudo apt-get install gtkwave
```

These tools will allow you to compile Verilog files and visualize waveform outputs.

![Screenshot 2025-07-09 150942](https://github.com/user-attachments/assets/0f30c5ee-21e3-45c4-ba69-a85477202f3a)

![Screenshot 2025-07-09 151053](https://github.com/user-attachments/assets/0864bae3-e7c2-40e7-8456-10f02e9ac3d3)

### Simulate the Design: `good_mux`

Follow the steps below to compile, simulate, and view the waveform for the `good_mux` design.

#### 1. Compile the Design and Testbench

```bash
iverilog good_mux.v tb_good_mux.v
```

#### 2. Run the Simulation

```bash
./a.out
```

This will generate a waveform file named `tb_good_mux.vcd`.

#### 3. View the Waveform

```bash
gtkwave tb_good_mux.vcd
```

The verilog code for the design good_mux.v is shown below

![Screenshot 2025-07-09 151517](https://github.com/user-attachments/assets/aab406e3-8420-4069-9ed0-23897d87bd9d)

The verilog code for the testbench tb_good_mux.v is shown below

![Screenshot 2025-07-09 151553](https://github.com/user-attachments/assets/30be7049-31fe-4892-9a11-b4509f56c16a)

results:

![Screenshot 2025-07-09 151737](https://github.com/user-attachments/assets/8c56832a-1d8c-454c-b89b-78cada20f947)

viewing the waveform 

![Screenshot 2025-07-09 151853](https://github.com/user-attachments/assets/7b132bcf-8e75-4842-a5b1-e519a5c157d0)

![Screenshot 2025-07-09 152147](https://github.com/user-attachments/assets/d208c04a-237f-44d9-b008-9e7926d5f996)

---
### SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2
---

### 1. `good_mux.v` (Design)

```verilog
module good_mux (input i0, input i1, input sel, output reg y);

  always @(*) begin
    if (sel)
      y = i1;
    else
      y = i0;
  end

endmodule
```

### Explanation:

* **Inputs**: `i0`, `i1`, and `sel` (all 1-bit signals)
* **Output**: `y` (register type, 1-bit)
* The `always @(*)` block watches all inputs.
* If `sel = 1`, then `y = i1`; else `y = i0`.
* This is a 2:1 multiplexer.

---

## 2.`tb_good_mux.v` (Testbench)

```verilog
`timescale 1ns / 1ps

module tb_good_mux;

  // Inputs
  reg i0, i1, sel;

  // Output
  wire y;

  // Instantiate the Unit Under Test (UUT)
  good_mux uut (
    .i0(i0),
    .i1(i1),
    .sel(sel),
    .y(y)
  );

  initial begin
    $dumpfile("tb_good_mux.vcd");
    $dumpvars(0, tb_good_mux);

    // Initialize Inputs
    sel = 0;
    i0 = 0;
    i1 = 0;

    // Run simulation for 300 ns
    #300 $finish;
  end

  // Toggle sel every 75 ns
  always #75 sel = ~sel;

  // Toggle i0 every 10 ns
  always #10 i0 = ~i0;

  // Toggle i1 every 55 ns
  always #55 i1 = ~i1;

endmodule
```

---

## Testbench Behavior:

* Simulation runs for 300 ns.
* `sel` toggles every 75 ns to switch between `i0` and `i1`.
* `i0` toggles every 10 ns.
* `i1` toggles every 55 ns.
* Output `y` follows `i0` or `i1` based on the value of `sel`.
* Waveform is dumped to `tb_good_mux.vcd` and can be viewed using GTKWave.

---
## Introduction to Yosys and Logic synthesis
---
### SKY130RTL D1SK3 L1 Introduction to yosys
---

## Introduction to Yosys

**Yosys** is the synthesizer tool used in this course. It is responsible for converting RTL (Register Transfer Level) code into a gate-level **netlist** using standard cells.

### Role of Synthesizer:

A synthesizer takes a digital RTL design and a standard cell library (`.lib` file) and generates a netlist that represents the circuit using gates and cells from the library.

### Yosys Synthesis Flow:

1. **Inputs to Yosys**:

   * The RTL design (`.v` file)
   * The standard cell library (`.lib` file)

![Screenshot 2025-07-09 155007](https://github.com/user-attachments/assets/a2b57e82-b6cb-489f-a5b2-fe5d23f89cf8)


2. **Yosys Commands**:

   * `read_verilog` – Reads the Verilog design file.
   * `read_liberty` – Reads the `.lib` file containing timing and cell information.
   * `write_verilog` – Writes out the synthesized netlist.

![Screenshot 2025-07-09 155111](https://github.com/user-attachments/assets/ecfeb932-9879-41b6-958a-39ed83652fe3)

3. **Output**:

   * A netlist file representing the design using standard cells from the `.lib` library.

### Netlist Verification:

To verify if the synthesis process was successful and functionally correct:

* Use the **same testbench** that was used for the original RTL simulation.
* Apply the synthesized **netlist** and the **testbench** to the simulator (**Icarus Verilog**).
* Generate the VCD (`.vcd`) file.
* Load the VCD file in **GTKWave** and compare the waveform output.

![Screenshot 2025-07-09 155345](https://github.com/user-attachments/assets/61b6d58e-e37e-4e12-b016-1ec309d89379)

### Important Notes:

* The stimulus in the testbench **must match** the one used during RTL simulation.
* The **primary inputs and outputs** of the netlist remain the same as the RTL design.
* Therefore, **the same testbench** can be reused for post-synthesis simulation.

![Screenshot 2025-07-09 155551](https://github.com/user-attachments/assets/fae00675-36ce-46d9-a14c-be5a60da2f5d)

---
### SKY130RTL D1SK3 L2 introduction to logic synthesis part1
---

### **Logic Synthesis Overview**

#### **1. RTL Design**

* RTL (Register Transfer Level) design is the **behavioral representation** of a digital system based on its required specification.
* It defines how data moves between registers and how operations are performed on that data.

![Screenshot 2025-07-10 093911](https://github.com/user-attachments/assets/14da95b2-b608-4591-9b49-6265b82af104)

![Screenshot 2025-07-10 093941](https://github.com/user-attachments/assets/97dbaded-68ba-4c5a-a742-81c2c2251a0c)

#### **2. What is Logic Synthesis?**

* Logic synthesis is the **process of converting RTL code into a digital logic circuit**.
* This involves translating behavioral descriptions into a network of logic gates.
* The transition from RTL to gate-level design is called **synthesis**.
* The final output of this process is a **netlist**, which describes the gates and their interconnections.

#### **3. Inputs and Outputs of Synthesis**

* **Inputs:**

  * RTL Design (written in Verilog or VHDL)
  * Technology Library (`.lib` file)
* **Output:**

  * Gate-level netlist (`.v` file)

![Screenshot 2025-07-10 094007](https://github.com/user-attachments/assets/cd388e51-8760-4ff2-9dcc-bbf54b26d40c)

#### **4. What is a `.lib` File?**

* A `.lib` file is a **collection of logic cells** provided by a standard cell library.
* It includes basic gates like **AND, OR, NOT**, and their **variants**:

  * Different **input configurations** (e.g., 2-input OR, 3-input OR)
  * Different **speed-power tradeoffs** (e.g., **slow**, **medium**, **fast** cells)

![Screenshot 2025-07-10 094022](https://github.com/user-attachments/assets/a81e341a-c57e-4682-8bab-8d948ff7abf7)

#### **5. Why Different Flavours of Gates?**

* The **combinational delay** in a logic path directly affects the **maximum speed** of a digital circuit.

![Screenshot 2025-07-10 094036](https://github.com/user-attachments/assets/e0f4f50a-053c-40fc-9b0f-62439c696b37)

* The clock cycle must account for:

  ```
  Tclk > Tcq_A + Tcomb + Tsetup_B
  ```

  * **Tcq\_A** = Clock-to-Q delay of DFF A
  * **Tcomb** = Delay of the combinational logic
  * **Tsetup\_B** = Setup time of DFF B

* To **minimize Tcomb**, we use **faster cells** from the `.lib` file.

* This helps reduce the required **clock period (Tclk)** and hence **increase the operating frequency**.

#### **6. Maximum Clock Frequency**

* The **minimum clock period** determines the **maximum frequency**:

  ```
  fclk(max) = 1 / Tclk(min)
  ```

![Screenshot 2025-07-10 094117](https://github.com/user-attachments/assets/e531047d-079a-4be1-bd90-bbcd3cefbbfe)

---
### SKY130RTL D1SK3 L3 introduction to logic synthesis part2
---

### **Are Faster Cells Sufficient?**

At first glance, it might seem that using only **faster cells** is the key to achieving **maximum performance**. After all, higher clock speeds typically mean better performance. But this leads us to an important question:

> If faster cells minimize delay, **why are slower cells needed at all?**

---

### **Why Do We Need Slow Cells?**

To meet **timing constraints**, both **setup** and **hold** times must be satisfied:

* For **setup time** (performance constraint), we want the data to arrive *before* the clock edge.
* For **hold time** (reliability constraint), we want the data to **stay stable briefly after** the clock edge.

![Screenshot 2025-07-10 095024](https://github.com/user-attachments/assets/66e3dea3-ce07-4e42-b216-b52dd5cd7e4c)

If the combinational delay is **too short**, we may violate **hold time**:

```
Thold_B < Tcq_A + Tcomb
```

So:

* We need **faster cells** to **reduce Tcomb** and meet setup timing.
* We need **slower cells** to **increase Tcomb** and avoid hold time violations.

The `.lib` file includes all these different **cell variants** to allow flexibility in achieving the correct balance.

---

### **Understanding Hold Time**

* **Hold time** of a flip-flop is the **minimum time** after the clock edge during which data **must remain stable**.
* If the input to flip-flop B changes **too quickly**, it might capture the **wrong data**.
* Thus, **slower cells** can intentionally **increase delay** to help meet the hold constraint.

---

### **Faster vs. Slower Cells**

* The **load** in a digital logic circuit is essentially a **capacitance**.
* The **faster** we can **charge/discharge** this load, the **lower** the propagation delay.

| Parameter        | Faster Cells          | Slower Cells              |
| ---------------- | --------------------- | ------------------------- |
| Transistor Width | Wider (more current)  | Narrower (less current)   |
| Delay            | Lower                 | Higher                    |
| Area             | Larger                | Smaller                   |
| Power            | Higher                | Lower                     |
| Use Case         | Improves setup timing | Helps fix hold violations |

---

### **Trade-Offs: Speed vs. Area/Power**

Faster cells offer performance benefits but come at a **cost**:

* **More area**
* **More power consumption**
* **Greater risk of hold time violations**

Slower cells are:

* **Power-efficient**
* **Area-efficient**
* **Useful in preventing hold violations**

Hence, **faster cells are not always sufficient or ideal**.

---

### **Selection of Cells: Synthesizer Guidance**

The **synthesis tool** decides which cells to use during logic synthesis. However, we must **guide** it to choose an **optimal mix** of fast and slow cells.

* **Too many fast cells** → High power, large area, potential hold issues.
* **Too many slow cells** → Fails to meet timing/performance goals.

This guidance is provided using **constraints**:

* Timing constraints (clock period, setup/hold margin)
* Area and power constraints
* Design objectives and priorities

---

### **Conclusion**

The process of synthesis is not just about making the circuit work—it's about making it work **efficiently**. The selection between faster and slower cells is a **critical design decision**, and synthesis tools use **constraints** to make this trade-off in a balanced way.

![Screenshot 2025-07-10 095118](https://github.com/user-attachments/assets/02fc26c7-9db8-4d52-8278-0edab170a5ef)

---
## Labs using Yosys and Sky130 PDKs
---
### SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux Part1
---

### **Introduction to Synthesizer: Yosys**

**Yosys** is an open-source synthesis tool used for converting RTL code into a gate-level netlist using a given standard cell library.

#### **Steps to Invoke and Use Yosys**

1. **Start Yosys**

   * Open a terminal and navigate to the working directory:

     ```bash
     cd verilog_files
     ```
   * Invoke the tool by typing:

     ```bash
     yosys
     ```

---

#### **1. Read the Standard Cell Library**

Before synthesis, the tool must understand the available logic cells. This is done by reading the `.lib` file:

```yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

---

#### **2. Read the Verilog Design**

Next, import the RTL design (example: a multiplexer design named `good_mux.v`):

```yosys
read_verilog good_mux.v
```

![Screenshot 2025-07-10 101837](https://github.com/user-attachments/assets/ee6362bf-f4a4-479a-aebf-9e94cdc53062)

---

#### **3. Perform Synthesis**

Specify the top module of the design:

```yosys
synth -top good_mux
```
![Screenshot 2025-07-10 101929](https://github.com/user-attachments/assets/0c1476d1-7ab7-49a9-9289-118e98a896c4)

This step translates the RTL to a gate-level representation using generic gates.

![Screenshot 2025-07-10 101957](https://github.com/user-attachments/assets/50c26202-08bc-45db-8e04-508c9e3238a2)

---

#### **4. Technology Mapping**

Map the synthesized design to standard cells defined in the `.lib` file:

```yosys
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
![Screenshot 2025-07-10 102113](https://github.com/user-attachments/assets/7c8b46da-a69b-4e00-ae1f-1abdd597ce5f)

At this stage, the synthesis is complete and the result is a netlist using specific standard cells.

---

#### **5. Analyze the Output**

![Screenshot 2025-07-10 102151](https://github.com/user-attachments/assets/d2a1e221-0bfd-468e-9298-97eb9467711e)

* Compare the netlist with the original `good_mux.v`.
* **Note:**

  * The output netlist will not include internal signals.
  * Only **3 inputs** and **1 output** are visible (as in the original RTL).
  * The following **standard cells** are used:
mux2_1

---

#### **6. Visualize the Logic**

To view a graphical representation of the synthesized logic, use the `show` command:

```yosys
show
```

![Screenshot 2025-07-10 102641](https://github.com/user-attachments/assets/ac6efe5e-b198-49cc-a005-fffeb38689a3)

This launches a viewer that displays the gate-level circuit as derived from the RTL.

![Screenshot 2025-07-10 102709](https://github.com/user-attachments/assets/472d982b-6b1f-41d2-82fb-cbb8a053e5bf)

---
### SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux Part2
--- 

### **Corresponding Verilog Code**

```verilog
module good_mux (
    input i0,
    input i1,
    input sel,
    output reg y
);

always @(*) begin
    if (sel)
        y = i1;
    else
        y = i0;
end

endmodule
```

---

### **Explanation of the Yosys Output Image**

This is a graphical, gate-level representation of the `good_mux` module, generated using the `show` command in Yosys after synthesis and technology mapping using the Sky130 standard cell library.

#### **Block-by-Block Explanation**

| Element                   | Description                                                                      |
| ------------------------- | -------------------------------------------------------------------------------- |
| `i0`, `i1`, `sel`         | These are the 3 input signals to the module, shown entering on the left.         |
| `$86`                     | Internal instance name auto-generated by Yosys.                                  |
| `sky130_fd_sc_hd__mux2_1` | This is the 2:1 multiplexer standard cell from the Sky130 standard cell library. |
| `A0`, `A1`, `S`           | Input pins of the multiplexer: A0 = i0, A1 = i1, S = sel                         |
| `X`                       | Output pin of the multiplexer cell.                                              |
| `y`                       | Final output of the module, connected to the mux output.                         |
| `good_mux`                | Name of the top-level module.                                                    |

---

### **Mapping Between RTL and Synthesized Logic**

* The `always` block in the RTL uses an `if-else` condition to assign either `i0` or `i1` to `y`, based on the value of `sel`.
* During synthesis, Yosys recognized this as a 2:1 multiplexer function.
* It replaced the behavioral logic with a `sky130_fd_sc_hd__mux2_1` standard cell.
* This standard cell has three inputs: A0 (i0), A1 (i1), and S (select), and one output X which drives `y`.

---

### **Conclusion**

Yosys successfully synthesized the behavioral Verilog into a gate-level representation using the appropriate multiplexer cell from the Sky130 library. The visualization shows that the design is mapped efficiently, and internal signals are optimized out in favor of direct cell-level connections.

---
### SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux Part3
---

### **Writing the Netlist in Yosys**

Once synthesis and technology mapping are complete, you can **export the gate-level netlist** using the following command:

```yosys
write_verilog good_mux_netlist.v
```
![image](https://github.com/user-attachments/assets/aa10189c-44cc-484e-84c1-e4438ba6fa24)

This generates a netlist file named `good_mux_netlist.v`.

To create a **simplified netlist** (without attributes like timing, area, etc.), use:

```yosys
write_verilog -noattr good_mux_netlist.v
```

This version is easier to read and focuses only on structural connections.

---
![Screenshot 2025-07-10 105453](https://github.com/user-attachments/assets/892fb7cd-bff9-4558-89a0-b853789e84ea)

![Screenshot 2025-07-10 105544](https://github.com/user-attachments/assets/129a4618-5555-4f00-ac41-a49579dff863)

### **Sample Netlist: `good_mux_netlist.v`**

```verilog
module good_mux(i0, i1, sel, y);

  // Wire declarations
  wire n0;
  wire n1;
  wire n2;
  wire n3;

  // Port declarations
  input i0;
  input i1;
  input sel;
  output y;

  // Instance of standard cell mux2_1 from Sky130 library
  sky130_fd_sc_hd__mux2_1 u1 (
    .A0(n0),
    .A1(n1),
    .S(n2),
    .X(n3)
  );

  // Wire assignments
  assign n0 = i0;
  assign n1 = i1;
  assign n2 = sel;
  assign y  = n3;

endmodule
```

---

### **Explanation of Key Elements**

| Component                          | Description                                           |
| ---------------------------------- | ----------------------------------------------------- |
| `sky130_fd_sc_hd__mux2_1`          | 2:1 multiplexer standard cell from the Sky130 library |
| `u1`                               | Instance name (can be autogenerated or user-defined)  |
| `.A0(n0), .A1(n1), .S(n2), .X(n3)` | Port-to-net connections                               |
| `n0–n3`                            | Internal wires for connecting RTL ports to cell ports |

---

### **Notes**

* This netlist is **structural**, meaning it lists the components used and how they’re connected.
* It's used for **place and route**, **static timing analysis**, and further backend steps.
* The simplified netlist with `-noattr` is generally preferred for **manual inspection or debugging**.

---
# Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles
---
## Introduction to timing .libs
---
### SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part1
---

### **Understanding the Contents of a `.lib` File**

The `.lib` file, also known as a **Liberty file**, contains detailed **timing, power, and functional information** about standard cells used during synthesis. Let’s break down the key elements from a typical `.lib` file.

---

![Screenshot 2025-07-10 115849](https://github.com/user-attachments/assets/cf4ef313-c43a-465a-81d5-98ab060e4ba0)

#### **1. Library Declaration**

```
Library ("sky130_fd_sc_hd__tt_025C_1v80")
```

This line defines the **name of the library** being used.

* `sky130_fd_sc_hd`: SkyWater 130nm standard cell library (high-density variant).
* `tt`: Refers to the **PVT (Process-Voltage-Temperature) corner**, in this case, **typical process**.
* `025C`: Indicates a **temperature of 25°C**.
* `1v80`: Indicates the **supply voltage** is **1.80V**.

---

#### **2. What is a PVT Corner?**

PVT stands for **Process, Voltage, and Temperature** — three key variables that influence how silicon behaves.

| Parameter       | Meaning                                                                                                |
| --------------- | ------------------------------------------------------------------------------------------------------ |
| **Process**     | Refers to **fabrication variation** (e.g., fast, slow, typical silicon).                               |
| **Voltage**     | Varying supply voltages affect the switching speed and power.                                          |
| **Temperature** | Higher temperatures cause **slower operation**, and lower temperatures can cause **faster switching**. |

---

#### **3. Why Do We Need PVT Corners?**

Due to real-world variations during manufacturing and operating conditions, we need to ensure that our design:

* Works correctly in **worst-case**, **best-case**, and **typical** conditions.
* Is **functionally correct** and **timing-safe** under **all valid scenarios**.

Examples of PVT corners:

| Corner Name    | Description                                   |
| -------------- | --------------------------------------------- |
| `ss_125C_1v60` | Slow process, 125°C, 1.60V (worst-case delay) |
| `ff_0C_1v95`   | Fast process, 0°C, 1.95V (best-case delay)    |
| `tt_025C_1v80` | Typical case for normal operation             |

---

#### **Conclusion**

The `.lib` file acts as a **technology reference** for the synthesis tool. It helps the tool:

* Select appropriate **standard cells**.
* Estimate **timing** and **power**.
* Perform **technology mapping** based on **PVT-aware constraints**.

A proper understanding of the `.lib` content ensures that the synthesized circuit will function correctly under all expected operating conditions.

---
### SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part2
---

### **Deep Dive into the `.lib` File**

The `.lib` (Liberty) file contains **detailed information about standard cells** used during logic synthesis and static timing analysis. Let’s explore its major contents and structure.

---

![Screenshot 2025-07-10 115849](https://github.com/user-attachments/assets/0670d001-20e5-4a37-a067-d664b963a4ed)

### **1. Units and Operating Conditions**

The `.lib` file begins by defining **units** for various physical quantities:

* **Time** (e.g., in nanoseconds)
* **Voltage** (e.g., volts)
* **Power** (e.g., microwatts)
* **Current** (e.g., milliamperes)
* **Resistance**, **Capacitance**, **Capacitive load** (typically in ohms, femtofarads, etc.)

![Screenshot 2025-07-10 120836](https://github.com/user-attachments/assets/c4c8e7d5-4a7f-421e-9f67-98fa581fdca1)

It also specifies the **operating conditions** under which the cell data is valid, including:

* **Temperature**
* **Supply voltage**
* **Process corner**

These parameters help the synthesis tool evaluate the performance of each cell under different environmental and manufacturing variations.

---

### **2. Multiple Cells and Cell Definitions**

A typical `.lib` file contains **many standard cells**. Each cell begins with the keyword:

```liberty
cell (cell_name) {
   ...
}
```

For example:

```liberty
cell (sky130_fd_sc_hd__a2111o_1) {
   ...
}
```
![Screenshot 2025-07-10 120920](https://github.com/user-attachments/assets/0aff8fc7-6ea3-435b-a98b-a0cecae7a0d8)


This marks the beginning of the definition for the cell `sky130_fd_sc_hd__a2111o_1`.

---

### **3. Flavours of Cells**

* The **same logic function** may have **multiple variants** (or flavours), e.g., `_0`, `_1`, `_2`, etc.
* These variants differ in **driving strength**, **delay**, **power consumption**, and **area**.
* For example:

  * `sky130_fd_sc_hd__a2111o_1`: Standard drive
  * `sky130_fd_sc_hd__a2111o_2`: Higher drive strength

---

### **4. Example Cell: `sky130_fd_sc_hd__a2111o_1`**

* This is a complex gate with **5 inputs**: `A1`, `A2`, `B1`, `C1`, `D1`.

* The cell performs a specific logic operation defined in both `.lib` and equivalent Verilog model.

![Screenshot 2025-07-10 123504](https://github.com/user-attachments/assets/6296668e-a456-456d-a440-16901512921d)

* You can view the **Verilog model** of the library using:

  ```bash
  :sp ../my_lib/verilog_model/sky130_fd_sc_hd.v
  ```

![Screenshot 2025-07-10 123718](https://github.com/user-attachments/assets/d68fcb2b-ca2d-4ce1-89ec-ae044a519da1)

* Since there are 5 inputs, and each can be 0 or 1:

  * Total possible input combinations = 2⁵ = **32**
  * The `.lib` includes **leakage power** data for **every combination**.

![Screenshot 2025-07-10 123819](https://github.com/user-attachments/assets/0f349e96-2b9e-48b8-a8a2-7c610fd18b1f)

---

### **5. Key Information Inside Each Cell Block**

Each cell definition includes:

| Parameter           | Description                                                              |
| ------------------- | ------------------------------------------------------------------------ |
| `area`              | Physical area of the cell (in square microns)                            |
| `pin`               | Definition block for each input/output port                              |
| `input_capacitance` | Intrinsic capacitance of the input pin                                   |
| `power`             | Power consumption info: internal power, leakage, dynamic                 |
| `timing`            | Delay, transition time, and slope-related timing information             |
| `function`          | Boolean logic function implemented by the cell                           |
| `related_pin`       | Specifies which other pin affects timing of a given pin (for setup/hold) |

![Screenshot 2025-07-10 124150](https://github.com/user-attachments/assets/45b75459-6780-4cd6-8089-39c057e4989a)

![Screenshot 2025-07-10 124248](https://github.com/user-attachments/assets/3de573fb-476b-4e52-a604-5c662b47b56b)

---

### **6. Importance in Synthesis and Timing**

The data in the `.lib` file helps the synthesis tool:

* Estimate **propagation delays**
* Analyze **power** and **leakage**
* Select the **most optimal variant** of a cell based on constraints
* Ensure that designs meet **setup**, **hold**, and **clock period** requirements

---
### SKY130RTL D2SK1 L2 Lab4 Introduction to dot Lib part3
---
Here is a structured explanation for **Example 2** on analyzing a smaller gate (AND gate) from the standard cell library. This version is formatted cleanly for use in reports, lab manuals, or documentation:

---

### **Example 2: Understanding a Simple Gate – AND Gate**

![Screenshot 2025-07-10 125526](https://github.com/user-attachments/assets/9bd03fb9-e2b0-4fcd-acda-adc65f037fa8)

#### **Cell Under Study: `sky130_fd_sc_hd__and2_0`**

![Screenshot 2025-07-10 125955](https://github.com/user-attachments/assets/f24be0a0-75cc-439a-b81e-ceadd350cb7d)

This is a **2-input AND gate** from the Sky130 standard cell library.

* **Name**: `sky130_fd_sc_hd__and2_0`
* **Function**: Performs logical AND on two inputs
* **Inputs**: A, B
* **Output**: Y
* **Input Combinations**: Since it has 2 inputs, total possible combinations = 2² = **4**

---

### **Verilog Model**

The behavior of this cell can be viewed by opening the Verilog model file:

```bash
:sp ../my_lib/verilog_model/sky130_fd_sc_hd.v
```
![Screenshot 2025-07-10 131129](https://github.com/user-attachments/assets/9d7f18e9-6af0-4fa1-b318-96f5b38fea76)

In the Verilog model, you’ll find something like:

![Screenshot 2025-07-10 131409](https://github.com/user-attachments/assets/3d0050b1-dfe1-4837-9aa0-6ba5b1069818)

---
### **Area Analysis**

To compare the area of two AND gate variants (`and2_0` vs `and2_1`), open the `.lib` file and locate the corresponding `cell` blocks.

> **Note:**
> To split the GVim window vertically for side-by-side viewing, use the command:
>
> ```
> :vsp
> ```
>
> This is useful for comparing two cells (e.g., `and2_0` and `and2_1`) in the same `.lib` file.

![Screenshot 2025-07-10 131816](https://github.com/user-attachments/assets/55cd3433-5d67-48d7-a0e1-a55507ed7250)

Inside the `.lib` file (`sky130_fd_sc_hd__tt_025C_1v80.lib`), search for:

```liberty
cell (sky130_fd_sc_hd__and2_0) {
    area : <value>;
    ...
}

cell (sky130_fd_sc_hd__and2_1) {
    area : <larger value>;
    ...
}
```
![Screenshot 2025-07-10 132314](https://github.com/user-attachments/assets/56b2f260-9359-4cd8-add5-23be44c5422e)

This shows that:

* `and2_1` has a **larger area** than `and2_0`.
* The larger area implies **wider transistors** are used in `and2_1`.
* **Wider transistors** can **source/sink more current**, leading to **faster switching**, but they occupy more silicon area and consume more power.

#### **Comparison: `and2_0` vs `and2_1`**

| Cell Name                 | Area (μm²) | Inference                    |
| ------------------------- | ---------- | ---------------------------- |
| `sky130_fd_sc_hd__and2_0` | Smaller    | Narrower transistors, slower |
| `sky130_fd_sc_hd__and2_1` | Larger     | Wider transistors, faster    |

This implies:

* **Higher drive strength versions** (like `_1`, `_2`) use **wider transistors**.
* Wider transistors can **charge/discharge load capacitance faster**, resulting in **lower delay**.
* However, they **consume more area** and often more **power**.

---

### **Conclusion**

By comparing `and2_0` and `and2_1` in the `.lib` file:

* You observe the **trade-off between area and performance**.
* Larger cells = **faster**, but **costlier** in silicon area.
* Synthesis tools must choose the **right variant** based on timing, area, and power constraints.

---
## Hierarchical vs Flat Synthesis
---
### SKY130RTL D2SK2 L1 Lab05 Hier synthesis flat synthesis part1
---
### **What is Hierarchical vs. Flat Synthesis?**

In digital design, a system can be built using **multiple submodules**. The way these are handled during synthesis can follow either a **hierarchical** or **flat** approach.

#### **Hierarchical Synthesis**

* In **hierarchical synthesis**, the **submodules are preserved** as independent entities during synthesis.
* Each module is synthesized separately, and then connected at the top level.
* **Benefits**:

  * Faster synthesis for large designs
  * Useful for modular debugging and reuse
* **Drawbacks**:

  * Limited global optimization across module boundaries

#### **Flat Synthesis**

* In **flat synthesis**, all submodules are **inlined into the top-level module**, forming a single flattened netlist.
* This allows the synthesizer to perform **global optimizations**.
* **Benefits**:

  * Better optimization for area, timing, and power
* **Drawbacks**:

  * More memory and time-consuming
  * Harder to trace logic back to original modules

---

### **Example Design: `multiple_modules.v`**

This file is located in the `verilog_files` directory and defines a small hierarchical design using two submodules.

#### **Code**

![Screenshot 2025-07-10 140014](https://github.com/user-attachments/assets/b1150e7a-e510-463b-a751-c58587950dca)

```verilog
// OR gate module
module sub_module2 (input a, input b, output y);
  assign y = a | b;
endmodule

// AND gate module
module sub_module1 (input a, input b, output y);
  assign y = a & b;
endmodule

// Top-level module using two submodules
module multiple_modules (input a, input b, input c, output y);
  wire net1;

  sub_module1 u1 (.a(a), .b(b), .y(net1));  // net1 = a & b
  sub_module2 u2 (.a(net1), .b(c), .y(y));  // y = net1 | c => y = (a & b) | c

endmodule
```
![Screenshot 2025-07-10 135806](https://github.com/user-attachments/assets/246af06f-d3e2-4162-82a8-aa1b4988be72)

### **Synthesis of `multiple_modules.v`**

Let’s now synthesize the `multiple_modules.v` file.

![Screenshot 2025-07-10 140800](https://github.com/user-attachments/assets/c255ac8a-9774-44e3-9264-f2a216745a5b)

![Screenshot 2025-07-10 141008](https://github.com/user-attachments/assets/0882e82d-f664-4f39-affa-84bed7c929c7)

![Screenshot 2025-07-10 141112](https://github.com/user-attachments/assets/b912493e-8afe-4f09-bc69-e2a7adf2619e)

This design includes two submodules:

* `sub_module1` implements an **AND** gate
* `sub_module2` implements an **OR** gate

The top-level module, `multiple_modules`, instantiates:

* One instance of `sub_module1` (named `u1`)
* One instance of `sub_module2` (named `u2`)

The report shows:

* `sub_module1` contains **one AND gate**
* `sub_module2` contains **one OR gate**
* The top module contains **one instance of each submodule**

Overall, the entire design consists of:

* **One AND gate**
* **One OR gate**

Now, Linkimg the design to the library
In Yosys, this is done using the following command:

```yosys
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
![Screenshot 2025-07-10 142103](https://github.com/user-attachments/assets/f730f208-60a0-49df-b9b9-fb43767f1dd9)

### **Visualizing the Synthesized Design: Hierarchical View**

After synthesis and linking, use the following Yosys command to view the synthesized logic:

```yosys
show multiple_modules
```
![Screenshot 2025-07-10 142511](https://github.com/user-attachments/assets/8aa2017e-3d17-4e3b-b29b-9ca131fc7192)

This command opens a graphical representation of the design.

---

### **What Do You See?**

![Screenshot 2025-07-10 142551](https://github.com/user-attachments/assets/da2cc977-5573-4381-816b-8ee66d8c60af)

Instead of seeing a logic-level **block diagram** composed of **AND** and **OR** gates, the view shows two **instantiations**:

* `u1`: Instance of `sub_module1`
* `u2`: Instance of `sub_module2`

These are preserved **as separate blocks**, not broken down into their internal logic (AND/OR).

---

### **Why Does This Happen?**

This is an example of a **hierarchical design**.

* The synthesis has preserved the **module hierarchy**.
* The submodules (`sub_module1` and `sub_module2`) are shown as **black boxes** or **instances** inside the top module.
* You don’t see the gates (like AND, OR) because they are **inside the submodules**, and those were **not flattened**.

---

### **What We Expected vs. What We See**

| Expectation                     | Observation                       |
| ------------------------------- | --------------------------------- |
| AND and OR gates shown directly | Only u1 and u2 instances visible  |
| Flat gate-level logic diagram   | Hierarchical module-level diagram |

This highlights the **difference between flat and hierarchical synthesis**.

* **Flat synthesis**: Would have shown individual AND and OR gates.
* **Hierarchical synthesis**: Keeps module boundaries intact, and shows only instances like `u1` and `u2`.

### **Writing the Netlist**

Now let’s write the netlist using the following command:

```yosys
write_verilog -noattr multiple_modules_hier.v
```
![Screenshot 2025-07-10 152824](https://github.com/user-attachments/assets/b00b201f-f9ab-4ccc-8dd1-c5bf18f9a2f4)

This generates a netlist file named `multiple_modules_hier.v` without additional attributes.

![Screenshot 2025-07-10 152924](https://github.com/user-attachments/assets/4fd2f847-9e64-4453-9aee-a9b42a7ddc60)

When you open the file, you’ll observe that `sub_module1` and `sub_module2` are preserved as **separate modules** in the netlist.

![Screenshot 2025-07-10 153224](https://github.com/user-attachments/assets/74881faf-3c39-41fb-8ae5-2007463ba273)

![Screenshot 2025-07-10 153239](https://github.com/user-attachments/assets/d0108a90-5b8c-46b4-bda1-d8b1e1855793)

![Screenshot 2025-07-10 153256](https://github.com/user-attachments/assets/cd43a2c2-62d7-4eba-a0db-7255c426612b)

### **Observation from the Generated Netlist**

When the netlist was generated by the instructor, the structure of `sub_module2` appeared different from a straightforward OR gate implementation. It resembled something like the following:

![Screenshot 2025-07-10 154710](https://github.com/user-attachments/assets/841ef486-a448-4cdd-833e-b002c9af001b)

Instead of directly using an **OR gate**, the synthesis tool generated logic using **inverters and a NAND gate**, effectively implementing a **bubbled NAND** (DeMorgan equivalent of an OR gate).

### **Why Did the Synthesis Tool Do This?**

The tool chose this structure not by accident, but as an **optimization based on CMOS design principles**.

#### **CMOS Gate Implementation Basics:**

* **NAND gates** are implemented using **stacked NMOS transistors**, which switch faster and consume less area.
* **NOR gates** are implemented using **stacked PMOS transistors**, which are **slower** and **larger** due to the **poor mobility of holes in PMOS**.

#### **Key Reason:**

> **PMOS transistors have lower mobility than NMOS**, so a stack of PMOS (as in a NOR gate) results in **larger area and slower switching**.

To avoid this:

* The synthesis tool avoids direct NOR gates
* Instead, it may use **NAND + Inverters** (i.e., a bubbled NAND structure) to implement the same logic function **more efficiently** in silicon.

### **Conclusion**

Even though the RTL defines `sub_module2` as an OR gate:

```verilog
assign y = a | b;
```

The synthesis tool rewrites this into a form better suited for CMOS implementation — one that:

* Uses **fewer or smaller PMOS transistors**
* Is **faster and more area-efficient**
* Maintains the exact same logical behavior

This is a common optimization done automatically by the synthesis engine during technology mapping.
---
### SKY130RTL D2SK2 L2 Lab05 Hier synthesis flat synthesis part2
---
### **Synthesis Behavior**

* If you synthesize this design **hierarchically**, `sub_module1` and `sub_module2` will appear as **separate blocks** in the netlist.
* If you synthesize it **flat**, the synthesis tool will **merge** all logic into the `multiple_modules` block and eliminate submodule boundaries.

### **Flattening the Design**

To flatten the design and remove module hierarchies, use the following command in Yosys:

```yosys
flatten
write_verilog -noattr multiple_modules_flat.v
```
![Screenshot 2025-07-10 155854](https://github.com/user-attachments/assets/aaeb6403-9637-484d-8753-6539b876739c)

This generates a **flattened netlist** named `multiple_modules_flat.v`.

---

### **Comparison with Hierarchical Netlist**

![Screenshot 2025-07-10 160154](https://github.com/user-attachments/assets/301c0095-2e48-4f43-ba45-4f338aea6fab)

* In the **hierarchical netlist**, the definitions of `sub_module1` and `sub_module2` are **preserved as separate modules**.
* In the **flattened netlist**, the **hierarchy is removed**.

  * The logic inside the submodules is **inlined** into the top-level module.
  * You directly see the **AND** and **OR** gate instantiations within `multiple_modules`.

![Screenshot 2025-07-10 160427](https://github.com/user-attachments/assets/2dace79d-f0c1-41c2-bf16-4638393dbcb8)

![Screenshot 2025-07-10 160246](https://github.com/user-attachments/assets/f4402877-7346-4655-a41a-31982256573e)

use command show to see the graphyical representation

```yosys
show
```
![Screenshot 2025-07-10 161512](https://github.com/user-attachments/assets/1dbf7f23-dbfd-4e28-a565-6736858ae9d5)

---

### **Conclusion**

Flattening simplifies the structure for downstream tools and allows better optimization, but it also removes modular boundaries, making the design harder to interpret manually.

---

### **Submodule-Level Synthesis**

Let’s now perform **synthesis at the submodule level**, taking `sub_module1` (instance `u1`) as an example.

#### **Yosys Commands:**

```yosys
read_liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog multiple_modules.v
synth -top sub_module1
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show
```
![Screenshot 2025-07-10 162957](https://github.com/user-attachments/assets/b79a96c2-df3b-4269-9438-6c37dd565e1b)

![Screenshot 2025-07-10 163123](https://github.com/user-attachments/assets/07edd3cf-00ef-46de-9ec6-4465440bfd08)

![Screenshot 2025-07-10 163216](https://github.com/user-attachments/assets/7c78eeea-f202-41cb-9852-51b393ee5558)

![Screenshot 2025-07-10 163255](https://github.com/user-attachments/assets/14eaa288-2e57-420e-a0a4-a722261ae945)

---

### **What Do We See?**

Since we’ve explicitly specified `sub_module1` as the top module, Yosys synthesizes **only this module**, which is a simple **AND gate**.

* The visualization (`show`) displays just the **AND gate logic**.
* You will **not see `sub_module2`** or the top-level module `multiple_modules`.

---

### **Why Perform Submodule-Level Synthesis?**

Submodule-level synthesis is useful in several scenarios:

#### **1. Reuse of Repeated Logic**

* Consider a design where the top-level module contains **six instances of a multiplier**.
* Instead of synthesizing the multiplier logic **six times**, we can:

  * Synthesize the multiplier module **once**
  * **Reuse** that synthesized instance multiple times in the top module
* This improves **efficiency**, **reduces redundancy**, and saves **time and resources**.

#### **2. Divide and Conquer Approach**

* For **large or complex designs**, it's more practical to:

  * Synthesize individual submodules independently
  * Then integrate them into the full system
* This approach is scalable and simplifies **debugging**, **timing analysis**, and **modular development**.

---

### **Conclusion**

Submodule-level synthesis allows:

* **Efficient handling** of repeated instances
* Easier **modular design and optimization**
* A scalable method for managing **large-scale digital systems**

---
##
---
###
---

### **Given:**

Expression:

```
Y = (A & B) | C
```

### **Gate Delays:**

* AND gate = **2 ns**
* OR gate = **1 ns**

---

### **Input Transitions at t = 0 ns:**

| Signal | Transition    |
| ------ | ------------- |
| A      | 0 → 1 at 0 ns |
| B      | 0 → 1 at 0 ns |
| C      | 1 → 0 at 0 ns |

---

### **Initial Values (before 0 ns):**

* A = 0
* B = 0
* C = 1
  → (A & B) = 0
  → Y = 0 | 1 = **1**

Now let’s analyze what happens **after time = 0 ns**.

---

### **Step-by-Step Timing:**

#### **Time = 0 ns**

* A and B start transitioning from 0 → 1
* C starts transitioning from 1 → 0

#### **Time = 1 ns**

* OR gate sees C = 0
  → It sees (A & B) = **still 0** (AND hasn't produced output yet — 2 ns delay)
  → OR gate evaluates: `0 | 0 = 0`
  → **Y falls to 0** → **glitch**

#### **Time = 2 ns**

* AND gate output becomes 1 (A=1, B=1)
* OR gate sees: `1 | 0 = 1`
  → Y returns to 1

---

### **Waveform**

![image](https://github.com/user-attachments/assets/287b99d2-b2ae-46ce-a503-28aa9ac7b920)

---

### **Conclusion:**

* Y was initially **1**
* Due to all signals changing simultaneously, the OR gate **briefly saw both inputs as 0** at 1 ns:

  * AND gate hadn't responded yet
  * C had already dropped to 0
* So **Y glitched** to 0, then returned to 1 after AND gate output arrived
* This is a **Static-1 hazard**, caused by **unbalanced path delays**

---

### **Why We Need a Flip-Flop in Digital Circuits**

In a **purely combinational circuit**, outputs respond directly to input changes — including glitches caused by signal delays. If there is no mechanism to control when outputs are sampled or updated, **glitches may propagate continuously**, preventing the output from ever settling. This is undesirable, especially in sequential digital systems.

---

### **Role of Flip-Flops**

To solve this problem, we introduce a **flip-flop** (typically a **D flip-flop**) — a **storage element** used to:

* **Capture and hold** the output of a combinational block
* **Restrict glitches** from propagating endlessly
* **Synchronize signal transitions** using a **clock edge**

The **D flip-flop updates its output only at a specific clock edge** (usually rising or falling), so:

* Even if the combinational logic is glitchy in between, the flip-flop **ignores** those changes
* It passes **only the final, stable value** to the next stage
* Thus, each stage in the circuit receives **stable inputs**, allowing the system to function reliably

---

### **Why Initialization Is Important**

If the **initial state** of a flip-flop is unknown (i.e., not set or reset), the output of the combinational logic **may evaluate incorrectly**, producing garbage values.

To avoid this:

* We **initialize** the flip-flop using a **reset** or **set** signal during startup
* This ensures the system starts from a **known, predictable state**

---
SKY130RTL D2SK3 L2 Why Flops and Flop coding styles part2
---
![WhatsApp Image 2025-07-12 at 19 07 29_9fdbf700](https://github.com/user-attachments/assets/543a755b-8899-45fe-b755-19e9146c9769)

![WhatsApp Image 2025-07-12 at 19 07 34_c758e502](https://github.com/user-attachments/assets/9265c24c-d36d-4ccc-a20e-c920d1046173)

![WhatsApp Image 2025-07-12 at 19 08 27_07462e6b](https://github.com/user-attachments/assets/10fe12ad-56d8-4694-ae1d-5ee622bcf00d)

---
### SKY130RTL D2SK3 L3 Lab flop synthesis simulations part1
---
Now lets simulate the following flops 
1) D FlipFlop with Asynchronous reset
2) D FlipFlop with Synchronous reset
3) D FlipFlop with Synchronous and Asynchronous reset
4) D FlipFlop with Asynchronous set

**1) D FlipFlop with Asynchronous reset**

<img width="2468" height="657" alt="Screenshot 2025-07-13 113250" src="https://github.com/user-attachments/assets/4b925fc8-c33b-4a61-8a35-faaae9858344" />

<img width="1531" height="1841" alt="Screenshot 2025-07-13 113344" src="https://github.com/user-attachments/assets/87e626f9-622f-446a-a2bb-756d769e7167" />

<img width="3838" height="2160" alt="Screenshot 2025-07-12 192545" src="https://github.com/user-attachments/assets/7f568421-7b4f-4b29-9b02-aa18e8f39465" />

Zoomed out waveform

<img width="3839" height="2159" alt="Screenshot 2025-07-12 192743" src="https://github.com/user-attachments/assets/6a8769d8-7a36-4282-8ca2-9ec1612007e5" />

Zooming at the point when reset changes from low to high

<img width="3839" height="2159" alt="Screenshot 2025-07-12 193027" src="https://github.com/user-attachments/assets/a0b06d49-72ec-4183-945d-3c2c39eede47" />

**2) D FlipFlop with Synchronous reset**

<img width="3075" height="591" alt="Screenshot 2025-07-13 113434" src="https://github.com/user-attachments/assets/b941fd73-e33b-4740-b05c-4da861c43bfb" />

<img width="1607" height="1617" alt="Screenshot 2025-07-13 113510" src="https://github.com/user-attachments/assets/fd59a134-d7b6-4225-95fa-4aee701c3d00" />

<img width="3838" height="2106" alt="Screenshot 2025-07-12 195332" src="https://github.com/user-attachments/assets/7a5b9b03-d367-4b54-bb5c-5d585e65f7eb" />

<img width="3838" height="2117" alt="Screenshot 2025-07-12 195852" src="https://github.com/user-attachments/assets/0277190a-6ed1-4939-8b17-eec084109245" />

<img width="3838" height="2160" alt="Screenshot 2025-07-12 195827" src="https://github.com/user-attachments/assets/0b63e386-56fc-43c8-9d71-673fd61c1a4b" />

**3) D FlipFlop with Synchronous and Asynchronous reset**

<img width="3340" height="670" alt="Screenshot 2025-07-13 113544" src="https://github.com/user-attachments/assets/6898f427-eef1-4c65-98d9-b30dc03d22e2" />

<img width="1760" height="1676" alt="Screenshot 2025-07-13 113624" src="https://github.com/user-attachments/assets/514cdab4-30d3-4c70-8359-c33bbe6d97fe" />

<img width="3838" height="2115" alt="Screenshot 2025-07-12 200247" src="https://github.com/user-attachments/assets/5b8a06e7-8593-4c84-ab5e-35fb73502564" />

<img width="3839" height="2119" alt="Screenshot 2025-07-12 200439" src="https://github.com/user-attachments/assets/1aa67ed3-0d37-43ad-bf9c-8b0cc78cff28" />

<img width="3839" height="2109" alt="Screenshot 2025-07-12 200550" src="https://github.com/user-attachments/assets/f68a6757-f7cd-4638-a6d7-e47125c42df0" />

<img width="3839" height="2114" alt="Screenshot 2025-07-12 201051" src="https://github.com/user-attachments/assets/bc43c50d-c700-401d-822d-ada4910fd15e" />

<img width="3839" height="2117" alt="Screenshot 2025-07-12 201122" src="https://github.com/user-attachments/assets/89bc27d5-1c87-46c2-920d-4f6f2c1216ac" />

**4) D FlipFlop with Asynchronous set**

<img width="2588" height="705" alt="Screenshot 2025-07-13 113700" src="https://github.com/user-attachments/assets/e49ecf70-45ec-4c57-999e-143490f427f1" />

<img width="1516" height="1616" alt="Screenshot 2025-07-13 113740" src="https://github.com/user-attachments/assets/762bf398-92db-4314-9daa-7a13a3195ac6" />

<img width="3838" height="2117" alt="Screenshot 2025-07-13 102619" src="https://github.com/user-attachments/assets/7ef519f8-8ec5-4a18-b372-f10ebb13f472" />

<img width="3838" height="2124" alt="Screenshot 2025-07-13 102732" src="https://github.com/user-attachments/assets/e88e694c-1b3f-45c5-81b1-e0c78c726900" />

<img width="3838" height="2151" alt="Screenshot 2025-07-13 102838" src="https://github.com/user-attachments/assets/49bacf1e-eb9c-46ed-b7cc-938f6ac6b1b6" />

<img width="3838" height="2115" alt="Screenshot 2025-07-13 103540" src="https://github.com/user-attachments/assets/c9f01b1a-979f-4065-a6dd-a7940cbfb6b8" />

---
### SKY130RTL D2SK3 L4 Lab flop synthesis simulations part2
---
Now let's synthesize the following D flipflops
1) D FlipFlop with Asynchronous reset
2) D FlipFlop with Synchronous reset
3) D FlipFlop with Synchronous and Asynchronous reset
4) D FlipFlop with Asynchronous set

### **1) D FlipFlop with Asynchronous reset**

**Why We Use `dfflibmap` in Synthesis Flow**

When performing logic synthesis using tools like **Yosys**, we typically use a standard cell library (`.lib` file) that contains both **combinational** and **sequential** cells (like D flip-flops). However, in many design flows, **flip-flops are provided in a separate library** from the main logic gates.

To handle this, we use the Yosys command:

```bash
dfflibmap -liberty ../lib/your_flipflop_library.lib
```

---
**What `dfflibmap` Does**

* It maps generic D flip-flop constructs (like `always @(posedge clk)` in RTL) to **specific standard cells** in the library.
* This is essential for **correct technology mapping** — otherwise, the tool may not know which flip-flop cell to use.
* It ensures **timing-aware synthesis** using the correct sequential elements.

---
**Typical Flow Including `dfflibmap`**

```bash
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog design.v
synth -top <top_module>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
<img width="3838" height="2160" alt="Screenshot 2025-07-13 105556" src="https://github.com/user-attachments/assets/4e7d1d83-c8c9-4942-b8bc-863e49795d1e" />

<img width="3838" height="2110" alt="Screenshot 2025-07-13 110713" src="https://github.com/user-attachments/assets/0f6acf5a-fac9-4114-9edb-78b861526ab7" />

<img width="3838" height="2115" alt="Screenshot 2025-07-13 110824" src="https://github.com/user-attachments/assets/0ce6792d-545c-48dc-bd62-4254c6b4a9da" />

<img width="3838" height="2160" alt="Screenshot 2025-07-13 110938" src="https://github.com/user-attachments/assets/1984c97e-5658-46d7-83e4-6aabaa3f86fd" />

<img width="3838" height="2112" alt="Screenshot 2025-07-13 111120" src="https://github.com/user-attachments/assets/aa77cee2-4a2e-4ec1-a876-155920014233" />

<img width="3838" height="2121" alt="Screenshot 2025-07-13 111052" src="https://github.com/user-attachments/assets/125cdfae-6a0d-4f49-9a24-8e824de3fa56" />

**Why the Tool Inserted an Inverter**

In the Verilog code, the D flip-flop is written with an **active-high reset** condition:

```verilog
if (reset)
    q <= 0;
```

However, the standard cell library may only contain **flip-flops with active-low reset** functionality.

To resolve this mismatch, the synthesis tool automatically inserts an **inverter** in front of the reset signal. This converts the active-high reset logic used in the RTL to match the **active-low reset behavior** expected by the physical flip-flop cell in the library.

---

**Why `dfflibmap` is Important**

* Without `dfflibmap`, the flip-flop may **not be mapped** correctly to a physical cell.
* This can result in either:

  * **Synthesis failure**
  * Or an **incomplete netlist** (no physical representation for your DFF)

---

### **2) D FlipFlop with Synchronous reset**

<img width="3838" height="2061" alt="Screenshot 2025-07-13 114542" src="https://github.com/user-attachments/assets/7d48c1ca-72ee-4871-999f-5b156cd2e58e" />

<img width="3838" height="2067" alt="Screenshot 2025-07-13 115048" src="https://github.com/user-attachments/assets/4796ed88-1bc8-4e81-90ed-3c98209c53e9" />

<img width="3838" height="2067" alt="Screenshot 2025-07-13 115134" src="https://github.com/user-attachments/assets/be259f87-b277-4631-a772-954cb767fdd7" />

<img width="3838" height="2117" alt="Screenshot 2025-07-13 115459" src="https://github.com/user-attachments/assets/c086a530-c32d-48f8-bc1c-d636bd6d74cb" />

![WhatsApp Image 2025-07-13 at 12 02 40_087389d9](https://github.com/user-attachments/assets/c59f3058-e53e-4170-9d0e-751c0b3e2ddc)

### **3) D FlipFlop with Synchronous and Asynchronous reset**

<img width="3838" height="2110" alt="Screenshot 2025-07-13 120630" src="https://github.com/user-attachments/assets/51686b36-e79e-4eff-bdde-b92a202d6422" />

<img width="3842" height="2115" alt="Screenshot 2025-07-13 120721" src="https://github.com/user-attachments/assets/b7ff9eac-5a56-4488-9b9f-fef035c6a7bf" />

<img width="3838" height="2103" alt="Screenshot 2025-07-13 120939" src="https://github.com/user-attachments/assets/a70f7166-1cd3-4644-9917-7e51966cd8d1" />

### **4) D FlipFlop with Asynchronous set**

<img width="3838" height="2065" alt="Screenshot 2025-07-13 121208" src="https://github.com/user-attachments/assets/80861ad3-04be-4107-8379-45b9a3f811f6" />

<img width="3845" height="2101" alt="Screenshot 2025-07-13 121305" src="https://github.com/user-attachments/assets/4c864882-cf1f-40bf-ba3c-a7d831d1b163" />

<img width="3838" height="2106" alt="Screenshot 2025-07-13 121533" src="https://github.com/user-attachments/assets/1b949a1b-248e-4292-962e-31de0dff0e38" />

---
### SKY130RTL D2SK3 L5 Interesting optimisations part1
---
### **Optimization Insight: Multiplication by Constant Power of 2**

We are examining an important optimization that synthesis tools automatically apply.

We will consider two Verilog RTL files: `mul2.v` and `mul8.v`. Open them together using:

```
gvim mul*.v -o
```

---

### **`mul2.v` – Multiply by 2**

```verilog
module mul2 (input [2:0] a, output [3:0] y);
    assign y = a * 2;
endmodule
```
![WhatsApp Image 2025-07-13 at 13 35 47_f902f42b](https://github.com/user-attachments/assets/ba22a63b-9d97-4c37-a37e-9f3385906d83)

This module multiplies a 3-bit input `a` by 2 and gives a 4-bit output `y`.

---

### **Optimization Insight**

At first glance, the multiplication operator (`*`) may suggest the need for a **hardware multiplier**. However, multiplying by 2 (or any power of 2) is simply a **bitwise left shift**(Hence after synthesizing the top module you will see that there are 0 cells inferred)

Example:

* $5 \times 4 = 20$
* $0101 \times 4 = 10100$ → This is just **shifting left by 2 bits**

Hence:

* Multiplication by 2 = shift left by 1 bit
* Multiplication by 4 = shift left by 2 bits
* Multiplication by $2^n$ = shift left by $n$ bits

---

### **Effect of Synthesis on `mul2`**

When we synthesize this module, the synthesis tool recognizes that:

```verilog
y = a * 2;
```

is equivalent to:

```verilog
y = a << 1;
```

<img width="3838" height="2103" alt="Screenshot 2025-07-13 130142" src="https://github.com/user-attachments/assets/fa4ce826-996e-4f65-a6df-891769bad102" />

<img width="3838" height="2115" alt="Screenshot 2025-07-13 130240" src="https://github.com/user-attachments/assets/f6dc1964-e1ed-4225-975b-2fc4331aa905" />

<img width="3838" height="2117" alt="Screenshot 2025-07-13 130428" src="https://github.com/user-attachments/assets/18f5fa98-f838-4f3d-8aa6-ff692964e1a8" />

<img width="3839" height="2108" alt="Screenshot 2025-07-13 130547" src="https://github.com/user-attachments/assets/d22303dc-2e1d-4c09-ab47-3723ba06804d" />

<img width="3845" height="2124" alt="Screenshot 2025-07-13 135730" src="https://github.com/user-attachments/assets/162f1019-a2b7-4979-ba1a-a90fdae5f1f0" />

<img width="3838" height="2160" alt="Screenshot 2025-07-13 135854" src="https://github.com/user-attachments/assets/9be00ada-7640-4f5d-b34d-7567eff7e051" />

<img width="3838" height="2119" alt="Screenshot 2025-07-13 135927" src="https://github.com/user-attachments/assets/d7b99870-8f64-43b2-969a-22eb2d831449" />


So instead of generating a multiplier, the tool simply wires the bits accordingly — **no actual multiplier hardware is required**.

This is a classic **strength reduction optimization** applied during synthesis.

---
### SKY130RTL D2SK3 L6 Interesting optimisations part2
---
### **Special case: Optimizing `y = a * 9` for `a[2:0]`**

We are considering the case:

```verilog
input  [2:0] a;
output [5:0] y;

assign y = a * 9;
```

---

### **Understanding the Multiplier**

Multiplying by 9 can be decomposed into a shift and add:

```
9 = 8 + 1 = (1 << 3) + 1
```

So:

```
a * 9 = (a << 3) + a
```

This means:

* `a << 3` is equivalent to appending **three 0s** at the right → forms `{a, 000}`
* Adding back `a` aligns it at LSB
* The total effect is **replicating `a` twice** in adjacent positions

---

### **Binary Form View**

Let `a = 3'babc`

* `a << 3` = `{a, 000}`
* Adding `a` to that gives: `{a, a}` → bits of `a` repeated

So:

```verilog
y = (a << 3) + a = {a, a} = {aa}
```

---

### **Conclusion**

Multiplying a 3-bit input `a` by 9 is equivalent to:

```
y = {a, a}
```

This optimization avoids the multiplier entirely by using a shift and add structure, and the result is simply **concatenating `a` with itself**.

**NOTE: only the name of the .v file is mul8 but its multiplying with 9**

<img width="3831" height="2110" alt="Screenshot 2025-07-13 140429" src="https://github.com/user-attachments/assets/ea1204de-137c-4eea-bcf3-bc728cf91e65" />

<img width="3838" height="2108" alt="Screenshot 2025-07-13 140602" src="https://github.com/user-attachments/assets/1fc2160b-d684-4599-a41f-1b6a7c99bd64" />

<img width="3840" height="2115" alt="Screenshot 2025-07-13 140659" src="https://github.com/user-attachments/assets/2754d618-75f2-4186-92ca-e6bceebe2010" />

<img width="3838" height="2117" alt="Screenshot 2025-07-13 140805" src="https://github.com/user-attachments/assets/7b6f4fa1-2b01-4726-8c90-5e66b3b7dc45" />

<img width="3838" height="2112" alt="Screenshot 2025-07-13 140901" src="https://github.com/user-attachments/assets/c34f47c8-489c-4d3e-b81b-344a5f5b0771" />

<img width="3833" height="2106" alt="Screenshot 2025-07-13 141000" src="https://github.com/user-attachments/assets/b431d822-70b3-4281-8f66-39b626a0b994" />

<img width="3838" height="2115" alt="Screenshot 2025-07-13 141235" src="https://github.com/user-attachments/assets/ed4d3fdc-936d-4c32-84b6-504dc2c13990" />

<img width="3838" height="2101" alt="Screenshot 2025-07-13 141303" src="https://github.com/user-attachments/assets/48b2b334-cc6a-4563-88fc-fb5eb6d655f2" />

---
# Day 3 - Combinational and sequential optimizations
---
## Introduction to optimizations
---
### SKY130RTL D3SK1 L1 Introduction to optimisations part1
---

### **Combinational Logic Optimization**

The goal of combinational logic optimization is to simplify logic circuits to reduce **area**, **power**, and sometimes **delay**, without altering the functionality of the design.

Optimized logic is essential for efficient hardware implementation.

### **Key Techniques for Optimization**

#### **1. Constant Propagation (Direct Optimization)**

If a signal is driven by a constant value (0 or 1), parts of the logic can be simplified at compile time.
``
assign y = a & 1'b0;  // optimized to y = 0
assign z = b | 1'b1;  // optimized to z = 1
``
![WhatsApp Image 2025-07-13 at 16 36 20_b498fd2f](https://github.com/user-attachments/assets/b67bc0f4-f0e6-4db8-ac3b-9508a9481da1)

![WhatsApp Image 2025-07-13 at 16 37 45_13ec31f5](https://github.com/user-attachments/assets/0c2791a8-4da2-4ef6-afc6-2c076d5991ac)

#### **2. Boolean Logic Optimization**

This involves algebraic simplification of logic expressions using Boolean identities.

Two major techniques:

##### a) **Karnaugh Map (K-Map)**

* Visual method used for manual simplification of Boolean expressions (typically for up to 4 or 5 variables).
* Identifies common groups (1s) in a truth table to reduce logic expressions.

##### b) **Quine–McCluskey Method**

* Tabular algorithmic approach to minimize Boolean functions.
* Suitable for automation and systematic minimization.
* Handles more variables than K-map and provides a deterministic minimal form.

![WhatsApp Image 2025-07-13 at 16 44 28_f0e6ada4](https://github.com/user-attachments/assets/5f4d517d-4086-4433-ba5b-5af10cd64d27)

---

### **Conclusion**

Optimizing combinational logic reduces hardware cost and improves power efficiency. Techniques like **constant propagation**, **K-map**, and **Quine–McCluskey** are fundamental to achieving these improvements during synthesis.

---
### SKY130RTL D3SK1 L2 Introduction to optimisations part2
---
and
---
### SKY130RTL D3SK1 L3 Introduction to optimisations part3
---

### **Sequential Logic Optimization**

Sequential logic optimization targets designs that include **flip-flops, latches, and state machines**. The objective is to reduce **area**, **power**, or **improve timing** while maintaining the same sequential behavior.

---

### **Types of Sequential Logic Optimization**

#### **1. Basic Optimization**

* **Sequential Constant Propagation**
  Similar to constant propagation in combinational logic but applied across clocked elements.
  If a flip-flop is fed by a constant or becomes constant due to logic conditions, it and related logic may be eliminated.

![WhatsApp Image 2025-07-13 at 17 09 18_0e221334](https://github.com/user-attachments/assets/2e3200ee-1d8b-4c8f-bdd2-9367d01e2c55)

Y=1 always irrespective of clock or reset and this is because of sequential constant propagation  so effectively we do t need any of these gates
---

#### **2. Advanced Optimizations** *(Not covered in lab)*

* **State Optimization**
  Minimizing the number of states or encoding them more efficiently in a finite state machine (FSM).
  For example, using Gray code or one-hot encoding to reduce switching activity or logic size.

* **Retiming**
  Moving flip-flops across combinational logic boundaries without changing functionality to balance path delays.
  Helps in meeting timing constraints by redistributing the pipeline stages.

* **Sequential Logic Cloning (Floorplan-Aware Synthesis)**
  Duplicating certain sequential elements to reduce routing congestion or balance timing across regions of a chip.
  Typically applied during physical-aware synthesis when layout information is available.

---

### **Conclusion**

Sequential logic optimization helps improve timing, reduce area, and minimize power consumption. While basic techniques like **sequential constant propagation** are performed early in synthesis, **advanced methods** such as **retiming** and **FSM state optimization** are used in high-performance, layout-aware flows.

---
## Combinational logic optimizations
---
### SKY130RTL D3SK2 L1 Lab06 Combinational Logic Optimisations part1
---
and
---
### SKY130RTL D3SK2 L2 Lab06 Combinational Logic Optimisations part2
---

We will be using the following files for our lab based on optimization.

<img width="3838" height="2112" alt="Screenshot 2025-07-14 100626" src="https://github.com/user-attachments/assets/35800109-8bf5-4840-ba25-ab2e5e1d92bb" />

The verilog codes for the above modules is shown in the image below

<img width="3839" height="2114" alt="Screenshot 2025-07-14 103317" src="https://github.com/user-attachments/assets/58440671-bf1b-4418-818f-b978ab4f595d" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 103534" src="https://github.com/user-attachments/assets/ef08f7ad-ba51-4935-8b54-3f8e27791cec" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 103447" src="https://github.com/user-attachments/assets/a1c1f596-be4d-449c-b7b0-f4d37ef3b2f2" />

Trying to understand the optimization of the above verilog codes

![WhatsApp Image 2025-07-14 at 09 52 49_9df564a5](https://github.com/user-attachments/assets/946270bf-ff6c-4170-8578-b58fb39f5e3d)

![WhatsApp Image 2025-07-14 at 09 55 34_8f8c91e1](https://github.com/user-attachments/assets/41deff88-861f-4e21-87a7-ef01a6adb1ad)

![WhatsApp Image 2025-07-14 at 09 56 38_ed01a8e8](https://github.com/user-attachments/assets/bb452a6c-fce0-4043-9333-5e9355494c65)

Now, Synthesizing the above 

### **1) opt_check.v**

<img width="3834" height="2115" alt="Screenshot 2025-07-14 100755" src="https://github.com/user-attachments/assets/e3c475d8-34ff-49cd-a18f-a17666d91b34" />

<img width="3838" height="2119" alt="Screenshot 2025-07-14 101040" src="https://github.com/user-attachments/assets/de84bd95-c929-4c83-9191-05343ffe3cf5" />

<img width="3834" height="2106" alt="Screenshot 2025-07-14 101134" src="https://github.com/user-attachments/assets/4e374180-5369-47a6-9834-dc87c4cf1fc9" />

### **2) opt_check2.v**

<img width="3838" height="2108" alt="Screenshot 2025-07-14 101242" src="https://github.com/user-attachments/assets/a0c5221a-ded5-4639-9b71-cb0234d743f4" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 101357" src="https://github.com/user-attachments/assets/ddf17f65-f508-48b5-85ff-735bee7e86b7" />

<img width="3838" height="2108" alt="Screenshot 2025-07-14 101451" src="https://github.com/user-attachments/assets/89f95452-16c8-45ee-bacf-dd4c7933f88e" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 101524" src="https://github.com/user-attachments/assets/3d7ae64a-b4ff-41be-a9b0-b2f5a573e3ce" />

### **3) opt_check3.v**

<img width="3838" height="2106" alt="Screenshot 2025-07-14 101745" src="https://github.com/user-attachments/assets/94467df5-3998-4307-855b-8ed93a30d7f7" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 101830" src="https://github.com/user-attachments/assets/266fdb8f-7e55-4560-bb12-3fbab8bd3388" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 101930" src="https://github.com/user-attachments/assets/8bc023a4-11fb-4b02-87ff-6f3ccf5ea078" />

<img width="3838" height="2106" alt="Screenshot 2025-07-14 102015" src="https://github.com/user-attachments/assets/2d2926e7-6ad4-44a8-bf1e-5c954c6ca83f" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 102050" src="https://github.com/user-attachments/assets/f0107cb2-81af-493d-881f-66d623adfd18" />

### **4) opt_check4.v**

<img width="3838" height="2110" alt="Screenshot 2025-07-14 102200" src="https://github.com/user-attachments/assets/5c895160-377b-447d-8c91-74d4b7d1f758" />

<img width="3838" height="2106" alt="Screenshot 2025-07-14 102255" src="https://github.com/user-attachments/assets/984a68b6-8f94-44ee-bb5d-7735809cb62b" />

<img width="3838" height="2121" alt="Screenshot 2025-07-14 102403" src="https://github.com/user-attachments/assets/6472e1c1-63f1-423c-bcb8-168b048bc4e0" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 102442" src="https://github.com/user-attachments/assets/9f4d66b1-40b3-455b-aa39-d9d9e991090d" />

### **5) multiple_module_opt.v**

<img width="3838" height="2115" alt="Screenshot 2025-07-14 102553" src="https://github.com/user-attachments/assets/08dc9078-384f-4b83-a5f3-c40ecbcf8e8d" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 102712" src="https://github.com/user-attachments/assets/6fd17120-1e00-457a-9ef5-960b03660c4f" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 102804" src="https://github.com/user-attachments/assets/1f51d314-fcb2-4c15-a4c6-3fa28e2f7f39" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 102836" src="https://github.com/user-attachments/assets/afaf0980-8e90-4fc2-a170-c2aeccb5b224" />

### **6) multiple_module_opt2.v**

<img width="3838" height="2110" alt="Screenshot 2025-07-14 102933" src="https://github.com/user-attachments/assets/f2334d20-c7fa-45ee-a823-983642639348" />

<img width="3838" height="2106" alt="Screenshot 2025-07-14 103026" src="https://github.com/user-attachments/assets/0f7889fc-8770-4f72-a837-ea23cb4ab87f" />

<img width="3838" height="2121" alt="Screenshot 2025-07-14 103129" src="https://github.com/user-attachments/assets/a9b95430-2c07-417b-9df6-918acefe707b" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 103208" src="https://github.com/user-attachments/assets/c234e3c7-b6c2-40f1-9258-2e577a0d813d" />

---
## Sequential logic optimizations
---
### SKY130RTL D3SK3 L1 Lab07 Sequential Logic Optimisations part1
---
we will be working on the following verilog codes

<img width="3838" height="2110" alt="Screenshot 2025-07-14 122438" src="https://github.com/user-attachments/assets/0c2597b4-6917-4a11-b9a2-0cd011d833f4" />

### **1) dff_const1.v and dff_const2.v**

The image below shows the verilog codes

<img width="3838" height="2101" alt="Screenshot 2025-07-14 122735" src="https://github.com/user-attachments/assets/5f801ad7-6a26-4f69-8159-75427e1e27a2" />

## Module 1: `dff_const`

```verilog
module dff_const1 (
    input clk,
    input reset,
    output reg q
);

always @(posedge clk or posedge reset) begin
    if (reset)
        q <= 1'b0;
    else
        q <= 1'b1;
end

endmodule
```

### What it describes:

* An asynchronous reset D flip-flop:

  * When `reset` is high: `q` is set to `0` immediately.
  * When `reset` is low: on the rising edge of `clk`, `q` is set to `1`.

### Why this infers a flip-flop:

* `q` changes only on the rising edge of the clock or when reset is applied.
* It requires state storage: `q` holds its value between clock cycles.
* Therefore, synthesis infers a D flip-flop with asynchronous reset.

---

## Module 2: `dff_const2`

```verilog
module dff_const2 (
    input clk,
    input reset,
    output reg q
);

always @(posedge clk or posedge reset) begin
    if (reset)
        q <= 1'b1;
    else
        q <= 1'b1;
end

endmodule
```

### What it describes:

* Regardless of whether reset is high or not, and regardless of clock, `q` is always set to `1`.

### Why this does not infer a flip-flop:

* `q` is never functionally dependent on `clk` or `reset`. It is always assigned the constant value `1`.
* The synthesis tool detects that the output is fixed and will optimize it as:

  ```verilog
  assign q = 1'b1;
  ```
* Since there's no dynamic or conditional behavior, no memory element (flip-flop) is required.

---

## Comparison Summary

| Feature          | `dff_const1`              | `dff_const2`                  |
| ---------------- | ------------------------ | ----------------------------- |
| Depends on clock | Yes                      | No (value is always 1)        |
| Output changes   | Yes (based on clk/reset) | No (always 1)                 |
| Storage required | Yes (flip-flop needed)   | No (constant logic only)      |
| Synthesis result | D flip-flop inferred     | Constant logic (no flip-flop) |

---

## Final Verdict

* `dff_const` infers a D flip-flop because the output `q` depends on control signals and stores state.
* `dff_const2` does not infer a flip-flop because the output is constant and requires no sequential behavior. The synthesis tool will optimize it into a simple wire driving logic high.

![WhatsApp Image 2025-07-14 at 12 19 10_92af4d1a](https://github.com/user-attachments/assets/a0f67b35-8a6c-4403-8658-8b78936ee68c)

Now let's verify simulating and also synthesize the modules:

### **1) Simulation of dff_const1 and dff_const2**

<img width="3838" height="2119" alt="Screenshot 2025-07-14 123655" src="https://github.com/user-attachments/assets/fe23ed7a-ed19-4610-9883-15c02a9bb97c" />

<img width="3838" height="2110" alt="Screenshot 2025-07-14 123801" src="https://github.com/user-attachments/assets/8d74cb70-6b60-4721-83c2-f1ec4770c270" />

<img width="3838" height="2110" alt="Screenshot 2025-07-14 123929" src="https://github.com/user-attachments/assets/68b111a1-840a-49e4-934e-61180864f836" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 124020" src="https://github.com/user-attachments/assets/7f6e90e0-9e6c-49b0-a5e5-4141cd389f6c" />

### **1) Synthesis of dff_const and dff_const2**

<img width="3838" height="2108" alt="Screenshot 2025-07-14 124455" src="https://github.com/user-attachments/assets/aa0aeed8-39da-43aa-8ddb-9a1580c30888" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 124626" src="https://github.com/user-attachments/assets/5873095f-6ed8-4c9a-9ce6-69a12ef394aa" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 124716" src="https://github.com/user-attachments/assets/ebc55d04-9837-4106-b813-c148f15c1a8f" />

<img width="3838" height="2119" alt="Screenshot 2025-07-14 124759" src="https://github.com/user-attachments/assets/fa1341bd-74a1-46dc-ac05-89e2846f851b" />

<img width="3834" height="2124" alt="Screenshot 2025-07-14 124834" src="https://github.com/user-attachments/assets/ddc1990f-ad3c-410c-9d02-1e27da3f7f2c" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 124944" src="https://github.com/user-attachments/assets/c3cf71b8-9858-4f92-863b-ccc2ec1c381b" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 125014" src="https://github.com/user-attachments/assets/022077bb-2dc7-4dd5-ac79-2f86b537ad4d" />

<img width="3838" height="2108" alt="Screenshot 2025-07-14 125130" src="https://github.com/user-attachments/assets/1f85a921-3fc9-45bb-bdf4-bf57236eb5d0" />

<img width="3838" height="2110" alt="Screenshot 2025-07-14 125220" src="https://github.com/user-attachments/assets/bdab9025-bae1-4e59-923d-5116a153d4f6" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 125312" src="https://github.com/user-attachments/assets/f109412a-af2e-40c0-bdfa-23bc6fbc916c" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 125349" src="https://github.com/user-attachments/assets/cea71c59-fa95-4212-87d7-c7ca12be82b0" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 125501" src="https://github.com/user-attachments/assets/72b98285-442a-4dd7-913a-b8db4e762645" />

<img width="3838" height="2115" alt="Screenshot 2025-07-14 125536" src="https://github.com/user-attachments/assets/7f0b1324-42a5-4783-9462-fd5e21cb6f10" />

---
### SKY130RTL D3SK3 L2 Lab07 Sequential Logic Optimisations part2
---
and
---
### SKY130RTL D3SK3 L3 Lab07 Sequential Logic Optimisations part3
---

<img width="3838" height="2103" alt="Screenshot 2025-07-14 131951" src="https://github.com/user-attachments/assets/e259240e-bbb8-4eea-b43d-d4550341ff99" />


Let's analyze the Verilog code carefully and explain **why this infers two D flip-flops**, even though `q1` appears to take on a constant value.

---

### **Given Module:**

```verilog
module dff_const3 (
    input clk,
    input reset,
    output reg q
);

reg q1;

always @(posedge clk or posedge reset) begin
    if (reset) begin
        q  <= 1'b1;
        q1 <= 1'b0;
    end else begin
        q1 <= 1'b1;
        q  <= q1;
    end
end

endmodule
```
![WhatsApp Image 2025-07-14 at 13 18 23_d1d19859](https://github.com/user-attachments/assets/67df6e14-08f3-41c4-86d7-45cc17893da5)

---

### **Line-by-line Behavior**

#### When `reset` is high:

* `q` is set to `1`
* `q1` is set to `0`

#### On rising edge of `clk` (if reset is low):

* `q1` is set to `1`
* `q` is assigned the value of `q1` **from the previous clock cycle** (because assignments in non-blocking (`<=`) style happen in parallel and are registered only at the end of the block).

---

### **Key Insight:**

Although `q1` is **assigned a constant `1'b1` every cycle**, **`q` depends on the value of `q1`** from the **previous clock cycle**:

```verilog
q <= q1;
```

That means:

* `q1` must **hold** its value between clock cycles.
* `q` must **read** that held value.
* Hence, both `q1` and `q` **require state**.

---

### **Why Two Flip-Flops Are Inferred**

Even though `q1` is always set to `1'b1` in the `else` block:

* `q1` is still **used as a register** (i.e., its value is needed across cycles for `q <= q1;`)
* This means it **cannot** be replaced by a constant logic high (`1'b1`) during synthesis.
* The tool **cannot optimize `q1` away** because its **past value is used** (delayed assignment behavior).

So:

* `q1` → needs a flip-flop to store `1` across cycles.
* `q` → also needs a flip-flop, since it depends on `q1`.

---

### **Conclusion**

Even though `q1` is assigned a constant value (`1'b1`), the fact that `q <= q1;` creates a **sequential dependency** on `q1`’s previous value. Therefore:

* The tool **cannot propagate the constant** through `q1`
* It **infers two flip-flops**: one for `q1`, one for `q`

This is a classic case where **sequential constant propagation fails** due to **temporal dependency**.

### **Simulation of the module dff_const3**

<img width="3838" height="2108" alt="Screenshot 2025-07-14 132703" src="https://github.com/user-attachments/assets/479ef4b5-653f-495f-b074-2e79439bcd86" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 132831" src="https://github.com/user-attachments/assets/45b35e4f-2259-4360-a338-a1539b1dd166" />

### **Synthesizing the module dff_const3**

<img width="3838" height="2115" alt="Screenshot 2025-07-14 132950" src="https://github.com/user-attachments/assets/2c75a4af-85fa-400a-b29b-549f4a327f1f" />

<img width="3838" height="2119" alt="Screenshot 2025-07-14 133040" src="https://github.com/user-attachments/assets/5a6d471a-5568-40e7-a8c6-b85ca7cd06f6" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 133125" src="https://github.com/user-attachments/assets/421ee75d-53ec-494e-a427-f7e0bed90d99" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 133204" src="https://github.com/user-attachments/assets/081c5a5e-d12e-4bfc-92f0-51b4ed7be5ed" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 133241" src="https://github.com/user-attachments/assets/b4412237-29e2-42f4-a1d1-1ddf07a74b14" />

### **4) dff_const4**

<img width="3839" height="2108" alt="Screenshot 2025-07-14 134628" src="https://github.com/user-attachments/assets/50e47d59-310e-48aa-b795-fd859e37e07f" />

### Module: `dff_const4`

```verilog
module dff_const4 (
    input clk,
    input reset,
    output reg q
);

reg q1;

always @(posedge clk or posedge reset) begin
    if (reset) begin
        q  <= 1'b1;
        q1 <= 1'b1;
    end else begin
        q1 <= 1'b1;
        q  <= q1;
    end
end

endmodule
```

---

### Behavioral Analysis

#### During reset:

* `q1` is set to `1'b1`
* `q` is set to `1'b1`

#### On every clock edge:

* `q1` is again assigned `1'b1`
* `q` is assigned the value of `q1`

Now observe the following:

* `q1` is **always** set to `1'b1`, regardless of reset or clock.
* `q` is set to `q1`, which is **always** `1'b1`.

So in functional terms, the entire block is just forcing both `q` and `q1` to be `1'b1` at all times.

---

### Synthesis Tool Perspective

* The synthesis tool recognizes that `q1` is assigned a constant `1'b1` in all cases.
* It replaces all usage of `q1` with `1'b1`.
* Then `q <= q1` becomes `q <= 1'b1`, which is also constant.

Since neither `q` nor `q1` depends on prior values or time-varying logic, **no memory elements** (flip-flops) are needed. The tool will optimize both out and directly tie `q` to logic high.

---

### Conclusion

* `q1` is a **sequential constant**, always `1'b1`.
* `q` is also set to that same constant value.
* There is **no true state-holding behavior**.
* Therefore, **no D flip-flops are inferred**.

The synthesis tool will reduce the entire design to something like:

```verilog
assign q = 1'b1;
```

---

### Summary Table

| Signal | Assignment        | Varies with Time? | Needs Flip-Flop? | Reason                      |
| ------ | ----------------- | ----------------- | ---------------- | --------------------------- |
| `q1`   | Always `1'b1`     | No                | No               | Constant value              |
| `q`    | Assigned `q1` (1) | No                | No               | Also constant after folding |

This module is fully optimized to a constant logic high, and **no sequential logic** remains after synthesis.

### **Simulation of the module dff_const4**

<img width="3838" height="2117" alt="Screenshot 2025-07-14 134745" src="https://github.com/user-attachments/assets/051a2866-1727-47e2-8c8a-be97245eaea8" />

<img width="3838" height="2106" alt="Screenshot 2025-07-14 134828" src="https://github.com/user-attachments/assets/126d6531-1a6c-4208-83be-03eb17518d90" />

### **Synthesizing the module dff_const4**

<img width="3838" height="2106" alt="Screenshot 2025-07-14 133759" src="https://github.com/user-attachments/assets/3a02615a-d9c3-4562-9491-dfcd2280933e" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 133837" src="https://github.com/user-attachments/assets/1aa904f5-4b53-4113-baab-1de07410213b" />

<img width="3838" height="2119" alt="Screenshot 2025-07-14 133916" src="https://github.com/user-attachments/assets/e610ff3f-c9e6-4b48-9866-6ec831d739f0" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 133955" src="https://github.com/user-attachments/assets/4068bca8-edb0-4362-bddc-8cd4f31268f1" />

### **5) dff_const5**

<img width="3838" height="2106" alt="Screenshot 2025-07-14 134646" src="https://github.com/user-attachments/assets/e0a7bec3-03c4-4cfc-bb73-d27a21a8777d" />

### Verilog Module: `dff_const`

```verilog
module dff_const (
    input clk,
    input reset,
    output reg q
);

reg q1;

always @(posedge clk or posedge reset) begin
    if (reset) begin
        q  <= 1'b0;
        q1 <= 1'b0;
    end else begin
        q1 <= 1'b1;
        q  <= q1;
    end
end

endmodule
```

---

### Understanding the Behavior

#### During `reset`:

* `q1` is assigned `0`
* `q` is assigned `0`

#### During normal clocked operation (`reset == 0`):

* `q1` is assigned `1`
* `q` is assigned the **previous value** of `q1`

This is the key:
Due to **non-blocking assignments (`<=`)**, the assignment `q <= q1;` uses the value of `q1` **from the previous clock cycle**, not the new value being assigned in the same block.

---

### Why Two D Flip-Flops Are Inferred

Even though `q1` always eventually holds `1`, the tool **cannot optimize it away** because:

* `q` depends on the **prior value** of `q1`
* This is a classic case of **sequential dependency**

Thus:

* `q1` must be a flip-flop (to hold its value from cycle to cycle)
* `q` must be another flip-flop (to store that delayed value)

---

### Summary Table

| Signal | Behavior                | Flip-Flop Needed | Reason                            |
| ------ | ----------------------- | ---------------- | --------------------------------- |
| `q1`   | 0 on reset, then 1      | Yes              | Must hold value across cycles     |
| `q`    | Delayed version of `q1` | Yes              | Depends on previous value of `q1` |

---

### Final Conclusion

Yes, this module **infers two D flip-flops**:

1. One for `q1` (holding a value that becomes constant after reset but is still sequential)
2. One for `q` (dependent on the value of `q1` from the previous clock cycle)

The synthesis tool **cannot collapse `q1` into a constant**, because it's part of a chain of sequential logic.

### **Simulation of the module dff_const5**

<img width="3838" height="2115" alt="Screenshot 2025-07-14 134913" src="https://github.com/user-attachments/assets/084d0e5d-9719-452c-b743-abe714f49542" />

<img width="3838" height="2108" alt="Screenshot 2025-07-14 134955" src="https://github.com/user-attachments/assets/c428eebf-98d4-46ac-883d-809034a12edc" />

### **Synthesizing the module dff_const5**

<img width="3838" height="2115" alt="Screenshot 2025-07-14 134151" src="https://github.com/user-attachments/assets/6ffb3643-69b2-449e-b8ac-cb6e66b03b5e" />

<img width="3838" height="2110" alt="Screenshot 2025-07-14 134230" src="https://github.com/user-attachments/assets/30f05b6f-0254-478c-be1b-d120f0082354" />

<img width="3838" height="2112" alt="Screenshot 2025-07-14 134333" src="https://github.com/user-attachments/assets/62fc339a-3d98-49ca-92ff-e719e795f826" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 134501" src="https://github.com/user-attachments/assets/e19cbd2d-2016-4822-8374-bb8de7ed7fcb" />

<img width="3838" height="2117" alt="Screenshot 2025-07-14 134543" src="https://github.com/user-attachments/assets/56d6ed61-1d06-4ad4-84a5-1f29e3e6965a" />

---
## Sequential optimzations for unused outputs
---
### SKY130RTL D3SK4 L1 Seq optimisation unused outputs part1
---

<img width="3839" height="2110" alt="Screenshot 2025-07-14 160419" src="https://github.com/user-attachments/assets/ef4b6e56-1752-4b07-8c2f-c7d84e1bab7e" />

### **Verilog Code: `counter_opt`**

```verilog
module counter_opt (
    input clk,
    input reset,
    output q
);

reg [2:0] count;
assign q = count[0];

always @(posedge clk or posedge reset) begin
    if (reset)
        count <= 3'b000;
    else
        count <= count + 1;
end

endmodule
```

---

### **What the Code Does**

* This is a **3-bit up counter**.
* Internally, it increments `count` on every clock cycle.
* However, **only `count[0]`** is exposed as the output (`q`).
* The other two bits `count[1]` and `count[2]` are **never used** in any computation or output.

---

### **Synthesis Tool Behavior**

* The synthesis tool performs **optimization** based on what parts of the logic contribute to the **primary outputs**.
* Since `count[1]` and `count[2]` are **not used**:

  * They do **not affect any observable behavior**.
  * So the tool will **remove the logic** related to them.
* As a result, the tool infers:

  * **Only one D flip-flop**, for `count[0]`
  * The remaining two flip-flops are **optimized out**

---

### **Key Principle:**

> **Any internal logic or signal that does not influence a primary output or observable side-effect will be eliminated during synthesis.**

This is called **unused logic optimization** or **dead code elimination**.

---

### **Conclusion**

Even though the RTL describes a 3-bit counter, the synthesis tool:

* Recognizes that only `count[0]` contributes to the output.
* Eliminates `count[1]` and `count[2]`.
* Implements **only a 1-bit counter** with a **single flip-flop**.

This demonstrates how synthesis tools perform **output-driven optimization**, and reinforces why **unused logic should be avoided in real designs** unless intentionally preserved through constraints.

![WhatsApp Image 2025-07-14 at 15 57 20_b26d6045](https://github.com/user-attachments/assets/4c27b082-0c12-4dfa-ba29-4825ad0ea786)

<img width="3838" height="2115" alt="Screenshot 2025-07-14 160829" src="https://github.com/user-attachments/assets/8fecb373-7e7b-4752-800f-94af6ed4cfd6" />

<img width="3838" height="2106" alt="Screenshot 2025-07-14 160925" src="https://github.com/user-attachments/assets/44bdca4c-f7e3-4ac7-81e3-c52c1fb54771" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161016" src="https://github.com/user-attachments/assets/0468e9fa-933d-4836-9971-34c2dc81483a" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161105" src="https://github.com/user-attachments/assets/93dc7bbf-2a44-4ea2-a637-32e55b20a817" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161144" src="https://github.com/user-attachments/assets/80e08ff3-e7c6-414b-9c97-c2876e4c398f" />

If assign q= (count[2:0] == 3'100)

<img width="3838" height="2106" alt="Screenshot 2025-07-14 160719" src="https://github.com/user-attachments/assets/1f2c46db-3c7e-4e94-b009-9e0cc0c2640d" />

```verilog
q = (count[2:0] == 3'b100);
```

**forces all 3 D flip-flops to be inferred**, using synthesis reasoning.

---

### **Updated Code**

```verilog
module counter_opt (
    input clk,
    input reset,
    output q
);

reg [2:0] count;
assign q = (count == 3'b100);

always @(posedge clk or posedge reset) begin
    if (reset)
        count <= 3'b000;
    else
        count <= count + 1;
end

endmodule
```

---

### **What Changed?**

In this version:

* The output `q` is no longer just `count[0]`.
* Instead, it is a **combinational comparison** of the entire 3-bit `count` value with `3'b100`.
* So now, `q` depends on **all three bits**: `count[0]`, `count[1]`, and `count[2]`.

---

### **Impact on Synthesis**

* Since the output `q` uses **all 3 bits**, the synthesis tool **cannot remove** any part of the `count` register.
* Each bit of `count` is **functionally necessary** to compute `q`.
* As a result:

  * All **3 D flip-flops** for `count[2:0]` are preserved.
  * No optimization of unused bits is possible.

---

### **Conclusion**

> When all bits of a register contribute to an output (like in a comparison), the synthesis tool must keep the full register, and all associated flip-flops are inferred.

This contrasts with the earlier case where `q = count[0]`, in which the tool eliminated unused flip-flops due to **partial usage** of the register.

---

### **Summary**

| Output Expression       | Flip-Flops Inferred | Reason                                                  |
| ----------------------- | ------------------- | ------------------------------------------------------- |
| `q = count[0]`          | 1                   | Only `count[0]` is needed; others optimized away        |
| `q = (count == 3'b100)` | 3                   | All 3 bits are used in output; no optimization possible |


<img width="3840" height="2160" alt="Screenshot 2025-07-14 161332" src="https://github.com/user-attachments/assets/d2052269-97ce-4ca2-9b35-53186e23fcf1" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161417" src="https://github.com/user-attachments/assets/e8c29857-926e-433d-8c06-7ebb6d9cac35" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161459" src="https://github.com/user-attachments/assets/f939f550-bd13-4fb1-9fbc-506d0062e6d9" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161534" src="https://github.com/user-attachments/assets/4ba9271f-356b-4157-8586-5bc2da7f9184" />

<img width="3840" height="2160" alt="Screenshot 2025-07-14 161623" src="https://github.com/user-attachments/assets/51ba39da-fe9b-4850-bcd8-5faa296b452a" />

---
# Day 4 - GLS, blocking vs non-blocking and Synthesis-Simulation mismatch
---
## GLS, Synthesis-Simulation mismatch and Blocking/Non-blocking statements
---
### SKY130RTL D4SK1 L1 GLS Concepts And Flow Using Iverilog
---

### **Introduction to Gate Level Simulation (GLS)**

When we write RTL code, we verify its functional correctness using a **testbench**. This process is known as **RTL simulation**.

In **Gate Level Simulation**, we run the **same testbench**, but instead of simulating the RTL code, we simulate the **netlist** — the gate-level version of the design generated after synthesis.

---

### **Why GLS is Needed**

1. **Logical Verification After Synthesis**
   Although the netlist is functionally equivalent to the RTL, synthesis tools may perform optimizations. GLS ensures that **no logical errors** were introduced during synthesis.

2. **Timing Verification**
   RTL simulation is functional but does not model actual delays. GLS helps verify that the **timing constraints are met**, especially when run with **delay annotation** (typically from SDF files). This ensures that the circuit works as expected **at the target clock frequency**.

---

### **Key Points**

* **Testbench Compatibility**:
  Since the netlist has the same ports as the RTL, it fits directly into the RTL testbench without changes.

* **Timing-Accurate Simulation**:
  With delay annotation, GLS reflects the real-world delays caused by gates, wires, and interconnects.

---

### **Summary**

Gate Level Simulation is the step where:

* We **validate the post-synthesis design**.
* Ensure **logical correctness**.
* Check **timing** with annotated delays.
* All using the **same testbench** written for RTL.

It serves as the final check before proceeding to physical design or fabrication.

### **Gate Level Simulation (GLS) using Icarus Verilog (iverilog)**

<img width="3840" height="2160" alt="Screenshot 2025-07-14 164037" src="https://github.com/user-attachments/assets/510e839f-bb80-4507-a03d-7ac33d2a68c3" />

#### **Components in the Setup:**

1. **Design**
   This is the synthesized **netlist**, which contains only logic gates.

2. **Gate Level Verilog Models**
   These define the behavior of standard cells (like AND, OR, DFF, etc.).
   They are essential because the netlist uses gate-level primitives, and `iverilog` needs to understand their functionality during simulation.

3. **Testbench**
   Provides stimulus to the design and checks the outputs.
   The same testbench used for RTL simulation can be reused, since the netlist ports match those of the RTL.

4. **iverilog**
   Compiles the testbench, the synthesized gate-level netlist, and the gate-level Verilog models.
   It generates a **VCD file** (Value Change Dump), which records the transitions of signals during simulation.

5. **gtkwave**
   This tool is used to visualize the signal waveforms from the VCD file.
   It helps in analyzing the behavior of the design over time.

---

### **Key Note (from the Diagram)**

> If the gate-level models are delay-annotated, then Gate Level Simulation can be used for **timing validation**, in addition to logic verification.

---

### **Important Point**

* The netlist alone is not sufficient for simulation — it does not describe the internal behavior of gates.
* **Gate-level models must be included** so that `iverilog` can understand and simulate the logic elements used in the netlist.

---

### **Conclusion**

Gate Level Simulation using `iverilog` ensures:

* Functional correctness after synthesis.
* Timing verification (if delays are annotated).
* A clear path from RTL to hardware by simulating exactly what was synthesized.

---
### SKY130RTL D4SK1 L2 Synthesis Simulation Mismatch
---
### **Synthesis-Simulation Mismatch**

1) Missing Sensitivity List
2) Blocking vs non blocking assignments
3) Non standard verilog coding 

### **1) Missing Sensitivity List**

#### **Issue Overview:**

This is a common source of simulation and synthesis mismatch in Verilog designs. The simulator responds to activity or changes on signals. If a signal is not listed in the sensitivity list of an `always` block, then changes in that signal will not trigger re-evaluation of the block during simulation.

---

<img width="2010" height="2050" alt="Screenshot 2025-07-14 185705" src="https://github.com/user-attachments/assets/1fa9b864-4439-4b9a-ad71-11b1b34f26a5" />
 
#### **Problematic Code:**

```verilog
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
```

In this code:

* The `always` block is only sensitive to `sel`.
* If `i0` or `i1` changes while `sel` remains constant, the block is not re-evaluated.
* As a result, `y` does not reflect the changes in `i0` or `i1`, even though it should.
* This causes the output `y` to appear static or incorrectly held, which resembles latch-like behavior.
* It behaves as a latch instead of MUX.

---

#### **Simulator vs Synthesis Behavior:**

* **Simulator** behaves based on signal changes. Since `i0` and `i1` are not in the sensitivity list, their changes are ignored.
* **Synthesis tools**, however, infer the correct multiplexer logic because they analyze the complete logic structure.

This results in a mismatch: the synthesized hardware behaves correctly, but the simulated output does not.

---

#### **Corrected Code:**

```verilog
always @(*)  // Correct sensitivity list
begin
    if (sel)
        y = i1;
    else
        y = i0;
end
```

* Using `@(*)` instructs the simulator to automatically include all right-hand side signals (`sel`, `i0`, `i1`) in the sensitivity list.
* This ensures that the always block is evaluated whenever any of the involved signals change, leading to correct and expected simulation behavior.

---
### SKY130RTL D4SK1 L3 Blocking And NonBlocking Statements In Verilog
---
### **2) Blocking vs non blocking assignments**
---
### **Blocking (`=`) vs Non-blocking (`<=`) Assignments in Verilog**

#### **1. Inside an `always` block:**

* **Blocking (`=`):**
  Executes statements **sequentially** — each statement blocks the next until it's done. This models **combinational** logic or procedural code flow.

* **Non-blocking (`<=`):**
  All right-hand side (RHS) expressions are **evaluated in parallel** at the start of the time step, and the values are assigned to the left-hand side (LHS) **at the end of the time step**. This models **sequential logic** (flip-flops).

---

### **2. Caveats with Blocking Assignments in Sequential Logic**

Let’s analyze two versions of the code provided:

---

#### **Correct Use of Blocking (Modeling Two DFFs):**

```verilog
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
```

* In the `else` block:

  * `q = q0;` is executed **first**
  * Then `q0 = d;` is executed
* Since `q` gets the **previous value** of `q0`, this mimics two separate flip-flops:

  * `q0` stores `d`
  * `q` stores the previous `q0`

This correctly models **two D flip-flops**.

---

#### **Incorrect Ordering – Leads to Single Flip-Flop:**

```verilog
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
```

* In this version:

  * `q0 = d;` is executed **before**
  * `q = q0;` — now `q` just copies `d` because `q0` was already updated.
* So both `q` and `q0` carry the **same value** → only **one flip-flop** inferred.

This leads to incorrect synthesis where **only one DFF** is inferred, despite needing two.

---

### **Conclusion:**

| **Aspect**        | **Blocking (`=`)**               | **Non-blocking (`<=`)**       |
| ----------------- | -------------------------------- | ----------------------------- |
| Evaluation        | Sequential                       | Parallel                      |
| Common Use Case   | Combinational logic              | Sequential logic (flip-flops) |
| Assignment Timing | Immediate                        | End of time step              |
| Pitfall           | Can result in incorrect hardware | Safer for clocked logic       |

---

### **Best Practice:**

* Use **non-blocking (`<=`)** for **sequential** logic (in `always @(posedge clk)` blocks).
* Use **blocking (`=`)** only for **combinational** logic (in `always @(*)` blocks).

This ensures clarity in simulation and synthesizes accurate and intended hardware.

---
### SKY130RTL D4SK1 L4 Caveats With Blocking Statements
---

### Version 1 – With Non-blocking Assignments

```verilog
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
```

**Explanation:**

* When non-blocking assignments (`<=`) are used, both `q <= q0;` and `q0 <= d;` are evaluated in parallel. The right-hand side (RHS) values are captured first, and the assignments happen at the end of the clock edge.
* Therefore:

  * `q` receives the previous value of `q0`
  * `q0` receives the new value of `d`
* This infers two D flip-flops:

  * One for storing `d` (q0)
  * One for storing `q0` (q)
* This properly represents a two-stage pipeline.

---

### Version 2 – Reversed Assignment Order

```verilog
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
```

**Explanation:**

* Although the order of statements is reversed, non-blocking assignments ensure correctness.
* Both RHS expressions are evaluated before any assignment:

  * `q0` gets the current value of `d`
  * `q` gets the previous value of `q0`
* This again infers two flip-flops, and the behavior is consistent with expected pipeline logic.

---

### Summary Table

| Code Version      | Blocking (`=`)    | Non-blocking (`<=`) |
| ----------------- | ----------------- | ------------------- |
| `q = q0; q0 = d;` | Correct           | Correct             |
| `q0 = d; q = q0;` | Incorrect (1 DFF) | Correct (2 DFFs)    |

---

### Conclusion:

Using non-blocking assignments (`<=`) in sequential logic:

* Ensures the right number of flip-flops are inferred
* Maintains logical correctness regardless of statement order
* Prevents unintended synthesis mismatches
* Leads to clean simulation results and consistent behavior across design tools

This is the recommended style for writing clocked logic in Verilog.

---
### **synthesis-simulation mismatch**

The code you provided illustrates a **synthesis-simulation mismatch** caused by using **blocking assignments (`=`)** in the wrong order.

### **Objective:**

Implement the logic:
`y = (a | b) & c`
That is, the output of an **OR gate** with inputs `a` and `b` is connected to one input of an **AND gate**, and `c` is the other input.

---

### **Version 1 – Incorrect Order (Causes Mismatch)**

```verilog
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
```

#### **Problem:**

* `y` is computed **before** `q0` is updated.
* Since blocking assignments execute sequentially, `q0` still holds the **previous** value when used in `y = q0 & c`.
* In simulation, this behaves as though `q0` is a **register** or **flip-flop**, even though there's no clock — this is **not synthesizable** as intended.
* Synthesis tools will still treat `q0` as combinational, leading to a **mismatch** between simulation and synthesized hardware.

---

### **Version 2 – Correct Order**

```verilog
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
```

#### **Explanation:**

* Here, `q0` is assigned **before** it is used to compute `y`.
* Since this is combinational logic and uses blocking assignments in the **correct order**, the circuit will simulate and synthesize correctly.
* The synthesized circuit will now have:

  * One OR gate computing `q0 = a | b`
  * One AND gate computing `y = q0 & c`

This matches the intended logic `y = (a | b) & c`.

---

### **Conclusion:**

| Aspect                | Incorrect Version              | Correct Version                      |          |                         |
| --------------------- | ------------------------------ | ------------------------------------ | -------- | ----------------------- |
| Assignment Order      | `y = q0 & c;` before \`q0 = a  | b;\`                                 | \`q0 = a | b;`before`y = q0 & c;\` |
| Behavior              | Uses old/undefined `q0`        | Uses current value of `q0`           |          |                         |
| Simulation Result     | May appear as sequential logic | Matches intended combinational logic |          |                         |
| Synthesis Result      | Combinational logic            | Combinational logic                  |          |                         |
| Match Between Sim/Syn | No                             | Yes                                  |          |                         |

**Best Practice:**
When using **blocking assignments** in **combinational `always @(*)` blocks**, always ensure the **data dependencies** are ordered correctly.
Alternatively, avoid intermediate variables if not needed, or write the logic in a single expression.

Due to errors like the above, we must do GLS and verify that our design will work as expected. Next, we will perform labs based on GLS.
---
---
## Labs on GLS and Synthesis-Simulation Mismatch
---
### SKY130RTL D4SK2 L1 Lab GLS Synth Sim Mismatch part1
---
### **1) Simulating and synthesizing ternary_operator_mux.v**

The **ternary operator** is commonly used in Verilog to implement a **2:1 multiplexer (MUX)** in a concise, combinational form.

---

### **Syntax of Ternary Operator:**

```verilog
<condition> ? <true_value> : <false_value>;
```

This reads as:
**If** `<condition>` is true, **then** return `<true_value>`, **else** return `<false_value>`.

---

### **Example: 2:1 MUX using Ternary Operator**

```verilog
module mux (
    input wire i0,
    input wire i1,
    input wire sel,
    output wire y
);

assign y = sel ? i1 : i0;

endmodule
```

---

### **Explanation:**

* When `sel = 1`, output `y = i1`
* When `sel = 0`, output `y = i0`

This is equivalent to:

```verilog
if (sel)
    y = i1;
else
    y = i0;
```

but written in a more compact, **combinational-friendly** form.

---

### **Note:**

* Ternary operators should be used **only in continuous assignments** (`assign`) or **inside `always @(*)` blocks** for combinational logic.
* For sequential logic (with clock), use `if-else` inside `always @(posedge clk)` blocks instead.

Now, lets start the simulation of ternary_operator_mux.v

<img width="3838" height="2110" alt="Screenshot 2025-07-15 160426" src="https://github.com/user-attachments/assets/68a94076-d0f4-48ef-8657-dd1f2a463c63" />

<img width="3838" height="2110" alt="Screenshot 2025-07-15 160609" src="https://github.com/user-attachments/assets/0be1969c-73be-4a5d-a951-7561211e477e" />

Now we will synthesize the module and generate a netlist and then later proceed with GLS

<img width="3838" height="2110" alt="Screenshot 2025-07-15 160718" src="https://github.com/user-attachments/assets/098f211e-937f-4cad-bef3-4e120113c537" />

<img width="3838" height="2119" alt="Screenshot 2025-07-15 160819" src="https://github.com/user-attachments/assets/0a43338c-1b5a-4c37-9817-3cf64319709d" />

<img width="3838" height="2115" alt="Screenshot 2025-07-15 160904" src="https://github.com/user-attachments/assets/ee36d169-90a3-4c01-84ea-73dfe63a40be" />

<img width="3838" height="2110" alt="Screenshot 2025-07-15 160954" src="https://github.com/user-attachments/assets/c6bc4fe9-e100-4a76-a373-ede41bcec7a1" />

<img width="3838" height="2115" alt="Screenshot 2025-07-15 161317" src="https://github.com/user-attachments/assets/204e2419-ccc1-4d27-85ea-32a63652d49a" />

<img width="3838" height="1989" alt="Screenshot 2025-07-15 161404" src="https://github.com/user-attachments/assets/104b558a-b3a6-4fcd-99c4-5afdcd7baa97" />

Now that we have generated the netlist, lets do GLS. so the inputs to the iverilog will be our verilog models, netlist and testbench

<img width="3838" height="2108" alt="Screenshot 2025-07-15 162841" src="https://github.com/user-attachments/assets/58e16398-1297-4797-b00c-831882261e2b" />

<img width="3839" height="2119" alt="Screenshot 2025-07-15 162315" src="https://github.com/user-attachments/assets/f9bc52dd-abfd-4054-afb7-e6381c3166e7" />

Compare the Waveforms. We find it to be same as that we simulated earlier hence the functionality is verified.
I'm just attaching the image of the previous simulation for quick comparison

<img width="3838" height="2110" alt="Screenshot 2025-07-15 160609" src="https://github.com/user-attachments/assets/cca44af1-7496-4c9a-bb1b-f15f59b0f94f" />

---
### SKY130RTL D4SK2 L2 Lab GLS Synth Sim Mismatch part2
---

### **Issue: Incorrect Sensitivity List in `bad_mux`**

```verilog
module bad_mux ( 
    input i0, input i1,
    input sel,
    output reg y
);

always @(sel)  // Incorrect sensitivity list
begin
    if (sel)
        y <= i1;
    else
        y <= i0;
end

endmodule
```

#### **What's wrong?**

* The `always` block is triggered **only when `sel` changes**.
* If `i0` or `i1` change but `sel` remains the same, the block **won’t execute**, and `y` will not update.
* This causes simulation to hold the old value of `y`, which is interpreted as **sequential behavior**, not combinational logic.
* Synthesis tools may infer a **latch** or unintended **flip-flop**, depending on the context.

---

### **Correct Version: `good_mux` with Proper Sensitivity List**

```verilog
module good_mux ( 
    input i0, input i1,
    input sel,
    output reg y
);

always @(*)  // Correct sensitivity list
begin
    if (sel)
        y <= i1;
    else
        y <= i0;
end

endmodule
```

#### **Why is this correct?**

* `always @(*)` tells the simulator to **automatically include all inputs** used in the block in the sensitivity list.
* So `i0`, `i1`, and `sel` are all tracked.
* Any change in these signals causes the block to re-evaluate, correctly modeling a **combinational multiplexer**.
* This avoids mismatches between simulation and synthesis.

---

### **Conclusion:**

| Design     | Sensitivity List | Behavior             | Synthesis Result          |
| ---------- | ---------------- | -------------------- | ------------------------- |
| `bad_mux`  | `@(sel)`         | Misses input changes | May infer a latch         |
| `good_mux` | `@(*)`           | Tracks all inputs    | Correct combinational mux |

**Always use `@(*)` for combinational logic** to prevent simulation-synthesis mismatches.

---
### **Simulating, Synthesizing and Gate Level Synthesis of bad_mux and comparing the waveforms**
---
<img width="3838" height="2115" alt="Screenshot 2025-07-15 175321" src="https://github.com/user-attachments/assets/45c7094c-6f63-4388-9606-bc2b67e0a7df" />

<img width="3838" height="2117" alt="Screenshot 2025-07-15 175428" src="https://github.com/user-attachments/assets/a164b1c2-94df-48f5-a216-b936bc339f6e" />

You can see in above waveform that even when sel=0, Y is not following i0.

Synthesizing bad_mux

<img width="3838" height="2121" alt="Screenshot 2025-07-15 175628" src="https://github.com/user-attachments/assets/af29ebd7-8d0e-476f-ba43-0938c35150df" />

<img width="3838" height="2117" alt="Screenshot 2025-07-15 175727" src="https://github.com/user-attachments/assets/436a897c-19cf-4866-8b63-b04113d4f77e" />

<img width="3838" height="2124" alt="Screenshot 2025-07-15 175820" src="https://github.com/user-attachments/assets/db994ad4-1d26-4312-8527-413a70703015" />

<img width="3838" height="2106" alt="Screenshot 2025-07-15 175846" src="https://github.com/user-attachments/assets/6fd105a8-3519-4e96-9f29-44a64fbe891f" />

<img width="3838" height="2108" alt="Screenshot 2025-07-15 175943" src="https://github.com/user-attachments/assets/eaaec0e0-23f1-40d9-be66-b1692336272a" />

<img width="3838" height="2103" alt="Screenshot 2025-07-15 180012" src="https://github.com/user-attachments/assets/08f146e7-fa37-4f3b-b0b2-2468700477cd" />

Now, let's do the Gate level Simulation my giving netlist as input to iverilog along with the verilog models and compare the resulatant waveform with our previous simulation

<img width="3847" height="2115" alt="Screenshot 2025-07-15 180447" src="https://github.com/user-attachments/assets/258505c3-230b-4e9b-ad42-9582c054bd4c" />

<img width="3838" height="2101" alt="Screenshot 2025-07-15 180533" src="https://github.com/user-attachments/assets/4a7acffb-4477-484e-85a4-5fe11edf88b7" />

The GLS shows a proper functionality of an MUX, but still our simulation and GLS are not the same hence we see a Simulation Mismatch.
I'm attaching below our previous simulation so that we can easily see the difference.

<img width="3838" height="2117" alt="Screenshot 2025-07-15 175428" src="https://github.com/user-attachments/assets/337d4b88-41b4-479e-ad20-4b75a902a3a1" />

---
### **Simulating, Synthesizing and Gate Level Synthesis of good_mux and comparing the waveforms**
---
<img width="3838" height="2117" alt="Screenshot 2025-07-15 181253" src="https://github.com/user-attachments/assets/9bcf6be5-17fc-4ef1-8a3d-d98cbcd3712b" />

<img width="3838" height="2119" alt="Screenshot 2025-07-15 181356" src="https://github.com/user-attachments/assets/7e92dcd3-0f4c-4255-a54a-09f23a787e07" />

<img width="3838" height="2115" alt="Screenshot 2025-07-15 181509" src="https://github.com/user-attachments/assets/56934095-e93a-4321-a28c-d30ff584a25a" />

<img width="3838" height="2115" alt="Screenshot 2025-07-15 181554" src="https://github.com/user-attachments/assets/4563ec38-15d4-41dc-8699-dbbafca466fb" />

<img width="3838" height="2121" alt="Screenshot 2025-07-15 181626" src="https://github.com/user-attachments/assets/3fe06d20-32fe-4cf6-856f-e4069584569b" />

<img width="3838" height="2115" alt="Screenshot 2025-07-15 181701" src="https://github.com/user-attachments/assets/25f98b68-550b-4913-a38d-de93293a54b1" />

<img width="3838" height="2117" alt="Screenshot 2025-07-15 181747" src="https://github.com/user-attachments/assets/cecbed5f-1d99-4423-b269-5b680504ce1e" />

<img width="3838" height="2108" alt="Screenshot 2025-07-15 181816" src="https://github.com/user-attachments/assets/b34f4503-e563-4e7a-8162-1ae6f4486164" />

<img width="3844" height="2119" alt="Screenshot 2025-07-15 181930" src="https://github.com/user-attachments/assets/ed966d33-0f06-4a86-93ba-7abf84cb3592" />

<img width="3838" height="2108" alt="Screenshot 2025-07-15 182012" src="https://github.com/user-attachments/assets/f8feec19-efa9-4eb5-930c-73561fa99456" />

---
## Labs on synth-sim mismatch for blocking statement
---
### SKY130RTL D4SK3 L1 Lab Synth sim mismatch blocking statement part1
and
### SKY130RTL D4SK3 L2 Lab Synth sim mismatch blocking statement part2
---
### **Incorrect Version (Simulation-Synthesis Mismatch)**

<img width="3840" height="2160" alt="Screenshot 2025-07-16 092340" src="https://github.com/user-attachments/assets/fff91cd7-fd93-45cb-9d0a-65423eca1e1d" />

```verilog
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
```
<img width="3840" height="2160" alt="Screenshot 2025-07-16 092736" src="https://github.com/user-attachments/assets/0cdcc173-0f61-4526-b6ee-39c5d9ac2a71" />

#### Problem:

* In a **blocking assignment (`=`)**, the operations are executed **in order**, like software instructions.
* Here, `d` is assigned **before** `x` is updated, so it uses the **old or garbage value** of `x`.
* In simulation, this will cause `d` to produce incorrect results.
* In synthesis, the tool might optimize and connect the logic correctly, causing a **mismatch** between simulation and real hardware.

---

### **Correct Version (Proper Combinational Logic)**

```verilog
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
```

#### Why This is Correct:

* `x` is computed **before** being used in `d`.
* This ensures that `d` always uses the **updated value** of `x`.
* Simulation behavior will **match** synthesis, and the logic will behave as intended.

### Summary Table

| Version     | Order of Assignments       | Behavior                | Synthesis-Simulation Match         |      |
| ----------- | -------------------------- | ----------------------- | -----------------------------------| -----|
|  Incorrect | `d = x & c;`, then \`x = a | b;\`                    | `d` uses stale `x`, behaves wrongly |  No  |
|  Correct   | \`x = a                    | b;`, then `d = x & c;\` | `d` uses fresh `x`, works correctly |  Yes |


Now let's simulate the module blocking_caveat and see if the output is as expected.
---
### Simulation and Synthesis of blocking_caveat followed by GLS**
---
<img width="3838" height="2112" alt="Screenshot 2025-07-15 190507" src="https://github.com/user-attachments/assets/8bcd0a7f-a6f7-4af7-8a35-fe08a7a9e55b" />

<img width="3838" height="2110" alt="Screenshot 2025-07-15 190615" src="https://github.com/user-attachments/assets/1dd53fa9-b115-48d4-934f-728eea81b7af" />

The marked point in the waveform is not following d = (a | b) & c; because x, which is (a | b), is storing old values.

Now, let's do the synthesis, generate our netlist and perform GLS and verify the results

<img width="3838" height="2124" alt="Screenshot 2025-07-16 091308" src="https://github.com/user-attachments/assets/0f6f4086-5456-4e7e-b35f-5bd7f93637fc" />

<img width="3838" height="2115" alt="Screenshot 2025-07-16 091607" src="https://github.com/user-attachments/assets/872a49ac-7080-4a3a-8887-f1a0acac12c2" />

<img width="3838" height="2112" alt="Screenshot 2025-07-16 091652" src="https://github.com/user-attachments/assets/821fd3e2-ddfc-4863-b183-9527dab8e522" />

<img width="3838" height="2115" alt="Screenshot 2025-07-16 091730" src="https://github.com/user-attachments/assets/01cf23e7-065c-4d99-8c46-b530e08897e4" />

<img width="3838" height="2121" alt="Screenshot 2025-07-16 091828" src="https://github.com/user-attachments/assets/a8a34bcb-1835-4584-be7e-fd436dd3d224" />

<img width="3838" height="2117" alt="Screenshot 2025-07-16 091904" src="https://github.com/user-attachments/assets/af713938-fa2a-4ed2-93da-9ac05994bd39" />

<img width="3838" height="2110" alt="Screenshot 2025-07-16 092043" src="https://github.com/user-attachments/assets/17889d04-8367-4143-a72a-8d850575c2ad" />

<img width="3840" height="2160" alt="Screenshot 2025-07-16 092236" src="https://github.com/user-attachments/assets/c6148df2-793d-4b44-8bee-c94103b634b9" />

The marked point in the waveform is following d = (a | b) & c

I'm attaching below our previous simulation so that we can easily see the difference.

<img width="3838" height="2110" alt="Screenshot 2025-07-15 190615" src="https://github.com/user-attachments/assets/1dd53fa9-b115-48d4-934f-728eea81b7af" />

So we can clearly Synthesis simulation mismatch due to blocking statements.

---
# Day 5 - Optimization in synthesis
---
## If Case constructs
---
### SKY130RTL D5SK1 L1 IF CASE Constructs part1
---

![WhatsApp Image 2025-07-16 at 19 11 01_39c4a7a8](https://github.com/user-attachments/assets/cc42eac0-5922-4aeb-9e33-9538ab752340)

**Caution While Using the `if` Construct:**

In digital design, using the `if` construct carelessly can lead to the inference of unintended latches. This typically happens due to incomplete conditional logic. Consider the following code:

```verilog
if (cond1)
    y = a;
else if (cond2)
    y = b;
```

In this example, there is no `else` clause specifying what should happen when neither `cond1` nor `cond2` is true. As a result, the synthesizer assumes that the value of `y` must be retained in such cases, and to do this, it infers a latch. The latch holds the previous value of `y`, effectively forming a feedback path and creating a combinational loop. Internally, the output of the latch is connected to the multiplexer (MUX) handling `cond2`, and the MUX controlling `cond1` sends its output to one input of the latch. The enable signal for the latch is derived from the logical OR of `cond1` and `cond2`. To avoid such latch inference, always ensure that all possible conditions are covered using a complete `if-else` structure or use a `case` statement when applicable.

![WhatsApp Image 2025-07-16 at 19 28 26_0c4c6f91](https://github.com/user-attachments/assets/9a4d8774-8fff-40cb-8821-3381cbc09435)

---
### Sky130RTL D5SK1 L2 IF CASE Constructs part2
---

Consider the example of a counter:

```verilog
always @ (posedge clk, posedge reset)
begin
    if (reset)
        count <= 3'b00;
    else if (en)
        count <= count + 1;
end
```

Although the code is not complete, it is functionally correct.

Now, let’s analyze the hardware implementation. (It’s always important to visualize the hardware.)

When the `enable` signal is active, the counter increments by 1 (`count + 1`). However, when `enable` is inactive, the counter holds its current value. This is the expected behavior and aligns with how a counter is supposed to function.

It’s important to note that **inferred latches are acceptable in sequential circuits**, where retaining previous state is intentional. However, **in combinational circuits, inferred latches are generally undesirable**, as they can lead to unintended behavior.

<img width="1854" height="1491" alt="image" src="https://github.com/user-attachments/assets/817604bf-2eb2-4d99-8c3a-d750a244af17" />

**Case Statement:**

* Both `if` and `case` statements are used inside an `always` block and must be assigned to a variable declared as `reg`.
* The `case` statement is typically used for multi-way branching, similar to the `switch-case` construct in C.
* It is well-suited for implementing **multiplexers**, **finite state machines (FSMs)**, and **decoders**.
* All branches of the `case` are evaluated **in parallel**, unlike `if`, which checks conditions sequentially.
* To prevent **unintended latch inference**, it is important to **always include a `default` case**.

Example:

```verilog
always @(sel or c1 or c2)
begin
  case (sel)
    2'b00: out = c1;
    2'b01: out = c2;
    default: out = 1'b0;
  endcase
end
```
<img width="954" height="938" alt="image" src="https://github.com/user-attachments/assets/f1972dfe-c0e4-422d-84f2-39d368b724a8" />

To avoid latch inference, we include a `default` case in the `case` statement.

Example:

```verilog
reg [1:0] sel;

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
```

Including the `default` ensures all possible values of `sel` are covered, thereby avoiding **inferred latches**.

---

### Partial Assignment in `case`:

When controlling multiple outputs within a `case`, **partial assignments** can lead to latch inference.

Example:

```verilog
reg [1:0] sel;
reg x, y;

always @(*)
begin
  case (sel)
    2'b00: begin
      x = a;
      y = b;
    end
    2'b01: begin
      x = c;
      // y is not assigned here
    end
    default: begin
      x = d;
      y = b;
    end
  endcase
end
```

In this example, for `sel = 2'b01`, only `x` is assigned, and `y` is left unassigned in that case. As a result, **`y` retains its previous value**, which causes the synthesis tool to **infer a latch** for `y`.

To avoid this, ensure **all outputs are assigned in every case branch**, including the `default`.

<img width="596" height="713" alt="image" src="https://github.com/user-attachments/assets/956e6738-6e8c-4bc5-a3ab-4531f5527afd" />

### **Comparison between `if` and `case` statements:**

#### **`if` Statement:**

```verilog
if        // Highest priority
else if
else if
else      // Lowest priority
```

* In the case of `if`, **only one condition is evaluated as true**, based on priority from top to bottom.
* The evaluation follows a **sequential priority order**, and once a true condition is found, the rest are skipped.
* This is ideal when **priority-based decisions** are required.

---

#### **`case` Statement:**

```verilog
case (sel)
  2'b00:
  2'b01:
  2'b10:
  2'b1?:   // '?' indicates a don't care bit (can be 0 or 1)
endcase
```

* In `case`, **all cases are evaluated in parallel**.
* It is essential to **avoid overlapping patterns**, as shown in the bad example above.
* For instance, both `2'b10` and `2'b1?` can match `2'b10`, causing **multiple branches to be valid at once**, which can lead to **unpredictable or incorrect behavior**.
* Therefore, **always ensure non-overlapping conditions** in `case` statements to maintain correctness.
e know if you’d like the same kind of comparison for synthesis results or behavioral use.

---
## Labs on "Incomplete If Case"
---
### Sky130RTL D5SK2 L1 Lab Incomplete IF part1
---
Here’s your content reframed clearly and concisely, without altering the technical meaning:

We will now observe how **synthesis tools** and **simulators** behave when there are **incomplete `if` and `case` statements**.

The necessary files for this demonstration are mentioned below

<img width="3840" height="2160" alt="Screenshot 2025-07-18 175357" src="https://github.com/user-attachments/assets/c7e55ee5-64c8-4631-bd0d-1b08bd4ff457" />

### **incomp_if**

In this case, the `if` statement gets translated into a **multiplexer (MUX)**.

Here, the **select line** is `i0`.

* When `i0 = 1`, the output `y` is assigned the value `1`.
* However, since the `else` part is missing, when `i0 = 0`, there is **no new assignment**, so the output **retains its previous value** — this results in **latch inference**.

The behavior of this MUX **resembles a D-latch**, with **latch enable** controlled by `i0`.
It acts like a **positive level-sensitive latch**:

* When `i0` is high (`1`), the input (`i1`) is passed to output `y`.
* When `i0` is low (`0`), the output `y` **holds its previous value**, effectively **latching** it.

<img width="666" height="490" alt="image" src="https://github.com/user-attachments/assets/082e7fe4-a7d3-41ef-b40d-3cc098a590ae" />

<img width="497" height="378" alt="image" src="https://github.com/user-attachments/assets/03114c82-5aef-4345-ae06-cf9deccffdd7" />

### Let’s examine the **simulation and synthesis** behavior:

#### **Simulation:**

```bash
iverilog incomp_if.v tb_incomp_if.v
./a.out
gtkwave tb_incomp_if.vcd
```

<img width="3840" height="2160" alt="Screenshot 2025-07-18 175452" src="https://github.com/user-attachments/assets/e117ef76-b5f4-453e-afc3-8cc617bb212f" />

<img width="3840" height="2160" alt="Screenshot 2025-07-18 175603" src="https://github.com/user-attachments/assets/d27fc1c9-9ddb-4dc1-838e-22fd1a19291f" />

<img width="3840" height="2160" alt="Screenshot 2025-07-18 175750" src="https://github.com/user-attachments/assets/74dcc004-cdf6-467f-bd53-e9c69097430e" />

<img width="3840" height="2160" alt="Screenshot 2025-07-18 175852" src="https://github.com/user-attachments/assets/27eed2d0-1b77-4bd4-96fd-b30cedfb2d16" />

<img width="3840" height="2160" alt="Screenshot 2025-07-18 180052" src="https://github.com/user-attachments/assets/da2fbd10-b0ed-449b-a549-88f4b6c52683" />

In the simulation output:

* When `i0` is **high (1)**, the output `y` follows the input `i1`.
* When `i0` is **low (0)**, `y` **latches** onto the last value of `i1` and remains **constant**, even though `i1` might change.

This clearly shows that the absence of an `else` block causes the simulator to treat the output as a **latch**.

<img width="3840" height="2160" alt="Screenshot 2025-07-18 180729" src="https://github.com/user-attachments/assets/c7016d2c-830d-459e-98c3-3a829bd10be3" />

<img width="3840" height="2160" alt="Screenshot 2025-07-18 180825" src="https://github.com/user-attachments/assets/d2d7f2b5-7352-46af-aeac-b42498b8398d" />

<img width="3840" height="2160" alt="Screenshot 2025-07-18 180913" src="https://github.com/user-attachments/assets/f0d41ca7-9f99-486b-9916-590a5add3e82" />



