# Off-by-One Error in VHDL Counter Reset

This repository demonstrates a common, yet subtle, off-by-one error in a VHDL counter.  The error lies in the reset condition of the counter, leading to unexpected behavior when the counter reaches its maximum value. The `buggy_counter.vhd` file contains the buggy code, while `buggy_counter_solution.vhd` provides the corrected version.

The bug is hard to spot at first glance because the syntax is correct, but the logic is flawed. This highlights the importance of thorough testing and code review in VHDL development.

## How to Reproduce

1.  Simulate `buggy_counter.vhd` using your preferred VHDL simulator (e.g., ModelSim, GHDL).
2.  Observe the counter's behavior when it reaches its maximum value (15 in this case).
3.  Compare its behavior to the expected behavior and the corrected code in `buggy_counter_solution.vhd`.

## Solution

The solution involves ensuring correct handling of the reset condition when the counter reaches its maximum value. The fix is in `buggy_counter_solution.vhd`.