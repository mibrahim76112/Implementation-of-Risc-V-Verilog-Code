# Implementation of RISC-V Verilog Code

A basic Verilog implementation of a **RISC-V processor datapath and control unit**.  
This project demonstrates the core building blocks of a simple RISC-V CPU, including instruction decoding, arithmetic and logic operations, register file access, memory interaction, branching, and a testbench for simulation.

It is a good academic project for understanding how a processor is built from modular hardware components in **Verilog HDL**.

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
