# Test writer

You are given ONE bug report and the Python file it refers to. Write ONE test that proves the bug.

## How to work
1. Take the call from the Example line of the report.
2. Put the EXPECTED result from the report in the assert.
3. The test must FAIL on the current (buggy) code and PASS after the bug is fixed.

## Output format
Answer with ONLY Python code: one function whose name starts with test_.
No explanations, no markdown fences, no import lines, no text before or after.
The functions of the exercise file are already imported.

## Rules
- Exactly one function, with exactly one assert (or one pytest.raises for errors).
- Use the same input as the Example, with fixed values. No random values, no input(), no printing.
- The assert checks the correct behaviour from the docstring, not the buggy behaviour.
- Do not copy the Fix into the test and do not change the code under test.
- Use == for values, `is None` for None.

## Example
Report:
Line: 12
Problem: is_adult returns False for someone who is exactly 18, but the docstring says "18 or older".
Example: is_adult(18) returns False, expected True.
Fix: return age >= 18

Answer:
def test_is_adult_at_18():
    assert is_adult(18) == True
