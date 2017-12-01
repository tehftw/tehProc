# tehProc

Simulator of the ultra basic, minimum instruction set, but hopefuly Turing-complete, processor

tehProc is currently in v2, and lacks any represantion of the actual memory of the processor

Current registers, both are 1-bit(True-False, or 1-0): A, B. 

Memory: M. It's a stream of 1-bit values.

P - Memory Pointer, it keeps track of where in memory the processor is(used for instructions)


       List of ASM commands as of v2 of tehProc:
       
  0)<NONE> : Do nothing
       
  1)<MEMFOR> : Move forward in memory
       
 MemoryPointer = MemoryPointer + 1
 
  2)<MEMBAC> : Move backwards in memory
       
 MemoryPointer = MemoryPointer - 1
 
 3)<TWONAND>/<NANDAB> : 2-NAND operation: takes two inputs, and gives the NAND of them
       
 regA = NAND(regA, regB)
 
 4)<WRITE> : write into memory. Writes the bit that's shown by the MemoryPointer into register A
 
 (MemoryPointer) = regA
 
 5)<READ> : read from memory
 
 regA = (MemoryPointer)
 
 6)<ATOB> : moves the register A into register B
 
 regB = regA
 
 7)<EMPTYA> : moves the register A into register B while erasing register A
 
 regA = 0
