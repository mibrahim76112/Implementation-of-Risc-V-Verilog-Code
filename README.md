# Implementation of RISC-V Verilog Code

A Verilog implementation of a **RISC-V processor datapath and control unit**.
This project demonstrates the core building blocks of a simple RISC-V CPU, including instruction decoding, arithmetic and logic operations, register file access, memory interaction, branching, and a testbench for simulation.

It is a strong academic project for understanding how a processor is built from modular hardware components in **Verilog HDL**.

---

## Project Overview

This repository implements the basic architecture of a RISC-V processor using separate Verilog modules.
The design includes modules for:

- instruction fetch
- instruction decode
- register file
- arithmetic and logic operations
- comparison and branching
- program counter update
- instruction memory
- data memory

A top-level `Core` module connects these units together to execute instructions.

---

## Features

- Modular Verilog implementation of a simple RISC-V CPU
- Separate ALU and adder/subtractor logic
- Register file implementation
- Instruction decoder and control signal generation
- Program counter and branch handling
- Instruction memory and data memory modules
- Comparator for branch decisions
- Testbench for simulation

---

## Repository Structure

```text
Implementation-of-Risc-V-Verilog-Code/
│
├── ALU.v                    # Arithmetic Logic Unit
├── Adder_Subtractor.v       # Adder and subtractor logic
├── Comparator.v             # Branch comparison logic
├── Core.v                   # Top-level processor core
├── DataMem.v                # Data memory module
├── InstrDecoder.v           # Instruction decoder / control unit
├── Instruction_Memory.v     # Instruction memory
├── ProgramCounter.v         # Program counter logic
├── RegFile.v                # Register file
├── tb.v                     # Testbench
└── README.md                # Project documentation
```

---

## Architecture Summary

The processor is organized around the `Core` module, which connects the major datapath and control blocks.

### Main Modules

**Core**
Integrates the complete processor datapath and control flow.

**ProgramCounter**
Tracks the current instruction address and supports branching and jump behavior.

**Instruction_Memory**
Stores the instructions to be executed.

**InstrDecoder**
Decodes the opcode and generates control signals for the datapath.

**RegFile**
Provides source register reads and destination register writes.

**ALU**
Performs arithmetic and logical operations.

**Comparator**
Evaluates branch conditions.

**DataMem**
Handles load and store operations.

**tb**
Testbench for simulation and verification.

---

## Supported Instruction Categories

Based on the instruction decoding logic, this design handles several common RISC-V instruction formats:

- R-type
- I-type
- S-type
- Load instructions
- Branch instructions
- JAL
- JALR
- LUI
- AUIPC

---

## How the Design Works

1. The Program Counter selects the current instruction address.
2. The Instruction Memory outputs the instruction.
3. The Instruction Decoder generates control signals from the opcode.
4. The Register File provides source operands.
5. Immediate values are generated depending on instruction format.
6. The ALU performs the selected operation.
7. The Comparator evaluates branch conditions.
8. The Data Memory is used for load/store instructions.
9. The result is written back to the register file when required.
