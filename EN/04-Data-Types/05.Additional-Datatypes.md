# Additional Datatypes


[slide]
# Python Collections (Arrays)

There are four collection data types in the Python programming language:

- **List** is a collection which is ordered and changeable and allows duplicate members;
- **Tuple** is a collection which is ordered and unchangeable and allows duplicate members;
- **Set** is a collection which is unordered and unindexed and there are no duplicate members;
- **Dictionary** is a collection which is unordered, changeable and indexed and there are no duplicate members;

When choosing a collection type, it is useful to understand the properties of that type.

Choosing the right type for a particular data set could mean retention of meaning, and, it could mean an increase in efficiency or security.

# List
A list is a collection which is ordered and changeable. 

In Python lists are written with square brackets `[]`.

```python live
thislist = ["apple", "banana", "cherry"]
print(thislist)
```
# Tuple
A tuple is a collection which is ordered and unchangeable.

In Python tuples are written with round brackets `()`.

```python live
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```
[/slide]

[slide]
# Set
A set is a collection which is unordered and unindexed.

In Python sets are written with curly brackets `{}`.

```python live
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

# Dictionary

A dictionary is a collection which is unordered, changeable and indexed. 

In Python dictionaries are written with curly brackets `{}`, and they have keys and values.

```python live
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```
[/slide]

[slide]
# Problem: Convert Meters to Kilometers
[code-task title="Problem: Convert Meters to Kilometers" taskId="python-fundamentals-Data-Types-04" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
You will be given an integer that will be distance in **meters**.

Write a program that converts **meters** to **kilometers** formatted to the **second decimal point**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1852 |1.85 |
| 798 |0.80|



[/task-description]
[code-io /]
[tests]
[test open]
[input]
1852
[/input]
[output]
1.85
[/output]
[/test]
[test open]
[input]
798
[/input]
[output]
0.80
[/output]
[/test]
[test]
[input]
1988
[/input]
[output]
1.99
[/output]
[/test]
[test]
[input]
55922
[/input]
[output]
55.92
[/output]
[/test]
[test]
[input]
91001
[/input]
[output]
91.00
[/output]
[/test]
[test]
[input]
25441
[/input]
[output]
25.44
[/output]
[/test]
[test]
[input]
965100
[/input]
[output]
965.10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Convert Meters to Kilometers
[code-task title="Problem: Convert Meters to Kilometers" taskId="f6eee421-3a69-4ca3-bda1-7d3f5319d538" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
meters = int(input())
kilometers = meters / 1000
print('{:.2f}'.format(kilometers))
```
[/code-editor]
[task-description]
## Description
You will be given an integer that will be distance in **meters**.

Write a program that converts **meters** to **kilometers** formatted to the **second decimal point**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1852 |1.85 |
| 798 |0.80|



[/task-description]
[code-io /]
[tests]
[test open]
[input]
1852
[/input]
[output]
1.85
[/output]
[/test]
[test open]
[input]
798
[/input]
[output]
0.80
[/output]
[/test]
[test]
[input]
1988
[/input]
[output]
1.99
[/output]
[/test]
[test]
[input]
55922
[/input]
[output]
55.92
[/output]
[/test]
[test]
[input]
91001
[/input]
[output]
91.00
[/output]
[/test]
[test]
[input]
25441
[/input]
[output]
25.44
[/output]
[/test]
[test]
[input]
965100
[/input]
[output]
965.10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Pounds to Dollars
[code-task title="Problem: Pounds to Dollars" taskId="python-fundamentals-Data-Types-05" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Write a program that converts British pounds to US dollars formatted to **3th decimal point**.

1 British Pound = 1.31 Dollars

## Examples
| **Input** | **Output** |
| --- | --- |
| 80 | 104.800 |
| 39 | 51.090 |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
80
[/input]
[output]
104.800
[/output]
[/test]
[test open]
[input]
39
[/input]
[output]
51.090
[/output]
[/test]
[test]
[input]
154
[/input]
[output]
201.740
[/output]
[/test]
[test]
[input]
87
[/input]
[output]
113.970
[/output]
[/test]
[test]
[input]
977
[/input]
[output]
1279.870
[/output]
[/test]
[test]
[input]
27110
[/input]
[output]
35514.100
[/output]
[/test]
[test]
[input]
855
[/input]
[output]
1120.050
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Pounds to Dollars
[code-task title="Problem: Pounds to Dollars" taskId="fd580c8e-8678-4301-a7c7-1e8f47d9c4fc" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
pounds = int(input())
dollars = pounds * 1.31
print('{:.3f}'.format(dollars))
```
[/code-editor]
[task-description]
## Description
Write a program that converts British pounds to US dollars formatted to **3th decimal point**.

1 British Pound = 1.31 Dollars

## Examples
| **Input** | **Output** |
| --- | --- |
| 80 | 104.800 |
| 39 | 51.090 |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
80
[/input]
[output]
104.800
[/output]
[/test]
[test open]
[input]
39
[/input]
[output]
51.090
[/output]
[/test]
[test]
[input]
154
[/input]
[output]
201.740
[/output]
[/test]
[test]
[input]
87
[/input]
[output]
113.970
[/output]
[/test]
[test]
[input]
977
[/input]
[output]
1279.870
[/output]
[/test]
[test]
[input]
27110
[/input]
[output]
35514.100
[/output]
[/test]
[test]
[input]
855
[/input]
[output]
1120.050
[/output]
[/test]
[/tests]
[/code-task]
[/slide]