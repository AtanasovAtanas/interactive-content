# Returning Values

[slide]
# The Return Keyword

The `return` keyword **immediately stops** the function's execution.

```python live
def print_numbers(start, end):
    for i in range(start, end):
        if (i == 5):
            return
        print(i, end=" ")

print_numbers(1, 10) # 1 2 3 4
```

In the example above, the printing **stops** at 4 because **if the number is 5**, the `return` keyword is used.

This can be used to make the **function return a value**, which can be used somehow **outside of the function**.

```python live
def sum(number_one, number_two):
    return number_one + number_two

print(sum(3, 6))
```
[/slide]

[slide]
# Using the Return Values

The **returned values** from functions can be used in many ways:
 - Assigned to a variable
 ```python live
def sum(number_one, number_two):
   return number_one + number_two

sum = sum(4, 8)
print(sum) # 12
```
 - Used in expression
```python live
def sum(number_one, number_two):
   return number_one + number_two

multiplied = sum(3, 2) * 2
print(multiplied) # 10
```
 - Passed to another function
```python live
def sum(number_one, number_two):
   return number_one + number_two

def multiply(number, multiplier):
   return number * multiplier

multiplied = multiply(sum(3, 2), 2)
print(multiplied) # 10
```
[/slide]