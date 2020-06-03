# Advanced Methods

[slide]
# Lambda Basics

A `lambda` operator is used for creating small, **one-time** and **anonymous** function objects in Python.

An **anonymous function** is one that is defined **without a name**.

Normal functions are defined with the `def` keyword, while the anonymous - with the `lambda` keyword.

```python
lambda arguments: expression
```

```python
lambda x: x * 2
```

The above lambda function accepts `x` parameter and returns `x * 2`.

Such functions can be saved in variables.

Now let's see it in action:

```python live
multipication = lambda x: x * 2
print(multipication(3)) # 6
```

[/slide]

[slide]
# map() Method

The `map(function, iterable)` function **executes** the **given function** for **each element of an iterable**, for example a **list**.

It returns an **iterator map object** so you need to **convert it into a list**.

There is an example that multiplies each element (number) of the list by 2:
```python live
my_list = [1, 2, 3, 4, 5]
my_list = list(map(lambda x: x * 2, my_list))
print(my_list) # [2, 4, 6, 8, 10]
```

You can pass **as many iterables as you wish**, but for this the **lambda function needs to have one parameter for each iterable**.

There is one example that uses 2 iterables and 2 parameters for the lambda:
```python live
numbers_list_one = [1, 2, 3, 4, 5]
numbers_list_two = [2, 5, 3, 10, 5]
my_list = list(map(lambda x, y: x * y, numbers_list_one, numbers_list_two))
print(my_list) # [2, 10, 9, 40, 25]
```

The example above takes each element of `numbers_list_one` and multiplies it with the element on the same index of `numbers_list_two`.

[/slide]

[slide]
# Problem: Even Numbers
[code-task title="Even Numbers" taskId="python-fund-13-Arrays-Advanced-problem-7" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that reads **a single string** with **numbers** separated by comma and space ", ".

Print the **indices** of **all even numbers**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3, 2, 1, 5, 8 | [1, 4] |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2, 4, 6, 9, 10 | [0, 1, 2, 4] |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3, 2, 1, 5, 8
[/input]
[output]
\[1, 4\]
[/output]
[/test]
[test open]
[input]
2, 4, 6, 9, 10
[/input]
[output]
\[0, 1, 2, 4\]
[/output]
[/test]
[test]
[input]
1, 3, 5, 7, 9
[/input]
[output]
\[\]
[/output]
[/test]
[test]
[input]
2, 4, 6, 8, 10
[/input]
[output]
\[0, 1, 2, 3, 4\]
[/output]
[/test]
[test]
[input]
1, 2, 3, 4, 5, 6
[/input]
[output]
\[1, 3, 5\]
[/output]
[/test]
[test]
[input]
10, 42, 55, 62, 14, 59, 999, 100, 41, 8, 66
[/input]
[output]
\[0, 1, 3, 4, 7, 9, 10\]
[/output]
[/test]
[test]
[input]
34, 2, 1, 5, 3, 65, 67, 99, 30, 12, 33, 56, 77, 998, 32, 1211, 654
[/input]
[output]
\[0, 1, 8, 9, 11, 13, 14, 16\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Even Numbers
[code-task title="Even Numbers" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
numbers = list(map(lambda x: int(x), input().split(", ")))
even_indices = []

for number in numbers:
    if number % 2 == 0:
        even_indices.append(numbers.index(number))

print(even_indices)
```
[/code-editor]
[task-description]
## Description
Write a program that reads **a single string** with **numbers** separated by comma and space ", ".

Print the **indices** of **all even numbers**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3, 2, 1, 5, 8 | [1, 4] |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2, 4, 6, 9, 10 | [0, 1, 2, 4] |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3, 2, 1, 5, 8
[/input]
[output]
\[1, 4\]
[/output]
[/test]
[test open]
[input]
2, 4, 6, 9, 10
[/input]
[output]
\[0, 1, 2, 4\]
[/output]
[/test]
[test]
[input]
1, 3, 5, 7, 9
[/input]
[output]
\[\]
[/output]
[/test]
[test]
[input]
2, 4, 6, 8, 10
[/input]
[output]
\[0, 1, 2, 3, 4\]
[/output]
[/test]
[test]
[input]
1, 2, 3, 4, 5, 6
[/input]
[output]
\[1, 3, 5\]
[/output]
[/test]
[test]
[input]
10, 42, 55, 62, 14, 59, 999, 100, 41, 8, 66
[/input]
[output]
\[0, 1, 3, 4, 7, 9, 10\]
[/output]
[/test]
[test]
[input]
34, 2, 1, 5, 3, 65, 67, 99, 30, 12, 33, 56, 77, 998, 32, 1211, 654
[/input]
[output]
\[0, 1, 8, 9, 11, 13, 14, 16\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# filter() Method

The `filter(function, iterable)` method **filters elements**, in other words - **removes elements** that **don't fulfill a given condition**.

The lambda function given **should return a boolean value** so that it can filter the elements.

It returns an **iterator map object** so you need to **convert it into a list**.

There is an example that **filters all the even numbers** of a list:
```python live
numbers_list = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers_list))
print(even_numbers) # [2, 4, 6]
```

[/slide]

[slide]
# Problem: The Office
[code-task title="The Office" taskId="python-fund-13-Arrays-Advanced-problem-9" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive **two lines** of input: a **list** of employee's happiness as **string with numbers separated by a single space** and a **happiness improvement factor** (single **number**).

Your task is to find out if the employees are generally happy in their office.

To do that you have to increase their happiness by **multiplying** the all the **employee's happiness** (the numbers from the list) **by the factor**, **filter** the employees which **happiness** is **greater** than or **equal** to the **average** in the **new list** and **print** the result.

There are two types of output:

 - If the **half or more** of the employees have **happiness >= than the average**: "**Score: {happy_count}/{unhappy_count}. Employees are happy!**"
 - Otherwise: "**Score: {happy_count}/{unhappy_count}. Employees are not happy!**"

## Examples
| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| 1 2 3 4 2 1 | Score 2/6. Employees are not happy! | After the mapping: |
| 3 |  | 3 6 9 12 6 3 |
|  |  | After the filtration: |
|  |  | 9 12 |
|  |  | 2/6 people are happy, so the overall happiness is bad |
|  |  |  |

| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| 2 3 2 1 3 3 | Score: 3/6. Employees are happy! | Half of the people are happy, so the overall happiness is good |
| 4 |  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 4 2 1
3
[/input]
[output]
Score: 2/6. Employees are not happy!
[/output]
[/test]
[test open]
[input]
2 3 2 1 3 3
4
[/input]
[output]
Score: 3/6. Employees are happy!
[/output]
[/test]
[test]
[input]
1 10 2 1 1 2
2
[/input]
[output]
Score: 1/6. Employees are not happy!
[/output]
[/test]
[test]
[input]
2 3 1 2 10 11
1
[/input]
[output]
Score: 2/6. Employees are not happy!
[/output]
[/test]
[test]
[input]
1 2 1 1 4 3 2 3 19 20 18
2
[/input]
[output]
Score: 3/11. Employees are not happy!
[/output]
[/test]
[test]
[input]
1 3 2 4 2 3 1 2 4 3 2 3 1 4 4
2
[/input]
[output]
Score: 8/15. Employees are happy!
[/output]
[/test]
[test]
[input]
1 1 2 1 2 2 2 2 1 1 3 2 2 2
2
[/input]
[output]
Score: 9/14. Employees are happy!
[/output]
[/test]
[test]
[input]
5 6 4 5 5 4 4 5 3 3 3 6 6 6 6 6 5 5
2
[/input]
[output]
Score: 12/18. Employees are happy!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: The Office
[code-task title="The Office" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
employees = input().split(" ")
happiness_factor = int(input())

employees = list(map(lambda x: int(x) * happiness_factor, employees))

filtered = list(filter(lambda x: x >= (sum(employees) / len(employees)), employees))

if len(filtered) >= len(employees) / 2:
    print(f"Score: {len(filtered)}/{len(employees)}. Employees are happy!")
else:
    print(f"Score: {len(filtered)}/{len(employees)}. Employees are not happy!")
```
[/code-editor]
[task-description]
## Description
You will receive **two lines** of input: a **list** of employee's happiness as **string with numbers separated by a single space** and a **happiness improvement factor** (single **number**).

Your task is to find out if the employees are generally happy in their office.

To do that you have to increase their happiness by **multiplying** the all the **employee's happiness** (the numbers from the list) **by the factor**, **filter** the employees which **happiness** is **greater** than or **equal** to the **average** in the **new list** and **print** the result.

There are two types of output:

 - If the **half or more** of the employees have **happiness >= than the average**: "**Score: {happy_count}/{unhappy_count}. Employees are happy!**"
 - Otherwise: "**Score: {happy_count}/{unhappy_count}. Employees are not happy!**"

## Examples
| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| 1 2 3 4 2 1 | Score 2/6. Employees are not happy! | After the mapping: |
| 3 |  | 3 6 9 12 6 3 |
|  |  | After the filtration: |
|  |  | 9 12 |
|  |  | 2/6 people are happy, so the overall happiness is bad |
|  |  |  |

| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| 2 3 2 1 3 3 | Score: 3/6. Employees are happy! | Half of the people are happy, so the overall happiness is good |
| 4 |  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 4 2 1
3
[/input]
[output]
Score: 2/6. Employees are not happy!
[/output]
[/test]
[test open]
[input]
2 3 2 1 3 3
4
[/input]
[output]
Score: 3/6. Employees are happy!
[/output]
[/test]
[test]
[input]
1 10 2 1 1 2
2
[/input]
[output]
Score: 1/6. Employees are not happy!
[/output]
[/test]
[test]
[input]
2 3 1 2 10 11
1
[/input]
[output]
Score: 2/6. Employees are not happy!
[/output]
[/test]
[test]
[input]
1 2 1 1 4 3 2 3 19 20 18
2
[/input]
[output]
Score: 3/11. Employees are not happy!
[/output]
[/test]
[test]
[input]
1 3 2 4 2 3 1 2 4 3 2 3 1 4 4
2
[/input]
[output]
Score: 8/15. Employees are happy!
[/output]
[/test]
[test]
[input]
1 1 2 1 2 2 2 2 1 1 3 2 2 2
2
[/input]
[output]
Score: 9/14. Employees are happy!
[/output]
[/test]
[test]
[input]
5 6 4 5 5 4 4 5 3 3 3 6 6 6 6 6 5 5
2
[/input]
[output]
Score: 12/18. Employees are happy!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]