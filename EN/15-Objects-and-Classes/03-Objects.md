# Objects
[slide]
# Video

[vimeo-video startTimeInSeconds="4344" endTimeInSeconds="5050"]
[stream language="EN" videoId="421734086" default /]
[stream language="RO" videoId="433520198" /]
[/video-vimeo]

[/slide]
[slide]
# Definition

An **instance** (object) is a copy of the class with **actual** values.

Objects encapsulate variables and methods **into a single entity**.

This is where we use the classes. Objects' **variables and methods are copied from the class**.

For example we know the characteristics of book - it has covers, content, number of pages, genre, etc. This is like a **class Book**.

But all books have different values of the above. Now this is like an **instance** of the **class Book**.

[image assetsSrc="books-example-picture.png" /]

[/slide]

[slide]
# Object Initialization

Now that we know how to create a class, we can make use of it.

To do that, the `__init__()` method is used, **giving it parameters** if needed.

Just like normal functions, if a parameter is **optional**, we **don't** need to **pass** it when calling the function.

To **initialize** an object of the class, type the **class name** and pass the **parameters** in the **braces** after it:

```python
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
cat_two = Cat('Purr')
```

[/slide]

[slide]
# Accessing Attributes

In order to access an attribute of the object directly, type the **variable name** plus **dot** ( `.` ) and the **attribute name**.

For better understanding, look at the example below, specifically where the **attributes are printed**:

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
cat_two = Cat('Purr')

print(cat_one.name)
print(cat_one.age)
print(cat_two.name)
print(cat_two.age)
```

[/slide]

[slide]
# Modifying Attributes

You can change the values of the attributes of an object after it's been initialized.

To do that, you have to access it and then give it a value, with the `=` operator.

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
print(cat_one.name)
cat_one.name = 'Shady'
print(cat_one.name)
```

[/slide]

[slide hideTitle]
# Problem: Party
[code-task title="Party" taskId="python-fund-16-Objects-and-Classes-problem-1" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Create a class **Party** that only has an attribute called **people**.

The \_\_init\_\_ method should **not accept** any **parameters**.

You will be given **names** of people (on separate lines) until you receive the command "**End**".

Use the created class to solve this problem.

After you receive the end command print **2 lines**:

 - "Going: \{people\}" - the people should be separated by comma and space ", "
 - "Total: \{total_people_going\}"

**Note:** Submit all of your code including the class.

## Examples
| **Input** | **Output** |
| --- | --- |
| ter | Going: Peter, John, Katy |
| John | Total: 3 |
| Katy |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter
John
Katy
End
[/input]
[output]
Going: Peter, John, Katy
Total: 3
[/output]
[/test]
[test]
[input]
a
b
c
d
End
[/input]
[output]
Going: a, b, c, d
Total: 4
[/output]
[/test]
[test]
[input]
End
[/input]
[output]
Going:
Total: 0
[/output]
[/test]
[test]
[input]
w
t
e
y
u
h
n
End
[/input]
[output]
Going: w, t, e, y, u, h, n
Total: 7
[/output]
[/test]
[test]
[input]
abc
def
End
[/input]
[output]
Going: abc, def
Total: 2
[/output]
[/test]
[test]
[input]
alabala
portokala
mortokala
End
[/input]
[output]
Going: alabala, portokala, mortokala
Total: 3
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Party
[code-task title="Party" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
class Party:
    def __init__(self):
        self.people = []

line = input()
party = Party()

while line != "End":
    party.people.append(line)
    line = input()

print(f"Going: {', '.join(party.people)}")
print(f"Total: {len(party.people)}")
```
[/code-editor]
[task-description]
## Description
Create a class **Party** that only has an attribute called **people**.

The \_\_init\_\_ method should **not accept** any **parameters**.

You will be given **names** of people (on separate lines) until you receive the command "**End**".

Use the created class to solve this problem.

After you receive the end command print **2 lines**:

 - "Going: \{people\}" - the people should be separated by comma and space ", "
 - "Total: \{total_people_going\}"

**Note:** Submit all of your code including the class.

## Examples
| **Input** | **Output** |
| --- | --- |
| ter | Going: Peter, John, Katy |
| John | Total: 3 |
| Katy |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter
John
Katy
End
[/input]
[output]
Going: Peter, John, Katy
Total: 3
[/output]
[/test]
[test]
[input]
a
b
c
d
End
[/input]
[output]
Going: a, b, c, d
Total: 4
[/output]
[/test]
[test]
[input]
End
[/input]
[output]
Going:
Total: 0
[/output]
[/test]
[test]
[input]
w
t
e
y
u
h
n
End
[/input]
[output]
Going: w, t, e, y, u, h, n
Total: 7
[/output]
[/test]
[test]
[input]
abc
def
End
[/input]
[output]
Going: abc, def
Total: 2
[/output]
[/test]
[test]
[input]
alabala
portokala
mortokala
End
[/input]
[output]
Going: alabala, portokala, mortokala
Total: 3
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
