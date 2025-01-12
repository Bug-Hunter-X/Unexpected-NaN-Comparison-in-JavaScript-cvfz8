# Unexpected NaN Comparison in JavaScript

This repository demonstrates a common, yet subtle, error in JavaScript related to comparing NaN (Not a Number) values.  The unexpected behavior stems from the fact that NaN is never equal to itself, regardless of whether you use loose (==) or strict (===) equality comparisons.

## The Bug

The `bug.js` file contains a simple function `foo` that attempts to compare two numbers for equality. However, when the input values are NaN, the function incorrectly returns `false` even though both values are NaN.

## The Solution

The `bugSolution.js` file offers a solution to this problem by using the `Number.isNaN()` function to explicitly check if a value is NaN before making any comparisons.