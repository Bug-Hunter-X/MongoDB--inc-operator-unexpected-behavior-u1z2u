# MongoDB $inc Operator Unexpected Behavior

This repository demonstrates a common error encountered when using the `$inc` operator in MongoDB update operations.  The `$inc` operator is designed to increment a numeric field by a specified value. However, attempting to increment with a non-numeric value leads to failure or unexpected results.

The `bug.js` file showcases the incorrect usage, while `bugSolution.js` provides the corrected implementation.

## Bug
The bug stems from supplying a string value ("1") to the `$inc` operator instead of a numeric value (1).  This results in the update operation not incrementing the `count` field as expected.  Depending on MongoDB's strictness, this might result in an error or simply no change.

## Solution
The solution involves correctly providing a numeric value (1) to the `$inc` operator to ensure the intended update operation takes place.
