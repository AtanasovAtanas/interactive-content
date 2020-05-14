# Strings


[slide]
# Strings

A string is a sequence of characters ands it's used to represent textual data.

The first element is at `index 0`, the next at `index 1` and so on.

The length of a String is the number of elements in it.

```python live
name ='Python'
print(name[0])
```

# String Literal

String literals in python are surrounded by either single quotation marks, or double quotation marks.

- `'hello'` is the same as `"hello"`.

The `len()` method returns  the length of a string: 

```python live
a ="Hello, World!"
print(len(a))
```
# Strings Are Immutable

Python strings are immutable, this means that once a string is created, it is not **possible** to modify it:

```python live
name ='Python'
name[0] ='G'
print(name)
```
[/slide]

[slide]
# String Interpolation 
**Python 3.6+** added new string interpolation method called **literal string interpolation** and introduced a new literal prefix `f`. 

These are string literals that allow embedded expressions:

```python live
name ='Rick'
age = 18
print(f'{name} = {age}')
```
In above example literal prefix `f` tells Python to restore the value of two string variable `name` and `age` inside braces `{}`.

So that when we `print` we get the above output.

[/slide]

[slide]
# Problem: Concatenate Names
[code-task title="Problem: Concatenate Names" taskId="python-fundamentals-Data-Types-01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Read two names and a delimiter.

Print the names joined by the delimiter.

## Examples
| **Input** | **Output** |
| --- | --- |
| John | John->Smith |
| Smith | |
| -> | |  

| **Input** | **Output** |
| --- | --- |
| Jan | Linda=>Terry |
| White | |
| => | | 

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John
Smith
-\>
[/input]
[output]
John-\>Smith
[/output]
[/test]
[test open]
[input]
Jan
White
\<-\>
[/input]
[output]
Jan\<-\>White
[/output]
[/test]
[test open]
[input]
Linda
Terry
=\>
[/input]
[output]
Linda=\>Terry
[/output]
[/test]
[test]
[input]
A
B
-
[/input]
[output]
A-B
[/output]
[/test]
[test]
[input]
Some
Name
separator
[/input]
[output]
SomeseparatorName
[/output]
[/test]
[test]
[input]
Other
Name
7
[/input]
[output]
Other7Name
[/output]
[/test]
[test]
[input]
Awe
me
so
[/input]
[output]
Awesome
[/output]
[/test]
[test]
[input]
AB
CD
(=)
[/input]
[output]
AB(=)CD
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Concatenate Names
[code-task title="Problem: Concatenate Names" taskId="829f528b-7b4a-4e3f-a01a-a1cc1fd94606" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
first_name = input()
last_name = input()
delimiter = input()
print(f'{first_name}{delimiter}{last_name}')
```
[/code-editor]
[task-description]
## Description
Read two names and a delimiter.

Print the names joined by the delimiter.

## Examples
| **Input** | **Output** |
| --- | --- |
| John | John->Smith |
| Smith | |
| -> | |  

| **Input** | **Output** |
| --- | --- |
| Jan | Linda=>Terry |
| White | |
| => | | 

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John
Smith
-\>
[/input]
[output]
John-\>Smith
[/output]
[/test]
[test open]
[input]
Jan
White
\<-\>
[/input]
[output]
Jan\<-\>White
[/output]
[/test]
[test open]
[input]
Linda
Terry
=\>
[/input]
[output]
Linda=\>Terry
[/output]
[/test]
[test]
[input]
Some
Name
separator
[/input]
[output]
SomeseparatorName
[/output]
[/test]
[test]
[input]
Other
Name
7
[/input]
[output]
Other7Name
[/output]
[/test]
[test]
[input]
Awe
me
so
[/input]
[output]
Awesome
[/output]
[/test]
[test]
[input]
AB
CD
(=)
[/input]
[output]
AB(=)CD
[/output]
[/test]
[/tests]
[/code-task]
[/slide]