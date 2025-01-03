# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL code: integer overflow in a counter.  The `buggy_counter.vhdl` file contains a counter that increments without handling overflow conditions. The `fixed_counter.vhdl` demonstrates a corrected version.

## Bug Description
The original code lacks a mechanism to prevent the counter from exceeding its defined range (0 to 15).  This leads to an unpredictable behavior and potential simulation errors or unexpected hardware behavior once the counter reaches its limit.

## Solution
The fixed version uses a modulo operator to wrap the counter back to 0 when it reaches 15, preventing overflow.  This ensures that the counter remains within the valid range and works correctly.

## How to Reproduce
1. Simulate `buggy_counter.vhdl` using your preferred VHDL simulator.
2. Observe the counter behavior; it will eventually overflow.
3. Simulate `fixed_counter.vhdl`; it will correctly wrap around at 15.
