---
created: 2024-01-21T01:00
updated: 2024-01-21T01:06
---
Write a python program to Find  maximum number between three numbers.Here's the Python program to find the maximum number between three numbers:

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
num3 = float(input("Enter third number: "))

if (num1 >= num2) and (num1 >= num3):
    largest = num1
elif (num2 >= num1) and (num2 >= num3):
    largest = num2
else:
    largest = num3

print("The largest number is", largest)
```

In this program, we first take three numbers as input from the user using the `input()` function. We then use nested `if-else` statements to compare these numbers and find out which one is the largest.

The `if` statement checks if `num1` is greater than or equal to both `num2` and `num3`. If it is, then we assign `largest` variable to `num1`.

The second `elif` statement checks if `num2` is greater than or equal to both `num1` and `num3`. If it is, then we assign `largest` variable to `num2`.

If none of the above conditions are true, then it means that the third number (`num3`) must be the largest. So, we assign that value to the variable named `largest`.

Finally, we print out the value of the `largest` variable using the `print()` function. 