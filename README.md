# Assembly Addressing Mode Error

This repository demonstrates an uncommon error in assembly language programming related to incorrect addressing modes. The bug involves an unintended overwrite of memory due to the use of the same base register for both source and destination memory addresses. This can lead to unexpected program behavior, including crashes or incorrect results.

## Bug Description
The `bug.asm` file contains code that attempts to add the value at memory address `[ebx+4]` to the value in `ecx`, storing the result back to the memory address pointed to by `ebx`.  The problem is that the instruction `mov [ebx], eax` overwrites the memory location used to calculate the sum in the first place, leading to incorrect results.

## Solution
The `bugSolution.asm` file provides a corrected version using a different register for the destination address to avoid the unintended overwrite.

## How to run the code (Example - Adapt to your assembler):
1. Assemble the code using NASM or your preferred assembler.
2. Link the object file.
3. Run the executable.

Note: The specific way to run the code depends on your assembler and operating system.