- The order in which atomic (scalar) parameters, or individual parts of a complex parameter, are allocated
- How parameters are passed
	- Pushed on the stack, placed in registers, or a mix of both
- Which registers the called function must preserve for the caller
	- Also known as: callee-saved registers or non-volatile registers
- How the task of preparing the stack for, and restoring after, a function call is divided between the caller and the callee

Subtle differences between compilers, can be difficult to interface codes from different compilers

Calling conventions, type representations, and name mangling are all part of what is known as an [application binary interface](https://en.wikipedia.org/wiki/Application_binary_interface) ([[ABI]])

# cdecl
C declaration

- Originally from Microsoft's C compiler
	- Used by many C compilers for x86
- Subroutine arguments passed on the stack
- Function arguments pushed right-to-left
	- Last pushed first
- Caller cleans stack after function call returns

# stdcall

- Variation on Pascal calling convention
- Callee cleans stack
- Params pushed onto stack right-to-left
	- Same as _cdecl_
- Standard for Microsoft Win32 API