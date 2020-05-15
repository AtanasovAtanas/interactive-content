# Functions with Parameters

[slide]
# Function Parameters

Data can be given to functions through **parameters**, thus the **function will make use of it**.

They are declared in the **braces after the function's name**.

Parameters can be **zero** or **several**.

They can be of **any data type**.

Each parameter has a **name**.

```python live
def print_name(name):
    print("Hello, " + name)

print_name("Jason")
```

Make sure you pass to the function **just as many parameters as it needs**.

You **cannot** invoke a function by passing **less or more** parameters than it needs.

```python live
def print_name(name):
    print("Hello, " + name)

print_name("Jason") # Hello, Jason
print_name() # TypeError, missing argument
print_name("Jason", "Oprah") # TypeError, more arguments
```

[/slide]

[slide]
# Problem: Grades
[code-task title="Grades" taskId="python-fundamentals-Functions-01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a function that receives a grade between 2.00 and 6.00 and prints the corresponding grade in words.
 - 2.00 – 2.99 - "Fail"
 - 3.00 – 3.49 - "Poor"
 - 3.50 – 4.49 - "Good"
 - 4.50 – 5.49 - "Very good"
 - 5.50 – 6.00 - "Excellent"

## Examples
| **Input** | **Output** |
| --- | --- |
| 3.33 | Poor |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 4.50 | Very good |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2.99 | Fail |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3.33
[/input]
[output]
Poor
[/output]
[/test]
[test open]
[input]
4.50
[/input]
[output]
Very Good
[/output]
[/test]
[test open]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
3.49
[/input]
[output]
Poor
[/output]
[/test]
[test]
[input]
4.40
[/input]
[output]
Good
[/output]
[/test]
[test]
[input]
5.50
[/input]
[output]
Excellent
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Grades
[code-task title="Grades" taskId="804bc194-e7c1-4f08-bfc1-759df3495764" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
grade_data = float(input())

def solve(grade):
    if 2.00 <= grade <= 2.99:
        print('Fail')
    elif 3.00 <= grade <= 3.49:
        print('Poor')
    elif 3.50 <= grade <= 4.49:
        print('Good')
    elif 4.50 <= grade <= 5.49:
        print('Very Good')
    elif 5.50 <= grade <= 6.00:
        print('Excellent')

solve(grade_data)
```
[/code-editor]
[task-description]
## Description
Write a function that receives a grade between 2.00 and 6.00 and prints the corresponding grade in words.
 - 2.00 – 2.99 - "Fail"
 - 3.00 – 3.49 - "Poor"
 - 3.50 – 4.49 - "Good"
 - 4.50 – 5.49 - "Very good"
 - 5.50 – 6.00 - "Excellent"

## Examples
| **Input** | **Output** |
| --- | --- |
| 3.33 | Poor |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 4.50 | Very good |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2.99 | Fail |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3.33
[/input]
[output]
Poor
[/output]
[/test]
[test open]
[input]
4.50
[/input]
[output]
Very Good
[/output]
[/test]
[test open]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
3.49
[/input]
[output]
Poor
[/output]
[/test]
[test]
[input]
4.40
[/input]
[output]
Good
[/output]
[/test]
[test]
[input]
5.50
[/input]
[output]
Excellent
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Optional Parameters

Parameters can accept **default values**.

```python
def print_numbers(start=0, end=100):
   for i in range(start, end + 1):
      print(i, end=' ')
```

Giving an argument a **default value**, gives you the possibility to **omit it when calling the function**.

Doing this, the function will be executed with its **default argument values**.

There are a few ways to call a function which has optional parameters:

```python live
def print_information(name="John Doe", location="London"):
  print(f"{name} is located in {location}")

print_information()
print_information("Peter", "New York")
print_information("Michael")
print_information(location="New Orleans")
```

[/slide]