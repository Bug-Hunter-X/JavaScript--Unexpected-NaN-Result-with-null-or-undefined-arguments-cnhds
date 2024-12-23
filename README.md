# JavaScript: Unexpected NaN Result with null or undefined arguments

This repository demonstrates a common but subtle bug in JavaScript that can lead to unexpected `NaN` (Not a Number) results when handling null or undefined function arguments.

## The Bug

The provided JavaScript code includes a function `foo` that attempts to handle null arguments gracefully. It checks if either `a` or `b` is strictly equal to null (`=== null`). However, this check doesn't account for the case where either `a` or `b` is undefined.

When an `undefined` value is passed to the function, the addition operation (`a + b`) results in `NaN`, breaking the program's expected behavior.

## Solution

The solution file provides corrected code that explicitly handles both `null` and `undefined` cases.

The improved function uses loose equality (`==`) to test for both null and undefined, thus producing a more robust result.