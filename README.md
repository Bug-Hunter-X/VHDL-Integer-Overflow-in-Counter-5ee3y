# VHDL Integer Overflow Bug
This repository demonstrates a common bug in VHDL: integer overflow in a counter. The `buggy_counter.vhd` file contains the erroneous code, while `fixed_counter.vhd` provides a corrected version.

## Bug Description
The `buggy_counter` entity uses an integer type to represent the counter value.  When the counter reaches its maximum value (15), incrementing it causes an overflow. The counter wraps around to 0 instead of stopping or generating an error, potentially leading to incorrect functionality.

## Solution
The `fixed_counter` entity addresses this issue using the `unsigned` type.  `unsigned` types provide a more controlled way to handle counter overflow, typically generating an error instead of silently wrapping around.  Alternatives include using a larger integer range or incorporating explicit overflow detection.