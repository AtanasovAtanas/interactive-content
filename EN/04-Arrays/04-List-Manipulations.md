# List Manipulations

[slide]
# Add Elements

We can add an element to the **end of the list** with the `append([element])` function.

```python live
my_list = [1, 2, 3]
my_list.append(4)
print(my_list) # [1, 2, 3, 4]
```

To add an element to a **specific index**, use the `insert(index, element)` function.

The first parameter is the index and the second - the element to be added.

```python live
my_list = [1, 3, 4]
my_list.insert(1, 2)
print(my_list) # [1, 2, 3, 4]
```

There is also a way to **merge two lists**.

This is done by using the `extend(list)` function.

**All** of the elements of the list **given as a parameter** will be appended to the **end** of the list that this function is being **executed over**.

```python live
my_list = [1, 2, 3]
my_list.extend([4, 5, 6])
print(my_list)
```

[/slide]

[slide]
# Problem: Courses
[code-task title="Courses" taskId="python-fund-07-Arrays-problem-3" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive a single number **n**.

On the next n lines you will receive **names** of courses.

You have to create a **list of them and print it**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | ['PB Python', 'PF Python'] |
| PB Python |  |
| PF Python |  |

| **Input** | **Output** |
| --- | --- |
| 4 | ['Front-End', 'C# Web', 'JS Core', 'Programming Fundamentals'] |
| Front-End |  |
| C# Web |  |
| JS Core |  |
| Programming Fundamentals |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
PB Python
PF Python
[/input]
[output]
\['PB Python', 'PF Python'\]
[/output]
[/test]
[test open]
[input]
4
Front-End
C\# Web
JS Core
Programming Fundamentals
[/input]
[output]
\['Front-End', 'C\# Web', 'JS Core', 'Programming Fundamentals'\]
[/output]
[/test]
[test]
[input]
1
Programming for Dummies
[/input]
[output]
\['Programming for Dummies'\]
[/output]
[/test]
[test]
[input]
3
Web for Dummies
Coding for Dummies
Life for Dummies
[/input]
[output]
\['Web for Dummies', 'Coding for Dummies', 'Life for Dummies'\]
[/output]
[/test]
[test]
[input]
5
A
B
C
D
E
[/input]
[output]
\['A', 'B', 'C', 'D', 'E'\]
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
\[\]
[/output]
[/test]
[test]
[input]
7
hello
its
me
from
the
other
side
[/input]
[output]
\['hello', 'its', 'me', 'from', 'the', 'other', 'side'\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Courses
[code-task title="Courses" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
n = int(input())
courses = []
for n in range(n):
    current_course = input()
    courses.append(current_course)
print(courses)
```
[/code-editor]
[task-description]
## Description
You will receive a single number **n**.

On the next n lines you will receive **names** of courses.

You have to create a **list of them and print it**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | ['PB Python', 'PF Python'] |
| PB Python |  |
| PF Python |  |

| **Input** | **Output** |
| --- | --- |
| 4 | ['Front-End', 'C# Web', 'JS Core', 'Programming Fundamentals'] |
| Front-End |  |
| C# Web |  |
| JS Core |  |
| Programming Fundamentals |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
PB Python
PF Python
[/input]
[output]
\['PB Python', 'PF Python'\]
[/output]
[/test]
[test open]
[input]
4
Front-End
C\# Web
JS Core
Programming Fundamentals
[/input]
[output]
\['Front-End', 'C\# Web', 'JS Core', 'Programming Fundamentals'\]
[/output]
[/test]
[test]
[input]
1
Programming for Dummies
[/input]
[output]
\['Programming for Dummies'\]
[/output]
[/test]
[test]
[input]
3
Web for Dummies
Coding for Dummies
Life for Dummies
[/input]
[output]
\['Web for Dummies', 'Coding for Dummies', 'Life for Dummies'\]
[/output]
[/test]
[test]
[input]
5
A
B
C
D
E
[/input]
[output]
\['A', 'B', 'C', 'D', 'E'\]
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
\[\]
[/output]
[/test]
[test]
[input]
7
hello
its
me
from
the
other
side
[/input]
[output]
\['hello', 'its', 'me', 'from', 'the', 'other', 'side'\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Remove Elements

To remove an element from a list, the function `remove(element)` can be used.

It removes the **first occurence** of the element given in the braces.

If such element **doesn't exist** in the list, a `ValueError` will be raised.

```python live
my_list = [1, 2, 3, 2]
my_list.remove(2)
print(my_list) # [1, 3, 2]
```

To remove **all** elements of a list, use the `clear()` function.

```python live
my_list = [1, 2, 3]
my_list.clear()
print(my_list) # []
```

There is also a way to remove an element at a **given index**, which also **returns** it.

For this purpose, the `pop([index])` function is used.

**Note:** The parameter `index` is between **square brackets**, it means that the parameter is **optional**. If **no index** is passed as a parameter, the function will remove (and return) the **last** element of the list.

```python live
my_list = [1, 2, 3, 4, 5, 6]
print(my_list.pop(2)) # 3
print(my_list.pop()) # 6
print(my_list) # [1, 2, 4, 5]
```

[/slide]