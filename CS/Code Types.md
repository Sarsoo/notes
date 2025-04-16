---
tags:
  - dev
title: Code Types
---
## Machine Code
-   Machine language instructions
-   Directly control [CPU](Processors.md)
-   Strictly numerical
-   Lowest-level representation of a compiled or assembled program
	-   Lowest-level visible to programmer
	-   Internally microcode might used
-   Hardware dependent
-   Higher-level languages translated to machine code
	-   [Compilers](Compilers.md), assemblers and linkers
	-   Not for interpreted code
		-   Interpreter runs machine code
-   [Assembly](Languages/Assembly.md) is effectively human readable machine code
	-   Has mnemonics for opcodes etc

## Microcode
-   Layer between CPU hardware and instruction set architecture
-   Normally written during design phase
	-   Deployed to ROM or PLA
		-   Programmable logic array
-   Machine code often has some backward compatibility
	-   Microcode is circuit specific

## Byte Code
Portable Code
-   Efficient execution by interpreter
-   Compact numeric codes, constants and references
	-   Encode compiler output following analysis and validation
-   Can be further compiled
	-   [Compilers](Compilers.md#JIT)
-   Typically passed to VM
	-   Java, [Python](Languages/Python.md) #py

## Object Code
-   Product of compiler
-   Sequence of statements
	-   Machine code
	-   Intermediate
		-   RTL
-   Linked to form executable
	-   Object code portion of machine code not yet linked