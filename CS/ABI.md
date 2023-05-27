- How data structures & computational routines are accessed in machine code ([[Code Types]])
	- Machine code therefore hardware-dependent
- API defines this structure in source code
- Adherence usually responsibility of
	- [[Compilers]]
	- OS
	- Library author

# Components

- Processor instruction set
	- Register file structure
	- Stack organisation
	- Memory access types
- Size, layouts and alignments of basic data types
- [[Calling Conventions]]
	- How function arguments are passed
		- Stack or register
		- Which registers for which function param
		- Parameter order
	- Return values retrieved
- How app makes sys calls to OS
	- If ABI specifies direct sys calls over procedure calls to sys call stubs then sys call numbers
- Binary format of object files, program files
	- For complete OS ABIs

# Complete ABI
- Allows program from one OS to run on any other without change
	- Provided all shared libraries and prerequisites etc

# Embedded ABI
- File format, data types, register usage, stack frame organisation, function parameter passing conventions
	- For embedded OS
- [[Compilers]] create object code compatible with code from other [[compilers]]
	- Link libraries from different [[compilers]]