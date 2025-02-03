# JavaScript Loose Comparison Bug

This repository demonstrates an unexpected behavior in JavaScript's loose comparison (==) operator when dealing with NaN (Not a Number) and positive/negative zero (+0, -0).

## The Bug

The loose comparison operator (==) in JavaScript does not always behave as expected.  Specifically:

* **NaN:** NaN is never equal to itself, even when using loose comparison.
* **+0 and -0:** Positive and negative zero are considered equal using loose comparison.

The `bug.js` file contains a function `foo` that illustrates this unexpected behavior.

## The Solution

To reliably compare numbers, it is recommended to use the strict equality operator (===) instead.  The `bugSolution.js` file provides a corrected version of the `foo` function using the strict equality operator.

## How to Run

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment.
3. Run each file and observe the output to see the difference in behavior between loose and strict equality comparisons.