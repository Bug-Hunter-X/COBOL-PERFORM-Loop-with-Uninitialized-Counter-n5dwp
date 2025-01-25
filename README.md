# COBOL PERFORM Loop Bug

This repository demonstrates a common error in COBOL programs involving the use of PERFORM loops with uninitialized counters or variables. The bug lies in how a loop condition is handled, leading to unexpected behavior.

## Description
The provided COBOL code snippet showcases a `PERFORM` loop that depends on the `WS-COUNT` variable.  If `WS-COUNT` is not properly initialized or set to a value less than the expected iteration, the loop body will not execute, resulting in unexpected or missing output.  There is also no error handling for potential issues in accessing the array out of bounds.

## Bug
The `bug.cob` file contains the flawed code. The second `PERFORM` statement incorrectly uses a potentially uninitialized counter (WS-COUNT) to control the loop, leading to an empty result if the counter is zero or negative. 

## Solution
The `bugSolution.cob` file shows the corrected code. The solution adds initialization and safeguards to handle potential issues and ensure correct program flow.