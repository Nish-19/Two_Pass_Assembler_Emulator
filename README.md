# Two_Pass_Assembler

Assembler and Emulator implementation in C Language for the given Assembly Language. Project as a part of CS321-CS322 Computer Architecture Course IIT-Patna.

## Rules of the given Assembly Language

* Two registers, A & B, arranged as an internal stack
* A program counter, PC
* A stack pointer, SP
* These registers are 32 bits in size
* Instructions have either no operands or a single operand
* The operand is a signed 2's complement value.
* The encoding uses the bottom 8 bits for opcode and the upper 24 bits for operand.
* Comments are denoted using ';' (semicolon)
* An operand is either a label or a number, the number can be decimal, hex or octal.
* Label definitions consist of the label name followed by a ':'
* Label Name is alpha_numberic
* Label used to calculate displacement in case of branch instructions.
* An operand is either a label or a number, the number can be decimal, hex or octal.

<img width="581" alt="instructions" src="https://user-images.githubusercontent.com/41947720/102636143-4ab31d00-417a-11eb-9676-a6e4798f2a0e.png">

## Assembler

* Has two data structures to store respectively labels and mnemonic table with expected operands.
* Reads the file once, converts to internal format using linked list and then parses.
* detects label errors.
* consistent and sensible formatting with sensible program structure.
* sensible variable, function & type names with explanatory comments.
* advanced listing file.
* assembles ALL test programs.                                 
* CAN IMPLEMENT and demonstrates the instruction SET.

## Emulator

* Three data structures are used to store respectively memory, 	mnemonic table with expected operands and a linked list structure 	code.
* loads object file,
* Does automatic trace i.e at each step displays the value of PC, SP, reg A, and Reg B
* Does automatic memory dump, before and after the program to show the state of memory elements.

## TestCases

Test cases consists of sample programs written in the simple assembly language. There are a total of 10 such programs. Test cases are present in the folder cs33testcases. The listing and object file obtained after execution from the assembler is also provided.

## Compiling and Running
1) For assembler
gcc asm.c -o asm

2) For emulator
gcc emu.c -o emu

### Running on given test cases
Assembler -
./asm cs33testcases/filename.asm

Emulator -
./emu cs33testcases/filename_obj.o
