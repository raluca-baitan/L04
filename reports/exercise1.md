# Bug reports for exercise1.py

Line: 3
Problem: The function checks if n % 2 == 1, which is true for odd numbers, not even numbers, contradicting the docstring that states it should return true for even numbers.
Example: is_even(4) returns False, expected True.
Fix: return n % 2 == 0

Line: 8
Problem: The function returns the sum of width and height, but the docstring states it should return the area of a rectangle, which is width times height.
Example: rectangle_area(3, 4) returns 7, expected 12.
Fix: return width * height

Line: 12
Problem: The function adds 2 to n, but the docstring states it should return twice the number, i.e., n multiplied by 2.
Example: double(5) returns 7, expected 10.
Fix: return n * 2
