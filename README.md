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

R type:						                  I type:                                     J type:
Bits (3 – 5): Write register			  Bits (3 – 5): Write register		            Bits (12-15): Operation code
Bits (6 – 8): Read register 1			  Bits (6 – 8): Read register 1               Bits (6 – 8): Immediate number X
Bits (9 - 11): Read register 2			Bits (12 - 15): Operation code
Bits (12 - 15): Operation code			Bits (0 – 2,9 – 11): Immediate number

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
