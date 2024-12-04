# Uncommon HTML innerHTML Bug

This repository demonstrates a subtle bug related to using `innerHTML` in HTML with a non-string value.  The issue arises when a number or other non-string data type is assigned directly to `innerHTML`.  This might not always throw an error but can lead to unexpected behavior or silent failure to update the content.

The `bug.html` file showcases the incorrect code, and `bugSolution.html` provides the corrected version.

## Bug Description
Attempting to set the `innerHTML` property of an element to a non-string value (e.g., a number) might not produce the expected output. Instead of converting the number to a string and displaying it, the browser might ignore the assignment or behave inconsistently.

## Solution
To ensure correct rendering, always convert non-string values to strings before assigning them to `innerHTML` using the `toString()` method or string concatenation.