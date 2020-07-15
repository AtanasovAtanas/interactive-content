# String Manipulation

[slide]
# Video

[vimeo-video startTimeInSeconds="1674" endTimeInSeconds="2447"]
[stream language="EN" videoId="421758207" default /]
[stream language="RO" videoId="434995028"  /]
[/video-vimeo]

[/slide]

[slide]
# Concatenation

The `+` operator is used to **merge** strings:

```python live
string_one = "Hello, "
string_two = "my name is "
string_three = "Zeus."

print(string_one + string_two + string_three)
```

The `*` operator is used to **repeat** a string:

```python live
repeated = "rep" * 4
print(repeated)
print("hi" * 3)
```

[/slide]

[slide]
# String Formatting

## %-Formatting

Formatting with the `%` operator:

```python live
fruit = "apples"
vegetable = "cucumbers"
kilos = 4
str = "In the basket are %s and %s. It weights %d kilos." % (fruit, vegetable, kilos)

print(str)
```

There are the **basic argument specifiers** you should know for the `%`-formatting:

 - `%s` - used for **strings**, or any **object** with a **string representation**
 - `%d` - used for **integer numbers**
 - `%f` - used for **floating point numbers**
 - `%.{number of digits}f` - used for **floating point numbers** with a fix**ed amount of digits to the right of the dot**

```python live
pi = 3.14159265359
print("Pi is equal to %f" % pi)
print("Pi is equal to %.2f" % pi)
```

## {}-Formatting

Formatting can be done more simply, with the `{}` operator and `format()` function:

```python live
fruit = "apples"
vegetable = "cucumbers"
kilos = 4.44
str = "In the basket are {} and {}. It weights {} kilos.".format(fruit, vegetable, kilos)

print(str)
```

The **first** `{}` will be **replaced** with the **first argument** passed to the `format()` function, and so on.

## f-string Formatting

The **most modern** way of string formatting is called "f-string".

It's so far the **easiest way** to format a string.

```python live
fruit = "apples"
vegetable = "cucumbers"
kilos = 4.44
str = f"In the basket are {fruit} and {vegetable}. It weights {kilos} kilos."

print(str)
```

The `{}` operator is used again, but this time the **variable** is **passed directly** where you want it to be **placed** in the string.

[/slide]

[slide]
# Substring

**Substringing** in Python is called "**slicing**".

It can also be used on **lists**.

Works with **indices**.

Its signature looks like this:

`string[start:end]`

 - `start` - declares from which index to **start** substringing
 - `end` - declares to which index the substring to **end**; it is **exclusive**

Both can be **omitted**, and doing so, means to **start from index 0** and/or **end at the last index**.

```python live
str = "Hello, my name is Jason"
print(str[18:23]) # Jason
print(str[:5]) # Hello
print(str[7:]) # my name is Jason
```

There is also one more thing to this syntax, the `step`:

`string[start:end:step]`

It can be made to **discount** every `step` character.

The default value of `step` is 1.

```python live
str = "H e l l o J o r d a n"
print(str[::2]) # HelloJordan
print(str[10::2]) # Jordan
print(str[:9:2]) # Hello
```

[/slide]

[slide]
# Problem: Repeat Strings
[code-task title="Repeat Strings" taskId="python-fundamentals-Text-Processing-02" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that reads an **array of strings**.

Each string is repeated **N** times, where **N** is the length of the string.

Print the concatenated string.

## Examples
| **Input** | **Output** |
| --- | --- |
| hi abc add | hihiabcabcabcaddaddadd |
|  |  |

| **Input** | **Output** |
| --- | --- |
| work | workworkworkwork |
|  |  |

| **Input** | **Output** |
| --- | --- |
| ball | ballballballball |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
hi abc add
[/input]
[output]
hihiabcabcabcaddaddadd
[/output]
[/test]
[test open]
[input]
work
[/input]
[output]
workworkworkwork
[/output]
[/test]
[test open]
[input]
ball
[/input]
[output]
ballballballball
[/output]
[/test]
[test]
[input]
p r t
[/input]
[output]
prt
[/output]
[/test]
[test]
[input]
pas s word
[/input]
[output]
paspaspasswordwordwordword
[/output]
[/test]
[test]
[input]
fail pass test
[/input]
[output]
failfailfailfailpasspasspasspasstesttesttesttest
[/output]
[/test]
[test]
[input]
djimi humu humu nuku nuku apua
[/input]
[output]
djimidjimidjimidjimidjimihumuhumuhumuhumuhumuhumuhumuhumunukunukunukunukunukunukunukunukuapuaapuaapuaapua
[/output]
[/test]
[test]
[input]
KJ!@318 12kjkk2 92991 p
[/input]
[output]
KJ!@318KJ!@318KJ!@318KJ!@318KJ!@318KJ!@318KJ!@31812kjkk212kjkk212kjkk212kjkk212kjkk212kjkk212kjkk29299192991929919299192991p
[/output]
[/test]
[test]
[input]
1 22 333 4444 55555
[/input]
[output]
1222233333333344444444444444445555555555555555555555555
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Repeat Strings
[code-task title="Repeat Strings" taskId="af67bdee-6416-4cb9-821f-85962ede59da" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
strings = input().split(" ")
result = ""
for word in strings:
    length = len(word)
    result += word * length
print(result)
```
[/code-editor]
[task-description]
## Description
Write a program that reads an **array of strings**.

Each string is repeated **N** times, where **N** is the length of the string.

Print the concatenated string.

## Examples
| **Input** | **Output** |
| --- | --- |
| hi abc add | hihiabcabcabcaddaddadd |
|  |  |

| **Input** | **Output** |
| --- | --- |
| work | workworkworkwork |
|  |  |

| **Input** | **Output** |
| --- | --- |
| ball | ballballballball |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
hi abc add
[/input]
[output]
hihiabcabcabcaddaddadd
[/output]
[/test]
[test open]
[input]
work
[/input]
[output]
workworkworkwork
[/output]
[/test]
[test open]
[input]
ball
[/input]
[output]
ballballballball
[/output]
[/test]
[test]
[input]
p r t
[/input]
[output]
prt
[/output]
[/test]
[test]
[input]
pas s word
[/input]
[output]
paspaspasswordwordwordword
[/output]
[/test]
[test]
[input]
fail pass test
[/input]
[output]
failfailfailfailpasspasspasspasstesttesttesttest
[/output]
[/test]
[test]
[input]
djimi humu humu nuku nuku apua
[/input]
[output]
djimidjimidjimidjimidjimihumuhumuhumuhumuhumuhumuhumuhumunukunukunukunukunukunukunukunukuapuaapuaapuaapua
[/output]
[/test]
[test]
[input]
KJ!@318 12kjkk2 92991 p
[/input]
[output]
KJ!@318KJ!@318KJ!@318KJ!@318KJ!@318KJ!@318KJ!@31812kjkk212kjkk212kjkk212kjkk212kjkk212kjkk212kjkk29299192991929919299192991p
[/output]
[/test]
[test]
[input]
1 22 333 4444 55555
[/input]
[output]
1222233333333344444444444444445555555555555555555555555
[/output]
[/test]
[/tests]
[/code-task]
[/slide]