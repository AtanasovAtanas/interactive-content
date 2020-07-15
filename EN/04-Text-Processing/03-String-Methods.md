# String Methods

[slide]
# Video

[vimeo-video startTimeInSeconds="2447" endTimeInSeconds="5357"]
[stream language="EN" videoId="421758207" default /]
[stream language="RO" videoId="434995028"  /]
[/video-vimeo]

[/slide]

[slide]
# isdigit()

There is a built-in method, `isdigit()`, that helps you check if a **character is a digit**:

```python live
print('1'.isdigit()) # True
print('k'.isdigit()) # False
```

It **returns** a **boolean** value.

**Note:** It **cannot** be used on **anything other than a string**.

```python live
a = '3'
print(a.isdigit()) # True
a = 3
print(a.isdigit()) # AttributeError
```

[/slide]

[slide]
# islower() and isupper()

Two built-in methods help you check if a **character is lowercase or uppercase**.

They are the `islower()` and `isupper()` methods:

```python live
print('p'.islower()) # True
print('p'.isupper()) # False
print('P'.islower()) # False
print('P'.isupper()) # True
```

Using those methods on a **string** (more than 1 character) tells you whether **all characters are lower/uppercase**.

```python live
print('meow'.islower()) # True
print('mEOw'.isupper()) # False
print('mEOw'.islower()) # False
print('MEOW'.isupper()) # True
```

**Note:** It **cannot** be used on **anything other than a string**.

```python live
a = 'meow'
print(a.islower()) # True
a = '3'
print(a.islower()) # False
a = 3
print(a.islower()) # AttributeError
```

[/slide]

[slide]
# lower() and upper()

There are built-in methods, `lower()` and `upper()`, that help you **convert strings to upper and lowercase**.

```python live
text = "heLlO"
print(text.lower()) # hello
print(text.upper()) # HELLO
```

**Note:** It **cannot** be used on **anything other than a string**.

```python live
a = 'mEOw'
print(a.lower()) # meow
a = '3'
print(a.lower()) # 3
a = 3
print(a.lower()) # AttributeError
```

[/slide]

[slide]
# strip()

There is also a method, `strip()`, that **removes white spaces** in the **start** and **end** of the string.

```python live
text = "  hello   "
text = text.strip() # "hello", without white spaces
print(text + ', my name is Jade')
```

There are also the `lstrip()` and `rstrip()` methods.

The `lstrip()` **removes white spaces** in the **start** of the string, `l` stands for **left**:

```python live
text = "  hello   "
text = text.lstrip() # "hello   ", without white spaces
print(text + ', my name is Jade')
```

The `rstrip()` **removes white spaces** in the **end** of the string, `r` stands for **right**:

```python live
text = "  hello   "
text = text.rstrip() # "  hello", without white spaces
print(text + ', my name is Jade')
```

[/slide]

[slide]
# replace()

A **specified phrase** can be **replaced** with another **specified phrase** with the `replace()` method.

Its signature is:

`replace(old_value, new_value)`

Both `old_value` and `new_value` are **required**.

```python live
text = "Willow loves to code in Java."
print(text.replace("Java", "Python"))
```

There is also one more thing in the signature of the `replace()` method - `count`:

`replace(old_value, new_value, [count])`

It is **optional** and defines how many **occurrences** of `old_value` to be **replaced**, starting from the **beginning**.

By **default**, **all occurences** are replaced.

```python live
text = "This replaced has replaced to replaced be replaced"
print(text.replace("replaced", "~"))
print(text.replace("replaced", "~", 3))
```

[/slide]

[slide]
# Problem: Substring
[code-task title="Substring" taskId="python-fundamentals-Text-Processing-03" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
On the **first line** you will receive a **string**.

On the **second line** you will receive a second **string**.

Write a program that **removes all** of the **occurrences** of the **first string** in the **second until** there is **no match**.

At the end **print** the **remaining string**.

## Examples
| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| ice | kgb | We remove ice once and we get "kgiciceeb" |
| kicegiciceeb |  | We match "ice" one more time and we get "kgiceb" |
|  |  | There is one more match. The finam result is "kgb" |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
ice
kicegiciceeb
[/input]
[output]
kgb
[/output]
[/test]
[test]
[input]
Uni
SoftUniSkillsUniUni
[/input]
[output]
SoftSkills
[/output]
[/test]
[test]
[input]
zero
zeroonetwozerothree
[/input]
[output]
onetwothree
[/output]
[/test]
[test]
[input]
not
n1o2t
[/input]
[output]
n1o2t
[/output]
[/test]
[test]
[input]
fast
slowfastAndFurious
[/input]
[output]
slowAndFurious
[/output]
[/test]
[test]
[input]
br
rbrbrbrbrbr
[/input]
[output]
r
[/output]
[/test]
[test]
[input]
test
testYourtestSkills
[/input]
[output]
YourSkills
[/output]
[/test]
[test]
[input]
8
12623940398178898887787
[/input]
[output]
1262394039179777
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Substring
[code-task title="Substring" taskId="ebb0e027-097b-41ff-801d-ef28c6ffbb5d" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
first = input()
second = input()
while first in second:
    second = second.replace(first, "")
print(second)
```
[/code-editor]
[task-description]
## Description
On the **first line** you will receive a **string**.

On the **second line** you will receive a second **string**.

Write a program that **removes all** of the **occurrences** of the **first string** in the **second until** there is **no match**.

At the end **print** the **remaining string**.

## Examples
| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| ice | kgb | We remove ice once and we get "kgiciceeb" |
| kicegiciceeb |  | We match "ice" one more time and we get "kgiceb" |
|  |  | There is one more match. The finam result is "kgb" |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
ice
kicegiciceeb
[/input]
[output]
kgb
[/output]
[/test]
[test]
[input]
Uni
SoftUniSkillsUniUni
[/input]
[output]
SoftSkills
[/output]
[/test]
[test]
[input]
zero
zeroonetwozerothree
[/input]
[output]
onetwothree
[/output]
[/test]
[test]
[input]
not
n1o2t
[/input]
[output]
n1o2t
[/output]
[/test]
[test]
[input]
fast
slowfastAndFurious
[/input]
[output]
slowAndFurious
[/output]
[/test]
[test]
[input]
br
rbrbrbrbrbr
[/input]
[output]
r
[/output]
[/test]
[test]
[input]
test
testYourtestSkills
[/input]
[output]
YourSkills
[/output]
[/test]
[test]
[input]
8
12623940398178898887787
[/input]
[output]
1262394039179777
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Text Filter
[code-task title="Text Filter" taskId="python-fundamentals-Text-Processing-04" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that takes a **text** and a **string of banned words**.

All words included in the ban list should be replaced with **asterisks** "*", equal to the word's length.

The entries in the ban list will be separated by a **comma** and **space** ", ".

The ban list should be entered on the first input line and the text on the second input line.

## Examples
| **Input** | **Output** |
| --- | --- |
| Linux, Windows | It is not \*\*\*\*\*, it is GNU/\*\*\*\*\*. \*\*\*\*\* is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/\*\*\*\*\*! Sincerely, a \*\*\*\*\*\*\* client |
| It is not Linux, it is GNU/Linux. Linux is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/Linux! Sincerely, a Windows client |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Linux, Windows
It is not Linux, it is GNU/Linux. Linux is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/Linux! Sincerely, a Windows client
[/input]
[output]
It is not \*\*\*\*\*, it is GNU/\*\*\*\*\*. \*\*\*\*\* is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/\*\*\*\*\*! Sincerely, a \*\*\*\*\*\*\* client
[/output]
[/test]
[test]
[input]
palindrome
A palindrome is a word, phrase, number, or other sequence of symbols or elements, whose meaning may be interpreted the same way in either forward or reverse direction. The word \*palindrome\* was coined by the English writer Ben Jonson in the 17th century.
[/input]
[output]
A \*\*\*\*\*\*\*\*\*\* is a word, phrase, number, or other sequence of symbols or elements, whose meaning may be interpreted the same way in either forward or reverse direction. The word \*\*\*\*\*\*\*\*\*\*\*\* was coined by the English writer Ben Jonson in the 17th century.
[/output]
[/test]
[test]
[input]
warrior, now
You can't hide now I am the warrior So decide now How they'll remember you Do not hide now Act like a warrior Show your pride now Solidify your place in time
[/input]
[output]
You can't hide \*\*\* I am the \*\*\*\*\*\*\* So decide \*\*\* How they'll remember you Do not hide \*\*\* Act like a \*\*\*\*\*\*\* Show your pride \*\*\* Solidify your place in time
[/output]
[/test]
[test]
[input]
warriors, world
Brothers everywhere - raise your hands into the air We're warriors, warriors of the world Like thunder from the sky - sworn to fight and die We're warriors, warriors of the world
[/input]
[output]
Brothers everywhere - raise your hands into the air We're \*\*\*\*\*\*\*\*, \*\*\*\*\*\*\*\* of the \*\*\*\*\* Like thunder from the sky - sworn to fight and die We're \*\*\*\*\*\*\*\*, \*\*\*\*\*\*\*\* of the \*\*\*\*\*
[/output]
[/test]
[test]
[input]
animal, mind, think, losing
Branded like an animal I can still feel them burning my mind I do believe that you made your message clear I think I am losing my mind I think I am losing my mind Deprivating, isolating all that I feel Leaving me with images I know are not real
[/input]
[output]
Branded like an \*\*\*\*\*\* I can still feel them burning my \*\*\*\* I do believe that you made your message clear I \*\*\*\*\* I am \*\*\*\*\*\* my \*\*\*\* I \*\*\*\*\* I am \*\*\*\*\*\* my \*\*\*\* Deprivating, isolating all that I feel Leaving me with images I know are not real
[/output]
[/test]
[test]
[input]
Lorem, ipsum, nisi, ut
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
[/input]
[output]
\*\*\*\*\* \*\*\*\*\* dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt \*\* labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris \*\*\*\* \*\* aliquip ex ea commodo consequat.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Text Filter
[code-task title="Text Filter" taskId="8f6d51d7-a5c0-49f1-9e82-48ec659a57e6" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
words_to_censure = input().split(", ")
text = input()
for word in words_to_censure:
    while word in text:
        text = text.replace(word, "*"*len(word))
print(text)
```
[/code-editor]
[task-description]
## Description
Write a program that takes a **text** and a **string of banned words**.

All words included in the ban list should be replaced with **asterisks** "*", equal to the word's length.

The entries in the ban list will be separated by a **comma** and **space** ", ".

The ban list should be entered on the first input line and the text on the second input line.

## Examples
| **Input** | **Output** |
| --- | --- |
| Linux, Windows | It is not \*\*\*\*\*, it is GNU/\*\*\*\*\*. \*\*\*\*\* is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/\*\*\*\*\*! Sincerely, a \*\*\*\*\*\*\* client |
| It is not Linux, it is GNU/Linux. Linux is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/Linux! Sincerely, a Windows client |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Linux, Windows
It is not Linux, it is GNU/Linux. Linux is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/Linux! Sincerely, a Windows client
[/input]
[output]
It is not \*\*\*\*\*, it is GNU/\*\*\*\*\*. \*\*\*\*\* is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/\*\*\*\*\*! Sincerely, a \*\*\*\*\*\*\* client
[/output]
[/test]
[test]
[input]
palindrome
A palindrome is a word, phrase, number, or other sequence of symbols or elements, whose meaning may be interpreted the same way in either forward or reverse direction. The word \*palindrome\* was coined by the English writer Ben Jonson in the 17th century.
[/input]
[output]
A \*\*\*\*\*\*\*\*\*\* is a word, phrase, number, or other sequence of symbols or elements, whose meaning may be interpreted the same way in either forward or reverse direction. The word \*\*\*\*\*\*\*\*\*\*\*\* was coined by the English writer Ben Jonson in the 17th century.
[/output]
[/test]
[test]
[input]
warrior, now
You can't hide now I am the warrior So decide now How they'll remember you Do not hide now Act like a warrior Show your pride now Solidify your place in time
[/input]
[output]
You can't hide \*\*\* I am the \*\*\*\*\*\*\* So decide \*\*\* How they'll remember you Do not hide \*\*\* Act like a \*\*\*\*\*\*\* Show your pride \*\*\* Solidify your place in time
[/output]
[/test]
[test]
[input]
warriors, world
Brothers everywhere - raise your hands into the air We're warriors, warriors of the world Like thunder from the sky - sworn to fight and die We're warriors, warriors of the world
[/input]
[output]
Brothers everywhere - raise your hands into the air We're \*\*\*\*\*\*\*\*, \*\*\*\*\*\*\*\* of the \*\*\*\*\* Like thunder from the sky - sworn to fight and die We're \*\*\*\*\*\*\*\*, \*\*\*\*\*\*\*\* of the \*\*\*\*\*
[/output]
[/test]
[test]
[input]
animal, mind, think, losing
Branded like an animal I can still feel them burning my mind I do believe that you made your message clear I think I am losing my mind I think I am losing my mind Deprivating, isolating all that I feel Leaving me with images I know are not real
[/input]
[output]
Branded like an \*\*\*\*\*\* I can still feel them burning my \*\*\*\* I do believe that you made your message clear I \*\*\*\*\* I am \*\*\*\*\*\* my \*\*\*\* I \*\*\*\*\* I am \*\*\*\*\*\* my \*\*\*\* Deprivating, isolating all that I feel Leaving me with images I know are not real
[/output]
[/test]
[test]
[input]
Lorem, ipsum, nisi, ut
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
[/input]
[output]
\*\*\*\*\* \*\*\*\*\* dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt \*\* labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris \*\*\*\* \*\* aliquip ex ea commodo consequat.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Digits, Letters and Other
[code-task title="Digits, Letters and Other" taskId="python-fundamentals-Text-Processing-05" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that receives a **single string** and on the **first line** prints **all the digits**, on the **second** – **all the letters**, and on the **third** – **all the other characters**.

**There will always be at least one digit, one letter and one other characters**.

## Examples
| **Input** | **Output** |
| --- | --- |
| Agd#53Dfg^&4F53 | 53453 |
|  | AgdDfgF |
|  | #^& |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Agd\#53Dfg^&4F53
[/input]
[output]
53453
AgdDfgF
\#^&
[/output]
[/test]
[test]
[input]
asdkj3\#\\$%543%\\$5\#%4safa
[/input]
[output]
354354
asdkjsafa
\#\\$%%\\$\#%
[/output]
[/test]
[test]
[input]
a1!
[/input]
[output]
1
a
!
[/output]
[/test]
[test]
[input]
a!a!24
[/input]
[output]
24
aa
!!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Digits, Letters and Other
[code-task title="Digits, Letters and Other" taskId="eb497ba6-47be-4e37-919a-9e951d4333f8" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
line = input()

digits = []
letters = []
others = []

for ch in line:
    if ch.isdigit():
        digits.append(ch)
    elif ch.isalpha():
        letters.append(ch)
    else:
        others.append(ch)

print("".join(digits))
print("".join(letters))
print("".join(others))
```
[/code-editor]
[task-description]
## Description
Write a program that receives a **single string** and on the **first line** prints **all the digits**, on the **second** – **all the letters**, and on the **third** – **all the other characters**.

**There will always be at least one digit, one letter and one other characters**.

## Examples
| **Input** | **Output** |
| --- | --- |
| Agd#53Dfg^&4F53 | 53453 |
|  | AgdDfgF |
|  | #^& |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Agd\#53Dfg^&4F53
[/input]
[output]
53453
AgdDfgF
\#^&
[/output]
[/test]
[test]
[input]
asdkj3\#\\$%543%\\$5\#%4safa
[/input]
[output]
354354
asdkjsafa
\#\\$%%\\$\#%
[/output]
[/test]
[test]
[input]
a1!
[/input]
[output]
1
a
!
[/output]
[/test]
[test]
[input]
a!a!24
[/input]
[output]
24
aa
!!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]