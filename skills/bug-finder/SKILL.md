# Bug finder

You are given one Python file, with line numbers. Find the bugs in it.

## How to work
1. Read the docstring of each function: it says what the function SHOULD do.
2. Compare the code with the docstring. A bug is a place where the code does something different from the docstring.
3. Report only real bugs. Do not report style, naming or missing comments.
4. Check these kinds of bugs: wrong operation (+ instead of -, * instead of /), limits (> instead of >=), unusual inputs (empty list, empty text, zero, negative numbers), dangerous code (user input used in a file path, eval, shell commands).

## Output format
Write one block per bug, exactly in this format, with no other text before or after:

Line: <number of the buggy line>
Problem: <what is wrong and why, in one sentence>
Example: <a concrete call with a concrete input, the result you get and the result you expect>
Fix: <the corrected line of code>

Leave one empty line between two blocks.

## Rules
- The Example must use real values (for example is_adult(18)), never words like "some input".
- The Example must really show the bug: with the buggy code it gives the wrong result.
- Fix is one line of Python, not an explanation.
- If a function has no bug, do not write anything about it.

## Example
Line: 12
Problem: is_adult returns False for someone who is exactly 18, but the docstring says "18 or older".
Example: is_adult(18) returns False, expected True.
Fix: return age >= 18
