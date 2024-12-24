# Incorrect Jump using `jmp short` in Assembly

This repository demonstrates a potential bug in assembly code involving the `jmp short` instruction. The `jmp short` instruction is used to perform a relative jump, where the target is specified by a relative offset from the current instruction.  The offset is limited to a small range (typically -128 to +127 bytes), so if the target label is too far away, the jump will not work correctly leading to incorrect program execution or a program crash.  The example showcases this error and provides a solution. 

## Bug Description
The `bug.asm` file contains assembly code with a `jmp short` instruction that points to a label which is outside the acceptable range for short jumps. This leads to an unexpected jump, causing the program to behave incorrectly. 

## Solution
The `bugSolution.asm` file corrects this issue by using `jmp` instruction without the `short` qualifier, allowing for longer jumps.  It also includes better comments to enhance clarity.  Alternatively, the code structure could be revised to reduce the distance between the `jmp` and target label.