Overview

This repository contains the Verilog implementation of a Binary Coded Decimal (BCD) counter and its corresponding testbench. The BCD counter is a 2-bit counter that cycles through decimal values in binary representation, resetting after reaching the maximum value.

Functional Description

BCD Counter

Inputs:

clk_in: Clock signal, on whose positive edge the counter updates.

reset_in: Reset signal, which initializes the counter to 00.

Output:

bcd_out: A 2-bit output that represents the current count in BCD.

Operation:

When reset_in is active, the counter resets to 2'b00.

On every positive edge of clk_in, the counter increments by 1.

If the counter reaches the maximum value (2'b10), it resets back to 2'b00.

Sequence: The counter cycles through the states:

00 → 01 → 10 → 00 (repeats)
