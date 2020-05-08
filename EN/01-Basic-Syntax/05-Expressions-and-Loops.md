# Expressions & Loops

[slide]
# Operators

Operators in Python work the same as other programming languages:
 - `+` stands for addition
 - `-` stands for subtraction
 - `*` stands for multiplication
 - `/` stands for division
 - `%` stands for modulus division
```python live
print(10 + 10)
print(20 - 10)
print(2 * 5)
print(10 / 2)
print(10 % 3)
```
Uncommon operators are:
- `**` stands for exponentiation
- `//` stands for floor division
```python live
print(27 // 4)
print(2 ** 5) # 5 times 2 multiplied by itself
```

[/slide]

[slide]
# If Statements
```python live
age = int(input())
age_range = None
if age < 10:
 age_range = 'child'
elif age < 18:
 age_range = 'teenager'
else:
 age_range = 'adult'

print(f'Your age range is {age_range}.')
```

[/slide]

[slide]
# For Loops

Usually use the `range([start], end, [step])` function, where the `start` and `step` arguments are **optional**.
```python live
print('Numbers from 0 to 4:')
for i in range(5):
    print(i)
```
```python live
print('Numbers from 5 to 20 by threes:')
for i in range(5, 20, 3):
    print(i)
```
**Note:** the `range()` function is **exclusive**, for example `range(0, 5)` is equivalent to [0,5).

# Reverse For Loops

The `range()` function can also produce a descending range, by giving it a **negative** `step`:
```python live
print('Numbers from 9 to 0:')
for i in range(9, -1, -1):
    print(i)
```
Another way to reverse the range is by using the `reversed()` function:
```python live
print('Numbers from 9 to 0:')
for i in reversed(range(0, 10)):
    print(i)
```

[/slide]

[slide]
# While Loops

The `while` loop executes the command(s) while the given condition is true.
```python live
i = 1
while i < 10:
    print(i)
    i += 1
```
There are two keywords that allow you to manipulate the loop:
 - `break` is used to end the loop
 - `continue` is used to skip an iteration
```python live
i = 0
while True:
    i += 1
    if i % 2 == 1:
        continue # don't print even numbers
    if i > 20:
        break
    print(i)
```

[/slide]