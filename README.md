# Uncommon COBOL Logic Error: Ineffective Loop Counter

This repository demonstrates a subtle logic error in a COBOL program. The code appears to use a loop, but the loop counter is not effectively utilized in the calculations within the loop, leading to unexpected results.

## Bug Description

The COBOL program intends to calculate a total using a loop.  However, the `ADD 1 TO WS-TOTAL` statement within the loop ignores the value of `WS-COUNTER`.  This results in the program always calculating a total of 10, regardless of the loop's range.

## How to Reproduce

1. Compile and run the `bug.cob` file.
2. Observe that the output is 'Total: 10', even though a loop is used.

## Solution

The `bugSolution.cob` file shows the corrected code. The loop counter is used appropriately to calculate the total dynamically based on the loop's iteration.