# Numbers



[slide]
# Numbers
The numeric types in Python are:
- `int`
- `float`

You can create а numeric types when you assign a number value to a variable:

```Python
x = 1    # int
y = 2.8  # float
```

# Int

Int, or integer is:
- **whole** number
- positive or negative
- without decimals
- with unlimited length, depends on the memory of your computer

```Python
x = 1
y = 231223423352
z = -2312312
```

# Float
Float, or **floating-point number** is:
- number containing one decimal
- positive or negative


```Python
x = 2.10
y = 3.0
z = -15.59
```
[/slide]

[slide]
# Problem: Centuries to Minutes
[code-task title="Problem: Centuries to Minutes" taskId="python-fund-04-Data-Types-problem-2" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Write program to enter an integer number of centuries and convert it to **years**, **days**, **hours** and **minutes**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 | 1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes |
| 5 | 5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes |

### Hint
- Assume that a year has 365.2422 days at average; 

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1
[/input]
[output]
1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes
[/output]
[/test]
[test open]
[input]
5
[/input]
[output]
5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
10 centuries = 1000 years = 365242 days = 8765808 hours = 525948480 minutes
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
8 centuries = 800 years = 292193 days = 7012632 hours = 420757920 minutes
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
4 centuries = 400 years = 146096 days = 3506304 hours = 210378240 minutes
[/output]
[/test]
[test]
[input]
21
[/input]
[output]
21 centuries = 2100 years = 767008 days = 18408192 hours = 1104491520 minutes
[/output]
[/test]
[test]
[input]
100
[/input]
[output]
100 centuries = 10000 years = 3652422 days = 87658128 hours = 5259487680 minutes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Centuries to Minutes
[code-task title="Problem: Centuries to Minutes" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
centuries = int(input())

years = centuries * 100
days = int(years * 365.2422)
hours = 24 * days
minutes = 60 * hours

print(f"{centuries} centuries = {years} years = {days} days = {hours} hours = {minutes} minutes")
```
[/code-editor]
[task-description]
## Description
Write program to enter an integer number of centuries and convert it to **years**, **days**, **hours** and **minutes**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 | 1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes |
| 5 | 5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes |

### Hint
- Assume that a year has 365.2422 days at average; 

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1
[/input]
[output]
1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes
[/output]
[/test]
[test open]
[input]
5
[/input]
[output]
5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
10 centuries = 1000 years = 365242 days = 8765808 hours = 525948480 minutes
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
8 centuries = 800 years = 292193 days = 7012632 hours = 420757920 minutes
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
4 centuries = 400 years = 146096 days = 3506304 hours = 210378240 minutes
[/output]
[/test]
[test]
[input]
21
[/input]
[output]
21 centuries = 2100 years = 767008 days = 18408192 hours = 1104491520 minutes
[/output]
[/test]
[test]
[input]
100
[/input]
[output]
100 centuries = 10000 years = 3652422 days = 87658128 hours = 5259487680 minutes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]