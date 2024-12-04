# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop.  The problem stems from how JavaScript handles variable scoping and closures.  The provided code demonstrates the bug and a solution that addresses the issue.

## Bug Description
The code initializes a `for` loop that iterates ten times and sets a `setTimeout` function to log the value of `i` after a one-second delay.  Due to how closures work in JavaScript, the value of `i` is not captured correctly for each iteration, leading to the same value (10) being logged ten times, instead of 0 through 9.

## Solution
The solution involves using an immediately invoked function expression (IIFE) to create a new scope for the variable `i`. This ensures each iteration has its own copy of `i`, effectively capturing the correct value for each `setTimeout` call.