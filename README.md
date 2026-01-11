# 16-bit-Processor-Design
A 16-bit CPU architecture simulation using Logisim Generic 2.7.1.

## Overview
![processor_architecture](https://github.com/user-attachments/assets/474f9e70-3592-40fb-809c-bf59b11c0728)

## Notes
To run this simulation on your local machine:

1.  Install Logisim: Download Logisim Generic 2.7.1, other versions might works with potential errors.
2.  Download "processor.circ".
3.  Open Logisim. Go to "File > Open", select "processor.circ" and select "main".
4.  Find Instr_Mem, and edit it the codes in hexcimal.
5.  Enable ticks (Ctrl+K) to start the clock cycle.

## Instruction Set Architecture (ISA)

### Instruction Formats
The processor uses a 16-bit instruction width with three primary formats:

| Type | Opcode (12-15) | Read Reg 2 (9-11) | Read Reg 1 (6-8) | Write Reg (3-5) | Immediate / Other |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **R-Type** | Opcode | Read 2 | Read 1 | Write Reg | (0-2) Unused |
| **I-Type** | Opcode | Imm (9-11) | Read 1 | Write Reg | Imm (0-2) |
| **J-Type** | Opcode | -- | Imm X (6-8) | -- | -- |

*(Note: For I-Type, the Immediate value is split between bits 9-11 and 0-2)*

##Supported Instruction
Instruction  Opcode
li           1001
add          0000
and          0001
or           0010
load         0110
store        0111
move         1000
addi         0011
andi         0100
ori          0101
ble          1010
bne          1011
jump         1100
call         1101
rtn          1110
halt         1111
