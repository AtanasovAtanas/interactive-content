# List Comprehensions

[slide]
# Video

[vimeo-video startTimeInSeconds="1273" endTimeInSeconds="3080"]
[stream language="EN" videoId="421712112" default /]
[stream language="RO" videoId="434994638"  /]
[/video-vimeo]

[/slide]

[slide]
# Structure

List comprehensions provide an **elegant way to create new lists**.

A list comprehension consists of a few parts:

 - An **input sequence** (iterable).
 - A **variable** that represents **each of the elements** of the **input sequence**.
 - A **predicate expression** (think of **lambda expressions**) which is **optional**.
 - An **output expression** that **produces the new list's elements** from **elements of the input sequence**.

The basic structure of a list comprehension looks like below:

```python
[return_expression] for [element] in [iterable] [optional_predicate_expression]
```

As you can see, the **keywords** `for` and `in` are used.

You are familiar with them from previous lessons.

They allow you to **go through every element of a sequence**.

[/slide]

[slide]
# Examples

The first one will be very simple, **just using the syntax above**:

```python live
x = [num for num in range(5)]
print(x) # [0, 1, 2, 3, 4]
```

In this comprehension the **input sequence** is created by the `range(5)` method and consists of the numbers from 0 to 4.

Then, we **get every element** from the **input sequence** and call the **variable** `num`.

In the beginning of the comprehension is the **output expression**, but in this example we just **pass** the `num` **without manipulating** it.

That's how we got the `[0, 1, 2, 3, 4]` **list**.

It would be the same if we just create the list with the following code:

```python live
numbers_list = list(range(5))
print(numbers_list)
```

The second example will be **without a predicate expression**, but with **manipulation in the output expression**:

```python live
grades = [3.33, 4.56, 5.50, 2.88, 3.42]
rounded_grades = [round(grade) for grade in grades]
print(rounded_grades)
```

In this example we have some **grades** which **have to be rounded**.

This is why we **round** them in the **output expression**.

In the last example for this slide, we'll have a **predicate expression**:

```python live
x = [2, 3, 'four', 'five', 6]
numbers = [element * 2 for element in x if isinstance(element, int)]
print(numbers)
```

There we **check** if the `element` is an `int`.

In case it is - we **multiply it by 2** and add pass it to the **resulting sequence**.

This can be used for **filtering sequences**, for example to get only the **odd numbers**:

```python live
numbers = [4, 12, 11, 13, 20, 0, 29]
odd_numbers = [num for num in numbers if num % 2 != 0]
print(odd_numbers) # [11, 13, 29]
```

[/slide]

[slide]
# Problem: No Vowels
[code-task title="No Vowels" taskId="python-fundamentals-comprehensions-1" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Using a comprehension write a program that receives a **text** and **removes** all the **vowels** from it.

Print the new text **string after removing the vowels**.

The vowels that should be considered are '**a**', '**o**', '**u**', '**e**', '**i**'.

## Examples
| **Input** | **Output** |
| --- | --- |
| Python | Pythn |
|  |  |

| **Input** | **Output** |
| --- | --- |
| ILovePython | LvPythn |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Python
[/input]
[output]
Pythn
[/output]
[/test]
[test open]
[input]
ILovePython
[/input]
[output]
LvPythn
[/output]
[/test]
[test]
[input]
jasklldjla
[/input]
[output]
jsklldjl
[/output]
[/test]
[test]
[input]
zxcv
[/input]
[output]
zxcv
[/output]
[/test]
[test]
[input]
qwer
[/input]
[output]
qwr
[/output]
[/test]
[test]
[input]
euroiqip
[/input]
[output]
rqp
[/output]
[/test]
[test]
[input]
qaeou
[/input]
[output]
q
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: No Vowels
[code-task title="No Vowels" taskId="7cc52049-0f2c-4794-b80b-08f26be86c72" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
text = input()
vowels = ['a', 'u', 'e', 'i', 'o', 'A', 'U', 'E', 'I', 'O']
no_vowels = ''.join([x for x in text if x not in vowels])
print(no_vowels)
```
[/code-editor]
[task-description]
## Description
Using a comprehension write a program that receives a **text** and **removes** all the **vowels** from it.

Print the new text **string after removing the vowels**.

The vowels that should be considered are '**a**', '**o**', '**u**', '**e**', '**i**'.

## Examples
| **Input** | **Output** |
| --- | --- |
| Python | Pythn |
|  |  |

| **Input** | **Output** |
| --- | --- |
| ILovePython | LvPythn |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Python
[/input]
[output]
Pythn
[/output]
[/test]
[test open]
[input]
ILovePython
[/input]
[output]
LvPythn
[/output]
[/test]
[test]
[input]
jasklldjla
[/input]
[output]
jsklldjl
[/output]
[/test]
[test]
[input]
zxcv
[/input]
[output]
zxcv
[/output]
[/test]
[test]
[input]
qwer
[/input]
[output]
qwr
[/output]
[/test]
[test]
[input]
euroiqip
[/input]
[output]
rqp
[/output]
[/test]
[test]
[input]
qaeou
[/input]
[output]
q
[/output]
[/test]
[/tests]
[/code-task]
[/slide]