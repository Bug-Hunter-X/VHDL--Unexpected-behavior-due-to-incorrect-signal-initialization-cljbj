# VHDL: Uninitialized Signal Bug
This repository demonstrates a common error in VHDL: incorrect initialization of internal signals.
The code in `bug.vhdl` initializes the `internal_data` signal with `x"00"`, however this should be avoided in VHDL.  The `x` denotes an undefined value, and depending on the synthesis tool, this may lead to unexpected behavior and a difficult-to-debug issue. 
The correct solution is shown in `bugSolution.vhdl`.  The initialization should specify a definite value, such as "00000000".