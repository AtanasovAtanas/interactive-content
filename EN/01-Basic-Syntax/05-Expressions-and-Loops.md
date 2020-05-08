# Expressions & Loops

[slide]
# Operators

# Summing up Numbers
We can **sum** up numbers using the `+` operator:
```python live
a = 5
b = 7
sum = a + b
print(sum) # 12
```
# Subtracting Numbers
**Subtracting** numbers is done using the `-` operator:
```python live
a = 15
b = 7
print(a - b) # 8
```

# Multiplying Numbers
For **multiplication** of numbers we use the `*` operator:
```python live
a = 5
b = 7
print(a * b) # 35
```

# Dividing Numbers
**Dividing** numbers is done using the `/` and `//` operators:

## Division
`/` does **floating point division**.
 - Regardless of whether we divide two integers, floating point with integer or two floating points, the obtained output is **always floating point**.
```python live
a = 5
b = 2
print(a / b) # 2.5
```

## Floor Division
`//` is used for **floor division**.

The output of a floor division represents how many times one number fits into another, without any decimal points or remainders.
 - The result is a **floating point** number only if one of the operands is:
```python live
a = 5
b = 2.0
print(a // b) # 2.0
```
 - Otherwise the result is an **integer** number:
```python live
a = 5
b = 2
print(a // b) # 2
```
Keep in mind that this type of division rounds down to the nearest low number and not to the next lowest absolute value.

See the example below:
```python live
print(11//2)
print(-11//2)
```

Here are a few more examples with the division operators:
```python live
a = 25
i = a / 4
print(i)
f = a // 4.0
print(f)
b = a // 4
print(b)
```

# Remainder
The remainder operator `%` computes the remainder after dividing its left-hand operand by its right-hand operand.
```python live
a = 7
b = 2
print(a % b)
print(3.5 % 1)
```

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
It is useful if we want to check whether a number is **even** or **odd**.

If the remainder when dividing by 2 is equal to 0, then the number is even, otherwise it is odd.

See the following example:
```python live
print(3 % 2)
print(4 % 2)
```

[/slide]

[slide]
# If Statements
One of the single most important statements in every programming language is the `if` statement.

In programming we often **check particular conditions** and perform various actions depending on the result of the check.
[image assetsSrc="02-usecase-if-statement.png" /]

This is done by `if` condition, which has the following structure:

```python
if condition:
  # condition body
```
## Example
Here if the condition of rainy weather evaluates to **true**, then the body of the statement gets executed.
```python live
weather = input()

if weather == "rainy":
    print("Take an umbrella!")
```
[/slide]

[slide]
# If-Else Conditions
The `if` construction may also contain an `else` clause to give a specific action in case the Boolean expression (which is set at the beginning `if (bool expression)`) returns a negative result (`false`).

Built this way, the conditional statement is called `if-else` and its behavior is as follows:
 - if the result of the condition is positive (`true`) – we perform some actions
 - when it is negative (`false`) – others
[image assetsSrc="02-usecase-if-else-statement.png" /]

The format of the construction is:
```python
if condition:
  # condition body
else:
  # else construction body
```
If condition is `false`, the else-statement runs.

Because a condition can’t be simultaneously `true` and `false`, the then-statement and the else-statement of an `if-else` statement can never both run.

After the then-statement or the `else`-statement runs, control is transferred to the next statement after the `if` statement.

In an `if` statement that doesn’t include an else statement, if condition is `true`, the then-statement runs.

If condition is `false`, control is transferred to the next statement after the if statement.

Both the then-statement and the else-statement can consist of a single statement or multiple statements.

The statement or statements in the then-statement and the else-statement can be of any kind, including another if statement nested inside the original if statement.

## Example
This is an extended version of the example from the previous slide.

As you can see now we have another case, which will be executed when the condition in the `if` statement turns out **false**.
```python live
weather = input()

if weather == "rainy":
    print("Take an umbrella!")
else:
    print("Leave your umbrella at home!")
```

[/slide]

[slide]
# Block of Code

Unlike other programming languages, Python uses indentation to indicate the blocks of code and not only to make it readable and pretty.

To make a block of code, you have to indent every line of the block by the same amount.

Here is an example where incorrect indentation leads to confusion:

```python live
color = "red"
if color == "red":
  print("tomato")
else:
  print("banana")
print("lemon")
```

With proper indentation:
```python live
color = "red"
if color == "red":
  print("tomato")
  print("strawberry")
else:
  print("banana")
  print("lemon")
```
[/slide]

[slide]
# For Loops

In programming it is often required to perform a block of commands multiple times.

In order to do that, the so-called loops are used.

```python
for i in iterable:
  print(i)
```
The block of code can be explained with this use case diagram:
[image assetsSrc="04-for-loop-use-case.png" /]

Usually use the `range([start], end, [step])` function, where the `start` and `step` arguments are **optional**.

 - The `start` argument specifies at which position to start the iteration, its default value is 0.
 - The `end` argument specifies at which position to end the iteration. It has no default value and is required to be specified.
 - The `step` argument specifies the incrementation, its default value is 1.
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
**Note:** the `range()` function is **exclusive**, for example `range(0, 5)` is equivalent to [0,5), it will iterate **from 0 to 4**, **not** to 5.

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

By "**condition**", we understand every expression that returns `True` or `False`. When the **condition** is **wrong**, the while loop is **interrupted**, the program **continues** to execute the remaining code after the loop.

[image assetsSrc="05-use-case-while.png" /]

## Example
```python live
i = 1
while i < 10:
    print(i)
    i += 1
```
## Keywords
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