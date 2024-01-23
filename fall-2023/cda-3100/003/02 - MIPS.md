## MIPS Intro
### General Classes of MIPS Assembly
- Arithmetic (+, -, *, /)
- Logical (&, |, ~, ^, <<, >>)
- Data transfer (load from memory or stores memory)
- Transfers of control (jump, brach, call, return)

### MIPS Instruction Operands
- Integer constants
	- character
	- integer
	- address
- Registers
	- Integer
	- Floating-point
	- special
- Memory

### MIPS Integer Constants
- Represented in 16 bits
- Extended to 32 before used in operation

### MIPS Registers
- Limited number of data words (16, 32, or 64) reside in processor and stored in registers
- Advantages of registers:
	- Accessed much faster
	- Use less power
	- Require only a few bits to address
- MIPS Registers:
	- 32 integer ($0 - $31)
	- *hi* and *lo*
	- 32 floating point ($f0 - $f31)

### MIPS Integer Registers
| Name      | Number  | Usage                                 | Callee Must Preserve? |
| --------- | ------- | ------------------------------------- | --------------------- |
| $zero     | $0      | constant value 0                      | N/A                   |
| $at       | $1      | used by assembler                     | no                    |
| $v0 - $v1 | $2-$3   | function results and expression eval. | no                    |
| $a0 - $a3 | $4-$7   | function arguments                    | no                    |
| $t0 - $t7 | $8-$15  | temporaries                           | no                    |
| $so - $s7 | $16-$23 | saved temporaries                     | no                    |
| $k0 - $k1 | $26-$27 | reserved for used by OS kernel        | N/A                   |
| $gp       | $28     | global pointer                        | yes                   |
| $sp       | $29     | stack pointer                         | yes                   |
| $fp       | $30     | frame pointer                         | yes                   |
| $ra       | $31     | return address                        | yes                   |

### Memory
- Contains both data and instructions
- Can be viewed as a large array (vector) of bytes
- Beginning variable or instruction is associated w/ specific elements of this array
- Address of variable or instruction is its offset from beginning of memory

### Processor/Memory Interconnections
- Memory ports
	- one for specifying address
	- one for reading or writing data

### MIPS Assembly File
- File consists of a set of lines
- Each line can be:
	- directive
	- instruction
- Each can start with a label, a way of denoting its data or instruction location
- Can include comments with #

### General Form of MIPS Assembly Language Program
- Directives and instructions are placed on separate lines
``` asm
.data
	<declarations of variables>
.text
.globl main

main:
	<instructions>
	jr $ra
```

### MIPS Directives
| Directive         | Meaning                                                          |
| ----------------- | ---------------------------------------------------------------- |
| .align n          | Align next datum on $2^n$ boundary                               |
| .asciiz str       | Place the null-terminated string in memory                       |
| .byte b1,...,bn   | Place the n byte values in memory                                |
| .data             | Switch data segment                                              |
| .double d1,...,dn | Place n double precision values in memory                        |
| .extern sym size  | Declare datum stored at sym size bytes and is a global label     |
| .float f1,...,fn  | Place the n single precision values in memory                    |
| .globl sym        | Label sym can be referenced in other files                       |
| .half h1,...,hn   | Place the n halfword values in memory                            |
| .space n          | Allocate n bytes of space at current location in current segment |
| .text             | Switch to the text segment                                       |
| .word w1,...,wn   | Place the n word values in memory                                |

### MIPS Instructions
- General form
```asm
<optional label> <operation> <operands>
```
#### Example:
```asm
loop:
	addu $t2, $t3, $t4
	subu $t2, $t3, $t4
```

## QtSpim

### QtSpim Syscalls
- Syscall provides operating system services

| Service      | Call Code Arg | Other Arguments                        | Result         |
| ------------ | ------------- | -------------------------------------- | -------------- |
| print_int    | $v0 = 1       | $a0 = integer                          |                |
| print_float  | $v0 = 2       | $f12 = float                           |                |
| print_double | $v0 = 3       | $f12 = double                          |                |
| print_string | $v0 = 4       | $a0 = string address                   |                |
| read_int     | $v0 = 5       |                                        | integer in $v0 |
| read_float   | $v0 = 6       |                                        | float in $f0   |
| read_double  | $v0 = 7       |                                        | double in $f0  |
| read_string  | $v0 = 8       | $a0 = string address, $a1 = max length |                |
| exit         | $v0 = 10      |                                        |                |
| print_char   | $v0 = 11      | $a0 = char                             |                |
| read_char    | $v0 = 12      |                                        | char in $v0    |

### Pseudoinstructions Used for System Calls
- An instruction that is not directly implemented as a machine instruction

| Example       | Meaning    | Comment                     |
| ------------- | ---------- | --------------------------- |
| li $v0, 4     | $v0 = 4    | assign constant to register |
| la $a0, $_a$  | $a0 = $_a$ | assign                      |
| move $a0, $t0 | $a0 = $t0  | assign register to register |

### Simple MIPS Program
```asm
.data

msg:
	.asciiz "Hello I'm Julian!\n"
.text
.globl main

main:
	li $v0, 4
	la $a0, msg
	syscall

	jr $ra
```


## Arithmetic/Logical Operations

### Form of MIPS Arithmetic and Logic Instructions
- Most arith./logical instructions require 3 operands
- Form 1:
```
<operation> <dstreg>,<src1reg>,<src2reg>
```


