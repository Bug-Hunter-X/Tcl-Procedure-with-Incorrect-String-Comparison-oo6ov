# Tcl Procedure with Incorrect String Comparison

This repository demonstrates a subtle bug in a Tcl procedure that incorrectly handles string comparisons.

## Bug Description

The `badproc` procedure is intended to compare two values and return 1 if they are equal and 0 otherwise. However, it uses the `==` operator, which performs a string comparison in Tcl. This means that if the inputs are numbers, the procedure might produce unexpected results due to implicit string conversions.

## Bug Solution

The solution involves using the `eq` operator for numerical comparisons and explicitly converting the input values to numbers if necessary.  The `goodproc` illustrates a corrected version of the procedure.

## How to reproduce

1.  Clone this repository.
2.  Run `tclsh bug.tcl` to see the incorrect behavior.
3.  Run `tclsh bugSolution.tcl` to see the corrected behavior.