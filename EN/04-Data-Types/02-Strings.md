# Strings

[slide]
# Strings explained

A string is a sequence of characters and it's used to represent textual data.

The first element is at `index 0`, the next at `index 1`, and so on.

Using `length - 1` we can take the last element of a string.


```python live
name ='Python'
print(name[0])
print(name[length - 1])
```

## String Literal

String literals in python are surrounded by either single quotation marks, or double quotation marks.

- `'hello'` is the same as `"hello"`

The `len()` method returns the length of a string.

The length of a String is the number of elements in it.

```python live
a = "Hello, World!"
print(len(a))
```

## Strings Are Immutable

Python strings are immutable, this means that once a string is created, it is not **possible** to modify it:

```python live
name ='Python'
name[0] ='G'
print(name)
```

When you run the example here you'll see `str object does not support item assignment` exception, which means that you can not **modify** a string.

## String Interpolation

**Python 3.6+** added a new string interpolation method called **literal string interpolation** and introduced a new literal prefix `f`.

These are string literals that allow embedded expressions:

```python live
name ='Rick'
age = 18
print(f'{name} = {age}')
```

In the above example literal prefix `f` tells Python to restore the value of two string variable `name` and `age` inside braces `{}`.

So that when we `print` we get the above output.

[/slide]

[slide]
# Problem: Concatenate Names
[code-task title="Problem: Concatenate Names" taskId="26487ea5-3211-4751-b86c-63366828e230" executionType="tests-execution" executionStrategy="python-code" requiresInput]
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
[code-task title="Problem: Concatenate Names" executionType="tests-execution" executionStrategy="python-code" requiresInput]
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