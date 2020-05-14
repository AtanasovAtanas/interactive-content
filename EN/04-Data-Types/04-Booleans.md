# Booleans



[slide]
# What Is a Boolean?
In programming you often need to know if an expression is `True` or `False`.

You can evaluate any expression in Python, and get one of two answers, `True` or `False`.

When you compare two values, the expression is evaluated and Python returns the Boolean answer:

```python live
print(10 > 9)
print(10 == 9)
print(10 < 9)
```

# Comparisons and Conditions

| Operator | Description | Example |
|---|---|---|
| `==` | equal | `if (day == 'Monday')` |
| `>` | greater than | `if (salary > 9000)` | 
| `<` | less than | `if (age < 18)` | 
| `>=` | greater than or equal | `if (6 >= 6)` |
| `!=` | not equal | `if (5 != 5)` |
| `is` | Object identity | `n = 'a'` <br/> `m = 'a'` <br\> `n is m == True`|
| `is not` | negated object identity | `n is not m == False` |

[/slide]

[slide]
# Boolean Examples

- Almost any value is evaluated to `True` if it has some sort of content:

```python live
print(bool("abc"))
print(bool(123))
```

- Any string is `True`, except **empty strings**:

```python live
x = "Hello"
print(bool(x))

y = ""
print(bool(y))
```

- Any number is `True`, **except 0**:

```python live
numberOne = 1
print(bool(numberOne))

numberTwo = 0
print(bool(numberTwo))

numberTwo = None
print(bool(numberTwo))
```

[/slide]

[slide]
# Problem: Special Numbers
[code-task title="Problem: Special Numbers" taskId="python-fundamentals-Data-Types-03" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
A **number** is **special** when its **sum of digits is 5, 7 or 11**.

Write a program to read an integer **n** and for all numbers in the range **1…n** to print the number and if it is special or not **\(True / False\)**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 15 |1 -> False |
| |2 -> False|
| |3 -> False|
| |4 -> False|
| |5 -> True|
| |6 -> False|
| |7 -> True|
| |8 -> False|
| |9 -> False|
| |10 -> False|
| |11 -> False|
| |12 -> False|
| |13 -> False|
| |14 -> True|
| |15 -> False|


[/task-description]
[code-io /]
[tests]
[test open]
[input]
15
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
[/output]
[/test]
[test]
[input]
6
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
[/output]
[/test]
[test]
[input]
18
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
16 -\> True
17 -\> False
18 -\> False
[/output]
[/test]
[test]
[input]
20
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
16 -\> True
17 -\> False
18 -\> False
19 -\> False
20 -\> False
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Special Numbers
[code-task title="Problem: Special Numbers" taskId="aba46b3b-4052-4418-bf3e-3a9810509f61" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
num = input()

for n in range(1, int(num) + 1):
  total = sum(int(i) for i in str(n))

if total in [5, 7, 11]:
  print(f "{n} -> True")
else :
  print(f "{n} -> False")
```
[/code-editor]
[task-description]
## Description
A **number** is **special** when its **sum of digits is 5, 7 or 11**.

Write a program to read an integer **n** and for all numbers in the range **1…n** to print the number and if it is special or not **\(True / False\)**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 15 |1 -> False |
| |2 -> False|
| |3 -> False|
| |4 -> False|
| |5 -> True|
| |6 -> False|
| |7 -> True|
| |8 -> False|
| |9 -> False|
| |10 -> False|
| |11 -> False|
| |12 -> False|
| |13 -> False|
| |14 -> True|
| |15 -> False|


[/task-description]
[code-io /]
[tests]
[test open]
[input]
15
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
[/output]
[/test]
[test]
[input]
6
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
[/output]
[/test]
[test]
[input]
18
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
16 -\> True
17 -\> False
18 -\> False
[/output]
[/test]
[test]
[input]
20
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
16 -\> True
17 -\> False
18 -\> False
19 -\> False
20 -\> False
[/output]
[/test]
[/tests]
[/code-task]
[/slide]