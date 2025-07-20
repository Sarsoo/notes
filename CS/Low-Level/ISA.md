---
tags:
  - low-level
  - dev
title: ISA
---
Instruction Set Architecture

___Not Microarchitecture___
-   Physical implementation of ISA

- Abstract model of a computer
- CPU is an implementation
- Defines
	- Data types
	- Registers
	- Hardware support for main memory
	- Features
		- Memory consistency
		- Addressing modes
		- Virtual memory
- Specifies behaviour of machine code
	- Binary compatibility
	- Allows many implementations

# Complexity

## Complex
- CISC
	- Complex instruction set computer

## Reduced
- RISC
	- Reduced instruction set computer
- Simplifies processor
	- Implementing only frequent instructions
	- Less frequent as subroutines
- Typically requires less transistors than CISC
	- Improves
		- Cost
		- Power consumption
		- Heat dissipation

## Very Long Instruction Word
VLIW

## Long Instruction Word
LIW

## Explicitly Parallel instruction Computing
EPIC

# ARM
Acorn RISC Machine
Advanced RISC Machines

- RISC architectures
- System-on-Chips, System-on-Modules
	- SOC, SOM
- iPhones A Series
- 32-bit Profiles
	- A
		- Application
		- Cortex-A
	- R
		- Real-time
		- Cortex-R
	- M
		- Micro-controller
		- Cortex-M

# Instructions

- Params
	- Registers
		- Functions
			- Arithmetic
			- Addressing
			- Control
	- Memory locations
		- With offsets
	- Addressing modes
		- Interpret operands
- Types
	- Data handling and memory
		- Set register
		- Copy data from memory to register or reverse
			- Load and store operations
		- Read and write from hardware
	- Arithmetic and logic
		- +, -, x, ÷
		- Bitwise
		- Compare
		- Floating point instructions
	- Control flow
		- Branch
			- Another location in program to execute
		- Conditionally branch
		- Indirectly branch
			- Branch with argument memory address
		- Call
			- Save the location to return to
	- Coprocessor
		- Load/store to and from coprocessor
		- Perform coops
	- Complex
		- Multiple things at once
		- Move multiple values between stack and memory
		- Move large blocks of memory
		- Complicated integer and floating point maths
			- Square root, log, sin, cos
		- ALU operations from memory not register