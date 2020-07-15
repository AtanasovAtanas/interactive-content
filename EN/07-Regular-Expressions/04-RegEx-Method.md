# RegEx Method

[slide]
# Video

[vimeo-video startTimeInSeconds="5724" endTimeInSeconds="8248"]
[stream language="EN" videoId="435033424" default /]
[stream language="RO" videoId="435046150"  /]
[/video-vimeo]

[/slide]

[slide]
# RegEx Method

The `findall()` methid returns a list containing all matches in the order they are found:

```Python live
import re

txt = "The sun is shining in Bucharest"
x = re.findall("in", txt)

print(x)
```

If **no matches** are found, an **empty list** is returned:

```Python live
import re

txt = "The sun is shining in Bucharest"
x = re.findall("up", txt)

print(x)
```

# Method split()

The `split()` function returns a list where the string has been split at each match:

```Python live
import re

txt = "The sun is shining in Bucharest"
x = re.split("\s", txt)

print(x)
```
# Method search()

The `search()` function will check all lines of the input string for a match, and returns a **Match object** if there is a match.

If there is more than one match, only the **first occurrence** of the match will be returned:

```Python live
import re

str = "The sun is shining in Bucharest"
x = re.search("\s", str)

print("The first white-space character is located in position:", x.start())
```

If no matches are found, you'll receive `AttributeError: 'NoneType' object has no attribute`

```Python live
import re

str = "The sun is shining in Bucharest"
x = re.search("\d", str)

print("The first white-space character is located in position:", x.start())
```
[/slide]

[slide]
# Problem: Match Full Name
[code-task title="Problem: Match Full Name" taskId="f2d8764b-9b28-45ce-9db1-48b4d514a8f3" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Write a program to **match full names** from a list of names and **print** them on the console.

## Examples
| **Input** | **Output** |
| --- | --- |
| **Ivan Ivanov**, Ivan ivanov, ivan Ivanov, IVan Ivanov, **Test Testov**, Ivan	Ivanov | Ivan Ivanov Test Testov |

### Writing the Regular Expression
First, write a regular expression to match a valid full name, according to these conditions.

A valid full name has the following characteristics:
- It consists of two words
- Each word starts with a capital letter
- After the first letter, it only contains lowercase letters afterward
- Each of the two words should be at least two letters long
- The two words are separated by a single space

To help you out, we've outlined several steps:

- Use the online regex tester [Pythex](https://pythex.org)
- Check out how to use character sets denoted with square brackets - `[]`
- Specify that you want **two words** with a space between them the space character `' '`, and not any whitespace symbol
- For each word, specify that it should **begin** with an **uppercase letter** using a character set.
The desired characters are in a range – from `A` to `Z`.

- For each word, specify that what follows the first letter are only **lowercase letters**, one or more, use another character set and the correct quantifier
- To prevent capturing of letters across new lines, put `\b` at the **beginning** and at the end of your regex.
This will ensure that what precedes and what follows the match is a word boundary, like a new line


[/task-description]
[code-io /]
[tests]
[test open]
[input]
Ivan Ivanov, Ivan ivanov, ivan Ivanov, IVan Ivanov, Test Testov, Ivan	Ivanov
[/input]
[output]
Ivan Ivanov Test Testov
[/output]
[/test]
[test]
[input]
gosho goshov-Xi Ban cc DD-e e gosho goshov gosho goshov-pesho ivanov-PESHO IVANOV-AA PESHO IVANOV A A aa Ivan Ivanov B B-d d EE-ivanivanov-D D Ivan Ivanov
[/input]
[output]
Xi Ban Ivan Ivanov Ivan Ivanov
[/output]
[/test]
[test]
[input]
c c-PESHO IVANOV GOSHO GOSHOV-D D-GoshoGoshov goshogoshov-bb d d-CC d d A A-IvanIvanov A A-xiban gosho goshov-Xi Ban xi ban-BB-pesho petrov XiBan-
[/input]
[output]
Xi Ban
[/output]
[/test]
[test]
[input]
GOSHO GOSHOV-peshopetrov-c c ivanivanov peshoivanov-PeshoPetrov-PeshoIvanov-DD-PeshoPetrov Xi Ban-D D-IvanIvanov-D D-dd-aa pesho petrov PeshoIvanov-XI BAN-cc-ivan ivanov-
[/input]
[output]
Xi Ban
[/output]
[/test]
[test]
[input]
EE-e e pesho petrov-PeshoPetrov aa-gosho goshov-peshoivanov-B B EE-Pesho Petrov-Pesho Ivanov peshoivanov-BB Gosho Goshov GOSHO GOSHOV cc XiBan b b-ivanivanov CC
[/input]
[output]
Pesho Petrov Pesho Ivanov Gosho Goshov
[/output]
[/test]
[test]
[input]
d d gosho goshov XiBan pesho ivanov-Pesho Petrov-xiban-Pesho Ivanov pesho petrov-Pesho Petrov-IvanIvanov-Pesho Petrov-PESHO IVANOV-EE EE C C-Pesho Ivanov-peshoivanov-bb XiBan-aa
[/input]
[output]
Pesho Petrov Pesho Ivanov Pesho Petrov Pesho Petrov Pesho Ivanov
[/output]
[/test]
[test]
[input]
Xi Ban-GoshoGoshov B B-PeshoIvanov xiban B B aa C C-goshogoshov-IvanIvanov PeshoPetrov-PeshoIvanov C C ivan ivanov-Pesho Ivanov-IVAN IVANOV C C-PESHO IVANOV-PESHO IVANOV ivan ivanov
[/input]
[output]
Xi Ban Pesho Ivanov
[/output]
[/test]
[test]
[input]
A A-Xi Ban b b-C C ee XiBan-gosho goshov GoshoGoshov AA-IvanIvanov BB-cc-pesho petrov DD goshogoshov ivan ivanov IvanIvanov-pesho ivanov a a-gosho goshov-
[/input]
[output]
Xi Ban
[/output]
[/test]
[test]
[input]
gosho goshov-aa-C C-PESHO IVANOV PESHO PETROV-A A xi ban A A aa-peshopetrov Gosho Goshov d d-E E DD XI BAN-bb-Gosho Goshov-aa-dd ivan ivanov-
[/input]
[output]
Gosho Goshov Gosho Goshov
[/output]
[/test]
[test]
[input]
Gosho Goshov a a C C-GoshoGoshov EE PeshoPetrov-a a xi ban D D bb b b-B B-c c EE-IvanIvanov DD pesho ivanov B B PESHO IVANOV IVAN IVANOV-
[/input]
[output]
Gosho Goshov
[/output]
[/test]
[test]
[input]
goshogoshov peshoivanov-c c-XiBan-cc-Ivan Ivanov-D D IVAN IVANOV xi ban BB-xiban-PESHO PETROV xiban Ivan Ivanov-XI BAN-cc-IVAN IVANOV EE c c e e
[/input]
[output]
Ivan Ivanov Ivan Ivanov
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Match Full Name
[code-task title="Problem: Match Full Name" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
import re

pattern = r'\b[A-Z][a-z]+[ ][A-Z][a-z]+\b'

text = input()

matches = re.findall(pattern, text)

print(' '.join(matches))
```
[/code-editor]
[task-description]
## Description
Write a program to **match full names** from a list of names and **print** them on the console.

## Examples
| **Input** | **Output** |
| --- | --- |
|**Ivan Ivanov**, Ivan ivanov, ivan Ivanov, IVan Ivanov, **Test Testov**, Ivan	Ivanov | Ivan Ivanov Test Testov |

### Writing the Regular Expression
First, write a regular expression to match a valid full name, according to these conditions.

A valid full name has the following characteristics:
- It consists of two words
- Each word starts with a capital letter
- After the first letter, it only contains lowercase letters afterward
- Each of the two words should be at least two letters long
- The two words are separated by a single space

To help you out, we've outlined several steps:

- Use the online regex tester [Pythex](https://pythex.org)
- Check out how to use character sets denoted with square brackets - `[]`
- Specify that you want **two words** with a space between them the space character `' '`, and not any whitespace symbol
- For each word, specify that it should **begin** with an **uppercase letter** using a character set.
The desired characters are in a range – from `A` to `Z`.

- For each word, specify that what follows the first letter are only **lowercase letters**, one or more, use another character set and the correct quantifier
- To prevent capturing of letters across new lines, put `\b` at the **beginning** and at the end of your regex.
This will ensure that what precedes and what follows the match is a word boundary, like a new line


[/task-description]
[code-io /]
[tests]
[test open]
[input]
Ivan Ivanov, Ivan ivanov, ivan Ivanov, IVan Ivanov, Test Testov, Ivan	Ivanov
[/input]
[output]
Ivan Ivanov Test Testov
[/output]
[/test]
[test]
[input]
gosho goshov-Xi Ban cc DD-e e gosho goshov gosho goshov-pesho ivanov-PESHO IVANOV-AA PESHO IVANOV A A aa Ivan Ivanov B B-d d EE-ivanivanov-D D Ivan Ivanov
[/input]
[output]
Xi Ban Ivan Ivanov Ivan Ivanov
[/output]
[/test]
[test]
[input]
c c-PESHO IVANOV GOSHO GOSHOV-D D-GoshoGoshov goshogoshov-bb d d-CC d d A A-IvanIvanov A A-xiban gosho goshov-Xi Ban xi ban-BB-pesho petrov XiBan-
[/input]
[output]
Xi Ban
[/output]
[/test]
[test]
[input]
GOSHO GOSHOV-peshopetrov-c c ivanivanov peshoivanov-PeshoPetrov-PeshoIvanov-DD-PeshoPetrov Xi Ban-D D-IvanIvanov-D D-dd-aa pesho petrov PeshoIvanov-XI BAN-cc-ivan ivanov-
[/input]
[output]
Xi Ban
[/output]
[/test]
[test]
[input]
EE-e e pesho petrov-PeshoPetrov aa-gosho goshov-peshoivanov-B B EE-Pesho Petrov-Pesho Ivanov peshoivanov-BB Gosho Goshov GOSHO GOSHOV cc XiBan b b-ivanivanov CC
[/input]
[output]
Pesho Petrov Pesho Ivanov Gosho Goshov
[/output]
[/test]
[test]
[input]
d d gosho goshov XiBan pesho ivanov-Pesho Petrov-xiban-Pesho Ivanov pesho petrov-Pesho Petrov-IvanIvanov-Pesho Petrov-PESHO IVANOV-EE EE C C-Pesho Ivanov-peshoivanov-bb XiBan-aa
[/input]
[output]
Pesho Petrov Pesho Ivanov Pesho Petrov Pesho Petrov Pesho Ivanov
[/output]
[/test]
[test]
[input]
Xi Ban-GoshoGoshov B B-PeshoIvanov xiban B B aa C C-goshogoshov-IvanIvanov PeshoPetrov-PeshoIvanov C C ivan ivanov-Pesho Ivanov-IVAN IVANOV C C-PESHO IVANOV-PESHO IVANOV ivan ivanov
[/input]
[output]
Xi Ban Pesho Ivanov
[/output]
[/test]
[test]
[input]
A A-Xi Ban b b-C C ee XiBan-gosho goshov GoshoGoshov AA-IvanIvanov BB-cc-pesho petrov DD goshogoshov ivan ivanov IvanIvanov-pesho ivanov a a-gosho goshov-
[/input]
[output]
Xi Ban
[/output]
[/test]
[test]
[input]
gosho goshov-aa-C C-PESHO IVANOV PESHO PETROV-A A xi ban A A aa-peshopetrov Gosho Goshov d d-E E DD XI BAN-bb-Gosho Goshov-aa-dd ivan ivanov-
[/input]
[output]
Gosho Goshov Gosho Goshov
[/output]
[/test]
[test]
[input]
Gosho Goshov a a C C-GoshoGoshov EE PeshoPetrov-a a xi ban D D bb b b-B B-c c EE-IvanIvanov DD pesho ivanov B B PESHO IVANOV IVAN IVANOV-
[/input]
[output]
Gosho Goshov
[/output]
[/test]
[test]
[input]
goshogoshov peshoivanov-c c-XiBan-cc-Ivan Ivanov-D D IVAN IVANOV xi ban BB-xiban-PESHO PETROV xiban Ivan Ivanov-XI BAN-cc-IVAN IVANOV EE c c e e
[/input]
[output]
Ivan Ivanov Ivan Ivanov
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Match Phone Number
[code-task title="Problem: Match Phone Number" taskId="56c11a7c-67ea-4ae4-a3f8-80d2f39d52da" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Write a regular expression to match a valid phone number from Sofia.

After you find all valid phones, print them on the console, separated by a comma and a space `, `.

## Examples
| **Input** | **Output** |
| --- | --- |
| **+359 2 222 2222**,359-2-222-2222, +359/2/222/2222, +359-2 222 2222 +359 2-222-2222, +359-2-222-222, +359-2-222-22222 **+359-2-222-2222** | +359 2 222 2222, +359-2-222-2222 |

A valid number has the following characteristics:

- It starts with `+359`
- Then, it is followed by the area code (always 2)
- After that, it's followed by the **number** itself:
 The number consists of **7 digits**, separated in two groups of 3 and 4 digits respectively
- The different parts are **separated** by either a space or a hyphen `-`.

You can use the following RegEx properties to help with the matching:
- Use **quantifiers** to match a specific number of digits
- Use a **capturing group** to make sure the delimiter is only one of the allowed characters, space or hyphen and not a combination of both (e.g. +359 2-111 111 has mixed delimiters, it is invalid). 
Use a group backreference to achieve this.
- Add a **word boundary** at the end of the match to avoid partial matches, the last example on the right-hand side
- Ensure that before the `+` sign there is either a space or the beginning of the string.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
+359 2 222 2222,359-2-222-2222, +359/2/222/2222, +359-2 222 2222 +359 2-222-2222, +359-2-222-222, +359-2-222-22222 +359-2-222-2222
[/input]
[output]
+359 2 222 2222, +359-2-222-2222
[/output]
[/test]
[test]
[input]
+359-2-376-7398 +359-2-854-2280 -359 2 222 2222 -359 2 222 2222 +359 1 123 4567 +359-2-789-2584 +359 2 727 9740 +359 2 819 7146 +359 2 558 8560 +359-2-376-7398 +359-2-961-0248 +359-2-376-7398 +359 2 262 8203 +359 2 22 2222 +359-2-191-9995
[/input]
[output]
+359-2-376-7398, +359-2-854-2280, +359-2-789-2584, +359 2 727 9740, +359 2 819 7146, +359 2 558 8560, +359-2-376-7398, +359-2-961-0248, +359-2-376-7398, +359 2 262 8203, +359-2-191-9995
[/output]
[/test]
[test]
[input]
+359 2 357 3351 +359 2 22 2222 +359 2 173 3408 +359-2-789-2584 +359 2 193 3953 +359-2-961-0248 +359-2-789-2584 +359 2 222 222 +360 2 222 2222 +359 2 727 9740 +359-2-854-2280 +359 2 193 3953 +359 2 357 3351 +359 2 558 8560 +359 2 222 222
[/input]
[output]
+359 2 357 3351, +359 2 173 3408, +359-2-789-2584, +359 2 193 3953, +359-2-961-0248, +359-2-789-2584, +359 2 727 9740, +359-2-854-2280, +359 2 193 3953, +359 2 357 3351, +359 2 558 8560
[/output]
[/test]
[test]
[input]
+359-2-645-6120 +359 2 680 6053 +359 2 262 8203 +359 2 262 8203 +359 2 717 0238 +359-2-961-0248 +359 1 123 4567 +359 2 173 3408 +359-2-977-0618 +360 2 222 2222 +359 2 123 1273 +359 2 177 2605 +359 2 177 2605 +359 2 558 8560 +359-2-789-2584
[/input]
[output]
+359-2-645-6120, +359 2 680 6053, +359 2 262 8203, +359 2 262 8203, +359 2 717 0238, +359-2-961-0248, +359 2 173 3408, +359-2-977-0618, +359 2 123 1273, +359 2 177 2605, +359 2 177 2605, +359 2 558 8560, +359-2-789-2584
[/output]
[/test]
[test]
[input]
+359-2-376-7398 +359 2 558 8560 +360 2 222 2222 +359 2 073 2128 +359 2 628 8897 +359 2 123 1273 +359 2 819 7146 +359-2-191-9995 +359-2-645-6120 +359 2 262 8203 +359 2 123 1273 +359 2 073 2128 +359-2-191-9995 +359 2 22 2222 +359 2 073 2128
[/input]
[output]
+359-2-376-7398, +359 2 558 8560, +359 2 073 2128, +359 2 628 8897, +359 2 123 1273, +359 2 819 7146, +359-2-191-9995, +359-2-645-6120, +359 2 262 8203, +359 2 123 1273, +359 2 073 2128, +359-2-191-9995, +359 2 073 2128
[/output]
[/test]
[test]
[input]
+359 2 222 222 +359-2-961-0248 +359 2 717 0238 +359-2-789-2584 +359-2-376-7398 +359 2 173 3408 +359-2-977-0618 +359 2 680 6053 +359 2 22 2222 +359 2 22 2222 +359 2 680 6053 +359-2-191-9995 +359 2 819 7146 +359 2 262 8203 +359-2-854-2280
[/input]
[output]
+359-2-961-0248, +359 2 717 0238, +359-2-789-2584, +359-2-376-7398, +359 2 173 3408, +359-2-977-0618, +359 2 680 6053, +359 2 680 6053, +359-2-191-9995, +359 2 819 7146, +359 2 262 8203, +359-2-854-2280
[/output]
[/test]
[test]
[input]
+359 2 173 3408 +359 1 123 4567 +359 2 22 2222 +359 2 727 9740 +359 2 222 222 +359 2 262 8203 +359 2 222 222 +359-2-191-9995 +359 2 22 2222 +359 1 123 4567 +359 2 717 0238 +359 2 193 3953 +359 1 123 4567 +359 2 193 3953 +359 1 123 4567
[/input]
[output]
+359 2 173 3408, +359 2 727 9740, +359 2 262 8203, +359-2-191-9995, +359 2 717 0238, +359 2 193 3953, +359 2 193 3953
[/output]
[/test]
[test]
[input]
+359 2 680 6053 +359 1 123 4567 +359-2-191-9995 +359 2 073 2128 +359 2 262 8203 +359-2-789-2584 +359 2 173 3408 +359 2 717 0238 +359-2-645-6120 +359 2 628 8897 +359 2 222 222 +359 2 177 2605 +359-2-191-9995 +359-2-645-6120 +359-2-191-9995
[/input]
[output]
+359 2 680 6053, +359-2-191-9995, +359 2 073 2128, +359 2 262 8203, +359-2-789-2584, +359 2 173 3408, +359 2 717 0238, +359-2-645-6120, +359 2 628 8897, +359 2 177 2605, +359-2-191-9995, +359-2-645-6120, +359-2-191-9995
[/output]
[/test]
[test]
[input]
+359 2 123 1273 +359 2 222 222 +359 2 262 8203 +359 2 717 0238 +359-2-789-2584 +359 2 727 9740 +359-2-376-7398 +359 2 123 1273 +359 2 680 6053 +359 2 193 3953 +359 2 262 8203 +359-2-854-2280 +359 2 558 8560 +359 2 558 8560 +360 2 222 2222
[/input]
[output]
+359 2 123 1273, +359 2 262 8203, +359 2 717 0238, +359-2-789-2584, +359 2 727 9740, +359-2-376-7398, +359 2 123 1273, +359 2 680 6053, +359 2 193 3953, +359 2 262 8203, +359-2-854-2280, +359 2 558 8560, +359 2 558 8560
[/output]
[/test]
[test]
[input]
+359-2-376-7398 +359 2 727 9740 +359 2 680 6053 -359 2 222 2222 +359 2 123 1273 +359-2-961-0248 +359 2 22 2222 +359 2 173 3408 +359 2 558 8560 +359 2 073 2128 +359 2 357 3351 +359-2-789-2584 +359 2 717 0238 +359 2 073 2128 +359 2 22 2222
[/input]
[output]
+359-2-376-7398, +359 2 727 9740, +359 2 680 6053, +359 2 123 1273, +359-2-961-0248, +359 2 173 3408, +359 2 558 8560, +359 2 073 2128, +359 2 357 3351, +359-2-789-2584, +359 2 717 0238, +359 2 073 2128
[/output]
[/test]
[test]
[input]
-359 2 222 2222 +359 2 357 3351 +359-2-191-9995 -359 2 222 2222 +359 2 222 222 +359-2-789-2584 +359-2-376-7398 +359 1 123 4567 +360 2 222 2222 +359 2 22 2222 +359 2 262 8203 +359 2 193 3953 +359 2 177 2605 +359 2 073 2128 +359 2 073 2128
[/input]
[output]
+359 2 357 3351, +359-2-191-9995, +359-2-789-2584, +359-2-376-7398, +359 2 262 8203, +359 2 193 3953, +359 2 177 2605, +359 2 073 2128, +359 2 073 2128
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Match Phone Number
[code-task title="Problem: Match Phone Number" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
import re

phones = input()

reg = "(\\+359-2-[0-9]{3}-[0-9]{4}|\\+359 2 [0-9]{3} [0-9]{4})\\b"
matches = re.findall(reg, phones)

print(', '.join(matches))
```
[/code-editor]
[task-description]
## Description
Write a regular expression to match a valid phone number from Sofia.

After you find all valid phones, print them on the console, separated by a comma and a space `, `.

## Examples
| **Input** | **Output** |
| --- | --- |
| **+359 2 222 2222**,359-2-222-2222, +359/2/222/2222, +359-2 222 2222 +359 2-222-2222, +359-2-222-222, +359-2-222-22222 **+359-2-222-2222** | +359 2 222 2222, +359-2-222-2222 |

A valid number has the following characteristics:

- It starts with `+359`
- Then, it is followed by the area code (always 2)
- After that, it's followed by the **number** itself:
 The number consists of **7 digits**, separated in two groups of 3 and 4 digits respectively
- The different parts are **separated** by either a space or a hyphen `-`.

You can use the following RegEx properties to help with the matching:
- Use **quantifiers** to match a specific number of digits
- Use a **capturing group** to make sure the delimiter is only one of the allowed characters, space or hyphen and not a combination of both (e.g. +359 2-111 111 has mixed delimiters, it is invalid). 
Use a group backreference to achieve this.
- Add a **word boundary** at the end of the match to avoid partial matches, the last example on the right-hand side
- Ensure that before the `+` sign there is either a space or the beginning of the string.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
+359 2 222 2222,359-2-222-2222, +359/2/222/2222, +359-2 222 2222 +359 2-222-2222, +359-2-222-222, +359-2-222-22222 +359-2-222-2222
[/input]
[output]
+359 2 222 2222, +359-2-222-2222
[/output]
[/test]
[test]
[input]
+359-2-376-7398 +359-2-854-2280 -359 2 222 2222 -359 2 222 2222 +359 1 123 4567 +359-2-789-2584 +359 2 727 9740 +359 2 819 7146 +359 2 558 8560 +359-2-376-7398 +359-2-961-0248 +359-2-376-7398 +359 2 262 8203 +359 2 22 2222 +359-2-191-9995
[/input]
[output]
+359-2-376-7398, +359-2-854-2280, +359-2-789-2584, +359 2 727 9740, +359 2 819 7146, +359 2 558 8560, +359-2-376-7398, +359-2-961-0248, +359-2-376-7398, +359 2 262 8203, +359-2-191-9995
[/output]
[/test]
[test]
[input]
+359 2 357 3351 +359 2 22 2222 +359 2 173 3408 +359-2-789-2584 +359 2 193 3953 +359-2-961-0248 +359-2-789-2584 +359 2 222 222 +360 2 222 2222 +359 2 727 9740 +359-2-854-2280 +359 2 193 3953 +359 2 357 3351 +359 2 558 8560 +359 2 222 222
[/input]
[output]
+359 2 357 3351, +359 2 173 3408, +359-2-789-2584, +359 2 193 3953, +359-2-961-0248, +359-2-789-2584, +359 2 727 9740, +359-2-854-2280, +359 2 193 3953, +359 2 357 3351, +359 2 558 8560
[/output]
[/test]
[test]
[input]
+359-2-645-6120 +359 2 680 6053 +359 2 262 8203 +359 2 262 8203 +359 2 717 0238 +359-2-961-0248 +359 1 123 4567 +359 2 173 3408 +359-2-977-0618 +360 2 222 2222 +359 2 123 1273 +359 2 177 2605 +359 2 177 2605 +359 2 558 8560 +359-2-789-2584
[/input]
[output]
+359-2-645-6120, +359 2 680 6053, +359 2 262 8203, +359 2 262 8203, +359 2 717 0238, +359-2-961-0248, +359 2 173 3408, +359-2-977-0618, +359 2 123 1273, +359 2 177 2605, +359 2 177 2605, +359 2 558 8560, +359-2-789-2584
[/output]
[/test]
[test]
[input]
+359-2-376-7398 +359 2 558 8560 +360 2 222 2222 +359 2 073 2128 +359 2 628 8897 +359 2 123 1273 +359 2 819 7146 +359-2-191-9995 +359-2-645-6120 +359 2 262 8203 +359 2 123 1273 +359 2 073 2128 +359-2-191-9995 +359 2 22 2222 +359 2 073 2128
[/input]
[output]
+359-2-376-7398, +359 2 558 8560, +359 2 073 2128, +359 2 628 8897, +359 2 123 1273, +359 2 819 7146, +359-2-191-9995, +359-2-645-6120, +359 2 262 8203, +359 2 123 1273, +359 2 073 2128, +359-2-191-9995, +359 2 073 2128
[/output]
[/test]
[test]
[input]
+359 2 222 222 +359-2-961-0248 +359 2 717 0238 +359-2-789-2584 +359-2-376-7398 +359 2 173 3408 +359-2-977-0618 +359 2 680 6053 +359 2 22 2222 +359 2 22 2222 +359 2 680 6053 +359-2-191-9995 +359 2 819 7146 +359 2 262 8203 +359-2-854-2280
[/input]
[output]
+359-2-961-0248, +359 2 717 0238, +359-2-789-2584, +359-2-376-7398, +359 2 173 3408, +359-2-977-0618, +359 2 680 6053, +359 2 680 6053, +359-2-191-9995, +359 2 819 7146, +359 2 262 8203, +359-2-854-2280
[/output]
[/test]
[test]
[input]
+359 2 173 3408 +359 1 123 4567 +359 2 22 2222 +359 2 727 9740 +359 2 222 222 +359 2 262 8203 +359 2 222 222 +359-2-191-9995 +359 2 22 2222 +359 1 123 4567 +359 2 717 0238 +359 2 193 3953 +359 1 123 4567 +359 2 193 3953 +359 1 123 4567
[/input]
[output]
+359 2 173 3408, +359 2 727 9740, +359 2 262 8203, +359-2-191-9995, +359 2 717 0238, +359 2 193 3953, +359 2 193 3953
[/output]
[/test]
[test]
[input]
+359 2 680 6053 +359 1 123 4567 +359-2-191-9995 +359 2 073 2128 +359 2 262 8203 +359-2-789-2584 +359 2 173 3408 +359 2 717 0238 +359-2-645-6120 +359 2 628 8897 +359 2 222 222 +359 2 177 2605 +359-2-191-9995 +359-2-645-6120 +359-2-191-9995
[/input]
[output]
+359 2 680 6053, +359-2-191-9995, +359 2 073 2128, +359 2 262 8203, +359-2-789-2584, +359 2 173 3408, +359 2 717 0238, +359-2-645-6120, +359 2 628 8897, +359 2 177 2605, +359-2-191-9995, +359-2-645-6120, +359-2-191-9995
[/output]
[/test]
[test]
[input]
+359 2 123 1273 +359 2 222 222 +359 2 262 8203 +359 2 717 0238 +359-2-789-2584 +359 2 727 9740 +359-2-376-7398 +359 2 123 1273 +359 2 680 6053 +359 2 193 3953 +359 2 262 8203 +359-2-854-2280 +359 2 558 8560 +359 2 558 8560 +360 2 222 2222
[/input]
[output]
+359 2 123 1273, +359 2 262 8203, +359 2 717 0238, +359-2-789-2584, +359 2 727 9740, +359-2-376-7398, +359 2 123 1273, +359 2 680 6053, +359 2 193 3953, +359 2 262 8203, +359-2-854-2280, +359 2 558 8560, +359 2 558 8560
[/output]
[/test]
[test]
[input]
+359-2-376-7398 +359 2 727 9740 +359 2 680 6053 -359 2 222 2222 +359 2 123 1273 +359-2-961-0248 +359 2 22 2222 +359 2 173 3408 +359 2 558 8560 +359 2 073 2128 +359 2 357 3351 +359-2-789-2584 +359 2 717 0238 +359 2 073 2128 +359 2 22 2222
[/input]
[output]
+359-2-376-7398, +359 2 727 9740, +359 2 680 6053, +359 2 123 1273, +359-2-961-0248, +359 2 173 3408, +359 2 558 8560, +359 2 073 2128, +359 2 357 3351, +359-2-789-2584, +359 2 717 0238, +359 2 073 2128
[/output]
[/test]
[test]
[input]
-359 2 222 2222 +359 2 357 3351 +359-2-191-9995 -359 2 222 2222 +359 2 222 222 +359-2-789-2584 +359-2-376-7398 +359 1 123 4567 +360 2 222 2222 +359 2 22 2222 +359 2 262 8203 +359 2 193 3953 +359 2 177 2605 +359 2 073 2128 +359 2 073 2128
[/input]
[output]
+359 2 357 3351, +359-2-191-9995, +359-2-789-2584, +359-2-376-7398, +359 2 262 8203, +359 2 193 3953, +359 2 177 2605, +359 2 073 2128, +359 2 073 2128
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Match Dates
[code-task title="Problem: Match Dates" taskId="42746a86-baf4-47d5-bbd8-a7a54dba4775" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Write a program, which matches a date in the format `dd{separator}MMM{separator}yyyy`.

Use capturing groups in your regular expression.

## Examples
| **Input** | **Output** |
| --- | --- |
| **13/Jul/1928**, **10-Nov-1934**, , 01/Jan-1951,f **25.Dec.1937** 23/09/1973, 1/Feb/2016 | Day: 13, Month: Jul, Year: 1928 |
|  | Day: 10, Month: Nov, Year: 1934 |
|  | Day: 25, Month: Dec, Year: 1937 |

Every valid date has the following characteristics:
- Always starts with **two digits**, followed by a **separator**
- After that, it has **one uppercase** and **two lowercase** letters e.g. Jan, Mar
- After that, it has a **separator** and **exactly 4 digits**, for the year
- The separator could be either of three things: a period `.`, a hyphen `-` or a forward slash `/`
- The separator needs to be the same for the whole date (e.g. `13.03.2016` **is valid**, 13.03/2016 is NOT).

Use a group backreference to check for this.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
13/Jul/1928, 10-Nov-1934, 01/Jan-1951, 25.Dec.1937, 23/09/1973, 1/Feb/2016
[/input]
[output]
Day: 13, Month: Jul, Year: 1928
Day: 10, Month: Nov, Year: 1934
Day: 25, Month: Dec, Year: 1937
[/output]
[/test]
[test]
[input]
01/Jan-1951 29/Feb/2024 1/Jan-1951 27-Feb-2007 1/Jan-1951 1/Mar/2016 23/october/197
[/input]
[output]
Day: 29, Month: Feb, Year: 2024
Day: 27, Month: Feb, Year: 2007
[/output]
[/test]
[test]
[input]
24.Apr.2003 1/Jan-1951 12/Jan/2024 1/Jan-1951 22.Jan.2014 1/Jan-1951 24-Sep-2014 18-Jan-2012 23/october/197
[/input]
[output]
Day: 24, Month: Apr, Year: 2003
Day: 12, Month: Jan, Year: 2024
Day: 22, Month: Jan, Year: 2014
Day: 24, Month: Sep, Year: 2014
Day: 18, Month: Jan, Year: 2012
[/output]
[/test]
[test]
[input]
1/Jan-1951 23/october/197 11-Dec-2010 18.Jan.2014
[/input]
[output]
Day: 11, Month: Dec, Year: 2010
Day: 18, Month: Jan, Year: 2014
[/output]
[/test]
[test]
[input]
04-Jan-2014 1/Jan-1951 23/october/197 23/october/197 23/Nov/2023 1/Jan-1951 27-Feb-2012 08-Mar-2000 1/Jan-1951
[/input]
[output]
Day: 04, Month: Jan, Year: 2014
Day: 23, Month: Nov, Year: 2023
Day: 27, Month: Feb, Year: 2012
Day: 08, Month: Mar, Year: 2000
[/output]
[/test]
[test]
[input]
22.Nov.2011 09.May.2013 1/Jan-1951 29/Sep/2011 24-Jul-2012 06.Oct.2013
[/input]
[output]
Day: 22, Month: Nov, Year: 2011
Day: 09, Month: May, Year: 2013
Day: 29, Month: Sep, Year: 2011
Day: 24, Month: Jul, Year: 2012
Day: 06, Month: Oct, Year: 2013
[/output]
[/test]
[test]
[input]
02/Apr/2002 1/Jan-1951 21-Feb-2019
[/input]
[output]
Day: 02, Month: Apr, Year: 2002
Day: 21, Month: Feb, Year: 2019
[/output]
[/test]
[test]
[input]
1/Jan-1951 06-Jan-2014 1/Jan-1951 30/Jun/2004 21.Nov.2000 15/Nov/2018 11.Mar.2017 1/Jan-1951
[/input]
[output]
Day: 06, Month: Jan, Year: 2014
Day: 30, Month: Jun, Year: 2004
Day: 21, Month: Nov, Year: 2000
Day: 15, Month: Nov, Year: 2018
Day: 11, Month: Mar, Year: 2017
[/output]
[/test]
[test]
[input]
11/Aug/2005 18/Oct/2021 1/Jan-1951 30.Oct.2004 25/Aug/2002 13-Aug-2016
[/input]
[output]
Day: 11, Month: Aug, Year: 2005
Day: 18, Month: Oct, Year: 2021
Day: 30, Month: Oct, Year: 2004
Day: 25, Month: Aug, Year: 2002
Day: 13, Month: Aug, Year: 2016
[/output]
[/test]
[test]
[input]
1/Jan-1951 06-Jun-2021 21/Aug/2003 07/May/2008
[/input]
[output]
Day: 06, Month: Jun, Year: 2021
Day: 21, Month: Aug, Year: 2003
Day: 07, Month: May, Year: 2008
[/output]
[/test]
[test]
[input]
1/Jan-1951 02.Sep.2014 13/Aug/2024 01.Sep.2001 02.Sep.2022 07/Feb/2008
[/input]
[output]
Day: 02, Month: Sep, Year: 2014
Day: 13, Month: Aug, Year: 2024
Day: 01, Month: Sep, Year: 2001
Day: 02, Month: Sep, Year: 2022
Day: 07, Month: Feb, Year: 2008
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Match Dates
[code-task title="Problem: Match Dates" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
import re

pattern = "\\b(?P<day>\\d{2})([-.\\/])(?P<month>[A-Z][a-z]{2})\\2(?P<year>\\d{4})\\b"

text = input()
matches = re.finditer(pattern, text)

for match in matches:
    print(f"Day: {match.group('day')}, Month: {match.group('month')}, Year: {match.group('year')}")
```
[/code-editor]
[task-description]
## Description
Write a program, which matches a date in the format `dd{separator}MMM{separator}yyyy`.

Use capturing groups in your regular expression.

## Examples
| **Input** | **Output** |
| --- | --- |
| **13/Jul/1928**, **10-Nov-1934**, , 01/Jan-1951,f **25.Dec.1937** 23/09/1973, 1/Feb/2016 | Day: 13, Month: Jul, Year: 1928 |
|  | Day: 10, Month: Nov, Year: 1934 |
|  | Day: 25, Month: Dec, Year: 1937 |

Every valid date has the following characteristics:
- Always starts with **two digits**, followed by a **separator**
- After that, it has **one uppercase** and **two lowercase** letters e.g. Jan, Mar
- After that, it has a **separator** and **exactly 4 digits**, for the year
- The separator could be either of three things: a period `.`, a hyphen `-` or a forward slash `/`
- The separator needs to be the same for the whole date (e.g. `13.03.2016` **is valid**, 13.03/2016 is NOT).

Use a group backreference to check for this.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
13/Jul/1928, 10-Nov-1934, 01/Jan-1951, 25.Dec.1937, 23/09/1973, 1/Feb/2016
[/input]
[output]
Day: 13, Month: Jul, Year: 1928
Day: 10, Month: Nov, Year: 1934
Day: 25, Month: Dec, Year: 1937
[/output]
[/test]
[test]
[input]
01/Jan-1951 29/Feb/2024 1/Jan-1951 27-Feb-2007 1/Jan-1951 1/Mar/2016 23/october/197
[/input]
[output]
Day: 29, Month: Feb, Year: 2024
Day: 27, Month: Feb, Year: 2007
[/output]
[/test]
[test]
[input]
24.Apr.2003 1/Jan-1951 12/Jan/2024 1/Jan-1951 22.Jan.2014 1/Jan-1951 24-Sep-2014 18-Jan-2012 23/october/197
[/input]
[output]
Day: 24, Month: Apr, Year: 2003
Day: 12, Month: Jan, Year: 2024
Day: 22, Month: Jan, Year: 2014
Day: 24, Month: Sep, Year: 2014
Day: 18, Month: Jan, Year: 2012
[/output]
[/test]
[test]
[input]
1/Jan-1951 23/october/197 11-Dec-2010 18.Jan.2014
[/input]
[output]
Day: 11, Month: Dec, Year: 2010
Day: 18, Month: Jan, Year: 2014
[/output]
[/test]
[test]
[input]
04-Jan-2014 1/Jan-1951 23/october/197 23/october/197 23/Nov/2023 1/Jan-1951 27-Feb-2012 08-Mar-2000 1/Jan-1951
[/input]
[output]
Day: 04, Month: Jan, Year: 2014
Day: 23, Month: Nov, Year: 2023
Day: 27, Month: Feb, Year: 2012
Day: 08, Month: Mar, Year: 2000
[/output]
[/test]
[test]
[input]
22.Nov.2011 09.May.2013 1/Jan-1951 29/Sep/2011 24-Jul-2012 06.Oct.2013
[/input]
[output]
Day: 22, Month: Nov, Year: 2011
Day: 09, Month: May, Year: 2013
Day: 29, Month: Sep, Year: 2011
Day: 24, Month: Jul, Year: 2012
Day: 06, Month: Oct, Year: 2013
[/output]
[/test]
[test]
[input]
02/Apr/2002 1/Jan-1951 21-Feb-2019
[/input]
[output]
Day: 02, Month: Apr, Year: 2002
Day: 21, Month: Feb, Year: 2019
[/output]
[/test]
[test]
[input]
1/Jan-1951 06-Jan-2014 1/Jan-1951 30/Jun/2004 21.Nov.2000 15/Nov/2018 11.Mar.2017 1/Jan-1951
[/input]
[output]
Day: 06, Month: Jan, Year: 2014
Day: 30, Month: Jun, Year: 2004
Day: 21, Month: Nov, Year: 2000
Day: 15, Month: Nov, Year: 2018
Day: 11, Month: Mar, Year: 2017
[/output]
[/test]
[test]
[input]
11/Aug/2005 18/Oct/2021 1/Jan-1951 30.Oct.2004 25/Aug/2002 13-Aug-2016
[/input]
[output]
Day: 11, Month: Aug, Year: 2005
Day: 18, Month: Oct, Year: 2021
Day: 30, Month: Oct, Year: 2004
Day: 25, Month: Aug, Year: 2002
Day: 13, Month: Aug, Year: 2016
[/output]
[/test]
[test]
[input]
1/Jan-1951 06-Jun-2021 21/Aug/2003 07/May/2008
[/input]
[output]
Day: 06, Month: Jun, Year: 2021
Day: 21, Month: Aug, Year: 2003
Day: 07, Month: May, Year: 2008
[/output]
[/test]
[test]
[input]
1/Jan-1951 02.Sep.2014 13/Aug/2024 01.Sep.2001 02.Sep.2022 07/Feb/2008
[/input]
[output]
Day: 02, Month: Sep, Year: 2014
Day: 13, Month: Aug, Year: 2024
Day: 01, Month: Sep, Year: 2001
Day: 02, Month: Sep, Year: 2022
Day: 07, Month: Feb, Year: 2008
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Match Numbers
[code-task title="Problem: Match Numbers" taskId="d85ee291-7ae4-4a14-93b5-ca363738047a" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Wirte your code here
```
[/code-editor]
[task-description]
## Description
Write a program, which finds all integer and **floating-point numbers** in a string.

## Examples
| **Input** | **Output** |
| --- | --- |
| **1** **-1** 1s **123** s-s **-123** 55f **123.456** **-123.456** s-1.1 s2 -1- zs-2 s-3.5 | 1 -1 123 -123 123.456 -123.456 |

A number has the following characteristics:
- Has either **whitespace before** it or the start of the string, match either `^` or what's called a [positive lookbehind](https://www.regular-expressions.info/lookaround.html). 
The entire syntax for the beginning of your RegEx might look something like `(^|(?<=\s))`.
- The **number** might or might not be **negative**, so it might have a hyphen on its left side `-`.
- Consists of **one or more** digits.
- Might or might **not have digits after the decimal point**
- The decimal part, if it exists, consists of a period `.` and **one or more** digits after it. 
Use a capturing group.
- Has either whitespace before it or the end of the string match either `$` or what's called a [positive lookahead](https://www.regular-expressions.info/lookaround.html).
The syntax for the end of the RegEx might look something like `($|(?=\s))`.


[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 -1 1s 123 s-s -123 55f 123.456 -123.456 s-1.1 s2 -1- zs-2 s-3.5
[/input]
[output]
1 -1 123 -123 123.456 -123.456
[/output]
[/test]
[test]
[input]
379.59 -601 2122.2379 2960.63 1ss 3350.9748862829 1677 3351.504803879 -2387 134 -4795 s-1.1
[/input]
[output]
379.59 -601 2122.2379 2960.63 3350.9748862829 1677 3351.504803879 -2387 134 -4795
[/output]
[/test]
[test]
[input]
1ss s-1.1 4951 -3209 -4034 -1650.455834 s-1.1 1644.3 s-1.1 3726.5 3464 s-1.1
[/input]
[output]
4951 -3209 -4034 -1650.455834 1644.3 3726.5 3464
[/output]
[/test]
[test]
[input]
s-1.1 -607 s-1.1 1990.6 -4842.02 -4179 3358.9185 s-1.1 1ss s-1.1 3039.10019
[/input]
[output]
-607 1990.6 -4842.02 -4179 3358.9185 3039.10019
[/output]
[/test]
[test]
[input]
-4033.5 s-1.1 -718 1020 -4391.844 s-1.1 1460.699729 -3672.5666112 -1951.24667353 -3236.76726394 -2099
[/input]
[output]
-4033.5 -718 1020 -4391.844 1460.699729 -3672.5666112 -1951.24667353 -3236.76726394 -2099
[/output]
[/test]
[test]
[input]
1968.33627752 s-1.1 -956.67075 s-1.1 -2804 -1925 337.17 s-1.1 956
[/input]
[output]
1968.33627752 -956.67075 -2804 -1925 337.17 956
[/output]
[/test]
[test]
[input]
s-1.1 -547 -4773 -3507.4461 -2064 -2126
[/input]
[output]
-547 -4773 -3507.4461 -2064 -2126
[/output]
[/test]
[test]
[input]
s-1.1 2557.688 s-1.1 s-1.1 s-1.1 3984 -3203 -107.9807152415 -3733 s-1.1
[/input]
[output]
2557.688 3984 -3203 -107.9807152415 -3733
[/output]
[/test]
[test]
[input]
4670 s-1.1 909.513836428 -415 s-1.1 -3940.4 -983.49263895
[/input]
[output]
4670 909.513836428 -415 -3940.4 -983.49263895
[/output]
[/test]
[test]
[input]
-3078 3181.5451 1642.096 2679 s-1.1 -2285.21904316 s-1.1 -1980 227 -2337
[/input]
[output]
-3078 3181.5451 1642.096 2679 -2285.21904316 -1980 227 -2337
[/output]
[/test]
[test]
[input]
-4250.14 -3770 4919.414315975 s-1.1 s-1.1 -4643.61647 s-1.1 s-1.1 2930.1 -2246.4431545258 3018.867594 4036.59612 s-1.1
[/input]
[output]
-4250.14 -3770 4919.414315975 -4643.61647 2930.1 -2246.4431545258 3018.867594 4036.59612
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Match Numbers
[code-task title="Problem: Match Numbers" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
import re

pattern = r'(^|(?<=\s))-\d+\.*\d*($|(?=\s))|(^|(?<=\s))\d+\.*\d*($|(?=\s))'

text = input()

result = re.finditer(pattern, text)
res = ''
for item in result:
    res += item.group(0) + ' '
    
print(res.strip(' '))
```
[/code-editor]
[task-description]
## Description
Write a program, which finds all integer and **floating-point numbers** in a string.

## Examples
| **Input** | **Output** |
| --- | --- |
| **1** **-1** 1s **123** s-s **-123** 55f **123.456** **-123.456** s-1.1 s2 -1- zs-2 s-3.5 | 1 -1 123 -123 123.456 -123.456 |

A number has the following characteristics:
- Has either **whitespace before** it or the start of the string, match either `^` or what's called a [positive lookbehind](https://www.regular-expressions.info/lookaround.html). 
The entire syntax for the beginning of your RegEx might look something like `(^|(?<=\s))`.
- The **number** might or might not be **negative**, so it might have a hyphen on its left side `-`.
- Consists of **one or more** digits.
- Might or might **not have digits after the decimal point**
- The decimal part, if it exists, consists of a period `.` and **one or more** digits after it. 
Use a capturing group.
- Has either whitespace before it or the end of the string match either `$` or what's called a [positive lookahead](https://www.regular-expressions.info/lookaround.html).
The syntax for the end of the RegEx might look something like `($|(?=\s))`.


[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 -1 1s 123 s-s -123 55f 123.456 -123.456 s-1.1 s2 -1- zs-2 s-3.5
[/input]
[output]
1 -1 123 -123 123.456 -123.456
[/output]
[/test]
[test]
[input]
379.59 -601 2122.2379 2960.63 1ss 3350.9748862829 1677 3351.504803879 -2387 134 -4795 s-1.1
[/input]
[output]
379.59 -601 2122.2379 2960.63 3350.9748862829 1677 3351.504803879 -2387 134 -4795
[/output]
[/test]
[test]
[input]
1ss s-1.1 4951 -3209 -4034 -1650.455834 s-1.1 1644.3 s-1.1 3726.5 3464 s-1.1
[/input]
[output]
4951 -3209 -4034 -1650.455834 1644.3 3726.5 3464
[/output]
[/test]
[test]
[input]
s-1.1 -607 s-1.1 1990.6 -4842.02 -4179 3358.9185 s-1.1 1ss s-1.1 3039.10019
[/input]
[output]
-607 1990.6 -4842.02 -4179 3358.9185 3039.10019
[/output]
[/test]
[test]
[input]
-4033.5 s-1.1 -718 1020 -4391.844 s-1.1 1460.699729 -3672.5666112 -1951.24667353 -3236.76726394 -2099
[/input]
[output]
-4033.5 -718 1020 -4391.844 1460.699729 -3672.5666112 -1951.24667353 -3236.76726394 -2099
[/output]
[/test]
[test]
[input]
1968.33627752 s-1.1 -956.67075 s-1.1 -2804 -1925 337.17 s-1.1 956
[/input]
[output]
1968.33627752 -956.67075 -2804 -1925 337.17 956
[/output]
[/test]
[test]
[input]
s-1.1 -547 -4773 -3507.4461 -2064 -2126
[/input]
[output]
-547 -4773 -3507.4461 -2064 -2126
[/output]
[/test]
[test]
[input]
s-1.1 2557.688 s-1.1 s-1.1 s-1.1 3984 -3203 -107.9807152415 -3733 s-1.1
[/input]
[output]
2557.688 3984 -3203 -107.9807152415 -3733
[/output]
[/test]
[test]
[input]
4670 s-1.1 909.513836428 -415 s-1.1 -3940.4 -983.49263895
[/input]
[output]
4670 909.513836428 -415 -3940.4 -983.49263895
[/output]
[/test]
[test]
[input]
-3078 3181.5451 1642.096 2679 s-1.1 -2285.21904316 s-1.1 -1980 227 -2337
[/input]
[output]
-3078 3181.5451 1642.096 2679 -2285.21904316 -1980 227 -2337
[/output]
[/test]
[test]
[input]
-4250.14 -3770 4919.414315975 s-1.1 s-1.1 -4643.61647 s-1.1 s-1.1 2930.1 -2246.4431545258 3018.867594 4036.59612 s-1.1
[/input]
[output]
-4250.14 -3770 4919.414315975 -4643.61647 2930.1 -2246.4431545258 3018.867594 4036.59612
[/output]
[/test]
[/tests]
[/code-task]
[/slide]