## Project Overview

This project implements a **Single-Cycle MIPS Processor** using **Verilog HDL**.
The processor executes each instruction in a single clock cycle and supports basic MIPS instruction types including:

* R-type (add, sub, and, or, slt)
* I-type (lw, sw, beq)
* J-type (jump)

This project is developed as a **mini project** for understanding **Computer Architecture and Processor Design**.

---

## Objectives

* Understand the **single-cycle datapath architecture**
* Implement **control unit + datapath** in Verilog
* Simulate instruction execution step-by-step
* Learn interaction between **ALU, Register File, Memory, and Control Unit**

---

## Architecture

The processor consists of the following major components:

* **Program Counter (PC)** – Holds the address of the current instruction
* **Instruction Memory** – Stores instructions
* **Control Unit** – Generates control signals based on opcode
* **Register File** – Stores register values
* **ALU (Arithmetic Logic Unit)** – Performs operations
* **Data Memory** – Used for load/store instructions
* **MUXes** – Used for control-based data selection
* **Adder Units** – For PC increment and branch calculation

---

## 🔄 Instruction Flow

1. Fetch instruction from memory
2. Decode instruction fields (opcode, rs, rt, rd, etc.)
3. Generate control signals
4. Perform ALU operation
5. Access memory (if required)
6. Write result back to register
7. Update PC (sequential / branch / jump)

---

##Supported Instructions

| Type   | Instruction | Description     |
| ------ | ----------- | --------------- |
| R-type | add         | Addition        |
| R-type | sub         | Subtraction     |
| R-type | and         | Bitwise AND     |
| R-type | or          | Bitwise OR      |
| R-type | slt         | Set less than   |
| I-type | lw          | Load word       |
| I-type | sw          | Store word      |
| I-type | beq         | Branch if equal |
| J-type | j           | Jump            |

---

##Simulation

### Steps:

1. Open **Vivado**
2. Add all Verilog files
3. Set `Top_module` as top design
4. Add testbench
5. Run simulation

* Branch uses **shift left by 2**
* Jump uses **PC[31:28] concatenation**

---
##References

* Computer Organization and Design – Patterson & Hennessy
* MIPS Architecture Documentation


