# Assembler

### Simulator inputs:
1. Assembly program: The user should be able to input a program (using the supported
instructions only) to be simulated. He should also specify its starting address (where
the program’s first instruction should be loaded in the memory).
2. Program data: The user should also specify any data required by the program to be
initially loaded in the memory. For each data item both its value and memory
address should be specified.

### Simulation and simulation outputs:
 The simulator should assume a single cycle datapath
identical to the one presented in lecture 7 (slide 5) except where it needs to be extended to
support the extra instructions required. Your program should simulate the program
execution showing the values (possibly in decimal and/or hexadecimal) carried by all the
wires of the datapath in each clock cycle. The simulator should also keep track of the
register file contents and memory contents. Finally, while simulating the execution, your
program should also keep track of the number of clock cycles spanned.
Please note the following:
1. We will pretend to have separate instruction and data memories for timing
purposes; however, to keep our simulation simple, we will assume that there will be
a single common memory underlying both (we will assume that both have the same
address space and that they always have the same contents).
2. Register 0 always contains the value 0. You will need to make sure you initialize
register 0 appropriately and make sure any attempt to modify it does not succeed.


### Additional Features:
1. Building the application as a GUI application
2. Building the application as an educational GUI application. In this case the GUI
should include an animated diagram of the datapath illustrating how the wire values
propagate through it each clock cycle. This bonus feature is highly recommended
and will be counted as two features as far as grading is concerned (since it includes
and extends the previous bonus feature).
3. Implementing and integrating an assembler to allow the user to supply programs in
a suitable assembly language. The assembly code can either be entered directly in
your program or in a text file read by your program. The assembler should support
labels, pseudoinstructions (like move and blt), and directives (like .data, .word,
and .text).
4. Support the following instructions as well:
• Arithmetic: sub, mul
• Load/Store: lh, lhu, sh, lui
• Logic: srl, and, andi, or, ori
• Control flow: bne
• Comparison: sltu, sltui
5. Including a larger set of programs (at least 6 meaningful programs) and their
equivalent C programs.
6. Provide a simulator for the pipelined datapath of MIPS based on the diagram in
lecture 8 slide 29. Note that this datapath does not detect or handle hazards at all
(which means that the input program has to be hazard-free to produce correct
results). Your simulator should simulate the program execution showing the
contents (decimal and/or hexadecimal) of all the fields of the pipeline registers (PC,
IF/ID, ID/EX, EX/MEM, and MEM/WB) including control signals at each clock cycle.
Any control signals that are not part of the pipeline registers (e.g., the PCSrc) should
also be displayed at each clock cycle. This feature will be counted as two bonus
features as far as grading is concerned.
