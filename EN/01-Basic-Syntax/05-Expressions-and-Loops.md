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
# Problem: Biggest Of Three Numbers
[code-task title="Biggest Of Three Numbers" taskId="python-fundamentals-Basic-Syntax-01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that receives three whole numbers and print the biggest one.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | 5 |
| -1 |  |
| 5 |  |

| **Input** | **Output** |
| --- | --- |
| 0 |  |
| -1 |  |
| -2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
-1
5
[/input]
[output]
5
[/output]
[/test]
[test open]
[input]
0
-1
-2
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
3
-5
-221
[/input]
[output]
3
[/output]
[/test]
[test]
[input]
-42
-104
-552
[/input]
[output]
-42
[/output]
[/test]
[test]
[input]
123
4882
56
[/input]
[output]
4882
[/output]
[/test]
[test]
[input]
32
33
31
[/input]
[output]
33
[/output]
[/test]
[test]
[input]
134
245
590
[/input]
[output]
590
[/output]
[/test]
[test]
[input]
-45
-32
-1
[/input]
[output]
-1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Biggest Of Three Numbers
[code-task title="Biggest Of Three Numbers" taskId="2e2348f0-a250-49ce-8e44-6cd410873e01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
first_num = int(input())
second_num = int(input())
third_num = int(input())

if first_num > second_num and first_num > third_num:
    print(first_num)
elif second_num > first_num and second_num > third_num:
    print(second_num)
else:
    print(third_num)
```
[/code-editor]
[task-description]
## Description
Write a program that receives three whole numbers and print the biggest one.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | 5 |
| -1 |  |
| 5 |  |

| **Input** | **Output** |
| --- | --- |
| 0 |  |
| -1 |  |
| -2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
-1
5
[/input]
[output]
5
[/output]
[/test]
[test open]
[input]
0
-1
-2
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
3
-5
-221
[/input]
[output]
3
[/output]
[/test]
[test]
[input]
-42
-104
-552
[/input]
[output]
-42
[/output]
[/test]
[test]
[input]
123
4882
56
[/input]
[output]
4882
[/output]
[/test]
[test]
[input]
32
33
31
[/input]
[output]
33
[/output]
[/test]
[test]
[input]
134
245
590
[/input]
[output]
590
[/output]
[/test]
[test]
[input]
-45
-32
-1
[/input]
[output]
-1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Number Definer
[code-task title="Number Definer" taskId="python-fundamentals-Basic-Syntax-02" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that reads a floating-point number and prints "zero" if the number is zero.

Otherwise, print "positive" or "negative".

Add "small" if the absolute value of the number is less than 1, or "large" if it exceeds 1 000 000.

## Examples
| **Input** | **Output** |
| --- | --- |
| 25 | positive |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 0.7 | small positive |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 435247392.921 | large positive |
|  |  |

| **Input** | **Output** |
| --- | --- |
| -0.005 | small negative |
|  |  |

| **Input** | **Output** |
| --- | --- |
| -103.21 | negative |
|  |  |

| **Input** | **Output** |
| --- | --- |
| -358583355123.001 | large negative |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
25
[/input]
[output]
positive
[/output]
[/test]
[test open]
[input]
0.7
[/input]
[output]
small positive
[/output]
[/test]
[test open]
[input]
435247392.921
[/input]
[output]
large positive
[/output]
[/test]
[test open]
[input]
-0.005
[/input]
[output]
small negative
[/output]
[/test]
[test open]
[input]
-103.21
[/input]
[output]
negative
[/output]
[/test]
[test open]
[input]
-358583355123.001
[/input]
[output]
large negative
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
zero
[/output]
[/test]
[test]
[input]
0.999
[/input]
[output]
small positive
[/output]
[/test]
[test]
[input]
1000000.01
[/input]
[output]
large positive
[/output]
[/test]
[test]
[input]
1.001
[/input]
[output]
positive
[/output]
[/test]
[test]
[input]
-0.999
[/input]
[output]
small negative
[/output]
[/test]
[test]
[input]
-1000000.001
[/input]
[output]
large negative
[/output]
[/test]
[test]
[input]
-1.001
[/input]
[output]
negative
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Number Definer
[code-task title="Number Definer" taskId="633de16d-3fab-49da-8c47-6008dba08c5c" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
number = float(input())
if number == 0:
    print("zero")
elif number > 0:
    if number < 1:
        print("small positive")
    elif number > 1000000:
        print("large positive")
    else:
        print("positive")
else:
    if abs(number) < 1:
        print("small negative")
    elif abs(number) > 1000000:
        print("large negative")
    else:
        print("negative")
```
[/code-editor]
[task-description]
## Description
Write a program that reads a floating-point number and prints "zero" if the number is zero.

Otherwise, print "positive" or "negative".

Add "small" if the absolute value of the number is less than 1, or "large" if it exceeds 1 000 000.

## Examples
| **Input** | **Output** |
| --- | --- |
| 25 | positive |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 0.7 | small positive |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 435247392.921 | large positive |
|  |  |

| **Input** | **Output** |
| --- | --- |
| -0.005 | small negative |
|  |  |

| **Input** | **Output** |
| --- | --- |
| -103.21 | negative |
|  |  |

| **Input** | **Output** |
| --- | --- |
| -358583355123.001 | large negative |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
25
[/input]
[output]
positive
[/output]
[/test]
[test open]
[input]
0.7
[/input]
[output]
small positive
[/output]
[/test]
[test open]
[input]
435247392.921
[/input]
[output]
large positive
[/output]
[/test]
[test open]
[input]
-0.005
[/input]
[output]
small negative
[/output]
[/test]
[test open]
[input]
-103.21
[/input]
[output]
negative
[/output]
[/test]
[test open]
[input]
-358583355123.001
[/input]
[output]
large negative
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
zero
[/output]
[/test]
[test]
[input]
0.999
[/input]
[output]
small positive
[/output]
[/test]
[test]
[input]
1000000.01
[/input]
[output]
large positive
[/output]
[/test]
[test]
[input]
1.001
[/input]
[output]
positive
[/output]
[/test]
[test]
[input]
-0.999
[/input]
[output]
small negative
[/output]
[/test]
[test]
[input]
-1000000.001
[/input]
[output]
large negative
[/output]
[/test]
[test]
[input]
-1.001
[/input]
[output]
negative
[/output]
[/test]
[/tests]
[/code-task]
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
# Problem: Word Reverse
[code-task title="Word Reverse" taskId="python-fundamentals-Basic-Syntax-03" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that receives a single word from the user, reverses it and prints it.

## Examples
| **Input** | **Output** |
| --- | --- |
| Python | nohtyP |
|  |  |

| **Input** | **Output** |
| --- | --- |
| banana | ananab |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Python
[/input]
[output]
nohtyP
[/output]
[/test]
[test open]
[input]
banana
[/input]
[output]
ananab
[/output]
[/test]
[test]
[input]
asdf
[/input]
[output]
fdsa
[/output]
[/test]
[test]
[input]
potato
[/input]
[output]
otatop
[/output]
[/test]
[test]
[input]
ppythhonN
[/input]
[output]
Nnohhtypp
[/output]
[/test]
[test]
[input]
aaaaa
[/input]
[output]
aaaaa
[/output]
[/test]
[test]
[input]
super test
[/input]
[output]
tset repus
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Word Reverse
[code-task title="Word Reverse" taskId="b3bdc4ef-3e08-4396-8eec-96f6e6b6a1bc" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
word = input()
reversed_word = ""
for i in range(len(word) - 1, -1, -1):
    reversed_word += word[i]
print(reversed_word)
```
[/code-editor]
[task-description]
## Description
Write a program that receives a single word from the user, reverses it and prints it.

## Examples
| **Input** | **Output** |
| --- | --- |
| Python | nohtyP |
|  |  |

| **Input** | **Output** |
| --- | --- |
| banana | ananab |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Python
[/input]
[output]
nohtyP
[/output]
[/test]
[test open]
[input]
banana
[/input]
[output]
ananab
[/output]
[/test]
[test]
[input]
asdf
[/input]
[output]
fdsa
[/output]
[/test]
[test]
[input]
potato
[/input]
[output]
otatop
[/output]
[/test]
[test]
[input]
ppythhonN
[/input]
[output]
Nnohhtypp
[/output]
[/test]
[test]
[input]
aaaaa
[/input]
[output]
aaaaa
[/output]
[/test]
[test]
[input]
super test
[/input]
[output]
tset repus
[/output]
[/test]
[/tests]
[/code-task]
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

[slide]
# Problem: Number between 1 and 100
[code-task title="Number between 1 and 100" taskId="python-fundamentals-Basic-Syntax-04" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program which reads numbers from the console until it receives a number between 1 and 100 inclusive.

When the correct number is received, stop reading and print "The number {number} is between 1 and 100".

## Examples
| **Input** | **Output** |
| --- | --- |
| -3 | The number 44.0 is between 1 and 100 |
| 0.9 |  |
| 44 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
-3
0.9
44
[/input]
[output]
The number 44.0 is between 1 and 100
[/output]
[/test]
[test]
[input]
0.5
90
-4
101
[/input]
[output]
The number 90.0 is between 1 and 100
[/output]
[/test]
[test]
[input]
0.999
1
15
7
[/input]
[output]
The number 1.0 is between 1 and 100
[/output]
[/test]
[test]
[input]
100.001
99.999
-0.487
[/input]
[output]
The number 99.999 is between 1 and 100
[/output]
[/test]
[test]
[input]
-1
-42
0.999
1.4
3
19
101
[/input]
[output]
The number 1.4 is between 1 and 100
[/output]
[/test]
[test]
[input]
1.5
[/input]
[output]
The number 1.5 is between 1 and 100
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Number between 1 and 100
[code-task title="Number between 1 and 100" taskId="30970d74-fc78-49ff-8b57-5508977cd269" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
number = float(input())
while number < 1 or number > 100:
    number = float(input())
print(f'The number {number} is between 1 and 100')
```
[/code-editor]
[task-description]
## Description
Write a program which reads numbers from the console until it receives a number between 1 and 100 inclusive.

When the correct number is received, stop reading and print "The number {number} is between 1 and 100".

## Examples
| **Input** | **Output** |
| --- | --- |
| -3 | The number 44.0 is between 1 and 100 |
| 0.9 |  |
| 44 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
-3
0.9
44
[/input]
[output]
The number 44.0 is between 1 and 100
[/output]
[/test]
[test]
[input]
0.5
90
-4
101
[/input]
[output]
The number 90.0 is between 1 and 100
[/output]
[/test]
[test]
[input]
0.999
1
15
7
[/input]
[output]
The number 1.0 is between 1 and 100
[/output]
[/test]
[test]
[input]
100.001
99.999
-0.487
[/input]
[output]
The number 99.999 is between 1 and 100
[/output]
[/test]
[test]
[input]
-1
-42
0.999
1.4
3
19
101
[/input]
[output]
The number 1.4 is between 1 and 100
[/output]
[/test]
[test]
[input]
1.5
[/input]
[output]
The number 1.5 is between 1 and 100
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Patterns
[code-task title="Patterns" taskId="python-fundamentals-Basic-Syntax-05" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program to create the following pattern:

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | * |
|  | ** |
|  | *** |
|  | ** |
|  | * |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 5 | * |
|  | ** |
|  | *** |
|  | **** |
|  | ***** |
|  | **** |
|  | *** |
|  | ** |
|  | * |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
[/input]
[output]
\*
\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test open]
[input]
5
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
20
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
\*
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Patterns
[code-task title="Patterns" taskId="da379840-8f89-4209-bc98-fa1132f09920" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
number = int(input())
for i in range(1, number + 1):
    for j in range(0, i):
        print('*', end='')
    print()
for i in range(number - 1, 0, -1):
    for j in range(0, i):
        print('*', end='')
    print()
```
[/code-editor]
[task-description]
## Description
Write a program to create the following pattern:

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | * |
|  | ** |
|  | *** |
|  | ** |
|  | * |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 5 | * |
|  | ** |
|  | *** |
|  | **** |
|  | ***** |
|  | **** |
|  | *** |
|  | ** |
|  | * |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
[/input]
[output]
\*
\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test open]
[input]
5
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
20
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*
\*\*\*\*\*\*
\*\*\*\*\*
\*\*\*\*
\*\*\*
\*\*
\*
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
\*
[/output]
[/test]
[/tests]
[/code-task]
[/slide]