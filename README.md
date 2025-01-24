# Closure issue in Javascript/Typescript using setTimeout in a loop.
This repository demonstrates a common closure-related issue in Javascript/Typescript when using `setTimeout` within a loop.  The problem arises because the loop variable `i` is not captured correctly in each iteration of the loop.  This leads to unexpected behavior. 

## The Problem
The `printNumbers2` function attempts to print numbers 1 through 5 with a slight delay using `setTimeout`. However, due to the closure behavior, all the `setTimeout` callbacks end up referencing the final value of `i` after the loop has completed.

## The Solution
The solution involves using an immediately invoked function expression (IIFE) or `let` within the loop to create a new scope for each iteration, thus capturing the correct value of `i` for each callback.