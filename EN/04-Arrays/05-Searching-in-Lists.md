# Searching in Lists

[slide]
# Video

[vimeo-video startTimeInSeconds="6497" endTimeInSeconds="6945"]
[stream language="EN" videoId="425042764" default /]
[stream language="RO" videoId="425050167" /]
[/video-vimeo]

[/slide]

[slide]
# In Keyword

With the `in` keyword you can check **if an element is in a list**.

This is usually used with `if-else` statements.

```python live
my_list = [1, 2, 3, 4]
if 3 in my_list:
   print("The number 3 is in the list")
```

# Not in keywords

Combining the `in` keyword with the `not` one gives you the possibility to check if an element is **not** in a list.

Also usually used with `if-else` statements.

```python live
my_list = [1, 2, 3, 4]
if 5 not in my_list:
   print("The number 5 is not in the list")
```
[/slide]

[slide hideTitle]
# Problem: Search
[code-task title="Search" taskId="python-fund-07-Arrays-problem-7" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive a number **n** and a **word**.

On the next **n lines** you will be given some **strings**.

You have to **add** them in a list and **print** them.

After that you have to **filter** out only the **strings that include the given word** and **print** that list also.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | ['I study at SoftUni', 'I walk to work', 'I learn Python at SoftUni'] |
| SoftUni | ['I study at SoftUni', 'I learn Python at SoftUni'] |
| I study at SoftUni |  |
| I walk to work |  |
| I learn Python at SoftUni |  |

| **Input** | **Output** |
| --- | --- |
| 4 | ['I love tomatoes', 'I can eat tomatoes forever', "I don't like apples", 'Yesterday I ate two tomatoes'] |
| tomatoes | ['I love tomatoes', 'I can eat tomatoes forever', 'Yesterday I ate two tomatoes'] |
| I love tomatoes |  |
| I can eat tomatoes forever |  |
| I don't like apples |  |
| Yesterday I ate two tomatoes |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
SoftUni
I study at SoftUni
I walk to work
I learn Python at SoftUni
[/input]
[output]
\['I study at SoftUni', 'I walk to work', 'I learn Python at SoftUni'\]
\['I study at SoftUni', 'I learn Python at SoftUni'\]
[/output]
[/test]
[test open]
[input]
4
tomatoes
I love tomatoes
I can eat tomatoes forever
I don't like apples
Yesterday I ate two tomatoes
[/input]
[output]
\['I love tomatoes', 'I can eat tomatoes forever', "I don't like apples", 'Yesterday I ate two tomatoes'\]
\['I love tomatoes', 'I can eat tomatoes forever', 'Yesterday I ate two tomatoes'\]
[/output]
[/test]
[test]
[input]
5
code
i love to code
i love to drink
i can drink
i can code
code is life
[/input]
[output]
\['i love to code', 'i love to drink', 'i can drink', 'i can code', 'code is life'\]
\['i love to code', 'i can code', 'code is life'\]
[/output]
[/test]
[test]
[input]
3
eat
i love to drink cola
cola is life
cola is hapiness
[/input]
[output]
\['i love to drink cola', 'cola is life', 'cola is hapiness'\]
\[\]
[/output]
[/test]
[test]
[input]
4
i
i can fly
i belive i can fly
hey, i want to fly
i love flying
[/input]
[output]
\['i can fly', 'i belive i can fly', 'hey, i want to fly', 'i love flying'\]
\['i can fly', 'i belive i can fly', 'hey, i want to fly', 'i love flying'\]
[/output]
[/test]
[test]
[input]
0
bye
[/input]
[output]
\[\]
\[\]
[/output]
[/test]
[test]
[input]
2
some
some text
some stuff
[/input]
[output]
\['some text', 'some stuff'\]
\['some text', 'some stuff'\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Search
[code-task title="Search" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
n = int(input())
word = input()
strings = []
for i in range(n):
    current_string = input()
    strings.append(current_string)
print(strings)
for i in range(len(strings) - 1, -1, -1):
    element = strings[i]
    if word not in element:
        strings.remove(element)
print(strings)
```
[/code-editor]
[task-description]
## Description
You will receive a number **n** and a **word**.

On the next **n lines** you will be given some **strings**.

You have to **add** them in a list and **print** them.

After that you have to **filter** out only the **strings that include the given word** and **print** that list also.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | ['I study at SoftUni', 'I walk to work', 'I learn Python at SoftUni'] |
| SoftUni | ['I study at SoftUni', 'I learn Python at SoftUni'] |
| I study at SoftUni |  |
| I walk to work |  |
| I learn Python at SoftUni |  |

| **Input** | **Output** |
| --- | --- |
| 4 | ['I love tomatoes', 'I can eat tomatoes forever', "I don't like apples", 'Yesterday I ate two tomatoes'] |
| tomatoes | ['I love tomatoes', 'I can eat tomatoes forever', 'Yesterday I ate two tomatoes'] |
| I love tomatoes |  |
| I can eat tomatoes forever |  |
| I don't like apples |  |
| Yesterday I ate two tomatoes |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
SoftUni
I study at SoftUni
I walk to work
I learn Python at SoftUni
[/input]
[output]
\['I study at SoftUni', 'I walk to work', 'I learn Python at SoftUni'\]
\['I study at SoftUni', 'I learn Python at SoftUni'\]
[/output]
[/test]
[test open]
[input]
4
tomatoes
I love tomatoes
I can eat tomatoes forever
I don't like apples
Yesterday I ate two tomatoes
[/input]
[output]
\['I love tomatoes', 'I can eat tomatoes forever', "I don't like apples", 'Yesterday I ate two tomatoes'\]
\['I love tomatoes', 'I can eat tomatoes forever', 'Yesterday I ate two tomatoes'\]
[/output]
[/test]
[test]
[input]
5
code
i love to code
i love to drink
i can drink
i can code
code is life
[/input]
[output]
\['i love to code', 'i love to drink', 'i can drink', 'i can code', 'code is life'\]
\['i love to code', 'i can code', 'code is life'\]
[/output]
[/test]
[test]
[input]
3
eat
i love to drink cola
cola is life
cola is hapiness
[/input]
[output]
\['i love to drink cola', 'cola is life', 'cola is hapiness'\]
\[\]
[/output]
[/test]
[test]
[input]
4
i
i can fly
i belive i can fly
hey, i want to fly
i love flying
[/input]
[output]
\['i can fly', 'i belive i can fly', 'hey, i want to fly', 'i love flying'\]
\['i can fly', 'i belive i can fly', 'hey, i want to fly', 'i love flying'\]
[/output]
[/test]
[test]
[input]
0
bye
[/input]
[output]
\[\]
\[\]
[/output]
[/test]
[test]
[input]
2
some
some text
some stuff
[/input]
[output]
\['some text', 'some stuff'\]
\['some text', 'some stuff'\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Numbers Filter
[code-task title="Numbers Filter" taskId="python-fund-07-Arrays-problem-9" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive a single number **n**.

On the next **n lines** you will receive **integers**.

After that you will be given one of the following **commands**:

 - **even**
 - **odd**
 - **negative**
 - **positive**

**Filter** all the numbers that **fit in the category** (0 counts as a positive). Finally, **print** the result.

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 | [19, -2, 18, 998] |
| 33 |  |
| 19 |  |
| -2 |  |
| 18 |  |
| 998 |  |
| even |  |

| **Input** | **Output** |
| --- | --- |
| 3 | [-4] |
| 111 |  |
| -4 |  |
| 0 |  |
| negative |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
33
19
-2
18
998
even
[/input]
[output]
\[-2, 18, 998\]
[/output]
[/test]
[test open]
[input]
3
111
-4
0
negative
[/input]
[output]
\[-4\]
[/output]
[/test]
[test]
[input]
5
10
20
30
21
27
even
[/input]
[output]
\[10, 20, 30\]
[/output]
[/test]
[test]
[input]
6
10
20
30
40
50
65
odd
[/input]
[output]
\[65\]
[/output]
[/test]
[test]
[input]
10
-14
65
91
-66
-43
15
69
91
97
82
negative
[/input]
[output]
\[-14, -66, -43\]
[/output]
[/test]
[test]
[input]
4
-1
5
85
0
positive
[/input]
[output]
\[5, 85, 0\]
[/output]
[/test]
[test]
[input]
3
0
0
0
positive
[/input]
[output]
\[0, 0, 0\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Video: Numbers Filter

[vimeo-video startTimeInSeconds="7912" endTimeInSeconds="8879"]
[stream language="EN" videoId="425042764" default /]
[stream language="RO" videoId="425050167" /]
[/video-vimeo]

[/slide]

[slide hideTitle]
# Solution: Numbers Filter
[code-task title="Numbers Filter" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
n = int(input())
numbers = []
filtered = []
for i in range(n):
    current_number = int(input())
    numbers.append(current_number)
command = input()
if command == "even":
    for number in numbers:
        if number % 2 == 0:
            filtered.append(number)
elif command == "odd":
    for number in numbers:
        if number % 2 != 0:
            filtered.append(number)
elif command == "negative":
    for number in numbers:
        if number < 0:
            filtered.append(number)
elif command == "positive":
    for number in numbers:
        if number >= 0:
            filtered.append(number)
print(filtered)
```
[/code-editor]
[task-description]
## Description
You will receive a single number **n**.

On the next **n lines** you will receive **integers**.

After that you will be given one of the following **commands**:

 - **even**
 - **odd**
 - **negative**
 - **positive**

**Filter** all the numbers that **fit in the category** (0 counts as a positive). Finally, **print** the result.

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 | [19, -2, 18, 998] |
| 33 |  |
| 19 |  |
| -2 |  |
| 18 |  |
| 998 |  |
| even |  |

| **Input** | **Output** |
| --- | --- |
| 3 | [-4] |
| 111 |  |
| -4 |  |
| 0 |  |
| negative |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
33
19
-2
18
998
even
[/input]
[output]
\[-2, 18, 998\]
[/output]
[/test]
[test open]
[input]
3
111
-4
0
negative
[/input]
[output]
\[-4\]
[/output]
[/test]
[test]
[input]
5
10
20
30
21
27
even
[/input]
[output]
\[10, 20, 30\]
[/output]
[/test]
[test]
[input]
6
10
20
30
40
50
65
odd
[/input]
[output]
\[65\]
[/output]
[/test]
[test]
[input]
10
-14
65
91
-66
-43
15
69
91
97
82
negative
[/input]
[output]
\[-14, -66, -43\]
[/output]
[/test]
[test]
[input]
4
-1
5
85
0
positive
[/input]
[output]
\[5, 85, 0\]
[/output]
[/test]
[test]
[input]
3
0
0
0
positive
[/input]
[output]
\[0, 0, 0\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Index of Element

The `index(element)` function is used to find at **which index an element is located**.

```python live
my_list = [1, 2, 3, 4]
print(my_list.index(2)) # 1
```

If there is **no such element** in the list, an `ValueError` will be raised.

```python live
my_list = [1, 2, 3, 4]
print(my_list.index(7)) # ValueError
```

[/slide]

[slide]
# Element Occurences

The `count(element)` function is used to get the **number of occurences of an element**.

```python live
my_list = [1, 2, 3, 4, 4, 4]
print(my_list.count(4)) # 3
print(my_list.count(7)) # 0
```

[/slide]
