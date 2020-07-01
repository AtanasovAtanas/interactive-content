# Sorting
[slide]
# Video

[vimeo-video startTimeInSeconds="6102" endTimeInSeconds="8606"]
[stream language="EN" videoId="421723151" default /]
[stream language="RO" videoId="432059499"  /]
[/video-vimeo]

[/slide]
[slide]
# sorted()

The `sorted()` method **sorts the elements** of a **given iterable** in **ascending** or **descending** order.

The syntax of the method is `sorted(iterable, [key], [reverse])`:
 - `iterable` - **sequence**, **collection** or **any iterator**; **required**
 - `key` - **function** that serves as a key for the **sort comparison**; **optional**
 - `reverse` - if **true**, the sorted collection is **reversed** (in **descending** order); **optional**

It **returns** a **sorted list** of the **given iterable object**.

By **default** the `sorted()` method **sorts** in **ascending** order.

**Strings** are sorted **alphabetically**.

**Numbers** are sorted **numerically**.

**Note:** A list that contains **both strings** and **numbers cannot** be **sorted**.

Sorting numbers example:

```python live
numbers = [2, 5, 7, 1, -8, 0]
sorted_numbers = sorted(numbers)
descending_sorted_numbers = sorted(numbers, reverse=True)

print(numbers) # [2, 5, 7, 1, -8, 0]
print(sorted_numbers) # [-8, 0, 1, 2, 5, 7]
print(descending_sorted_numbers) # [7, 5, 2, 1, 0, -8]
```

Sorting strings example:

```python live
names = ["Eric", "Alice", "Peter", "Zed"]
sorted_names = sorted(names)
descending_sorted_names = sorted(names, reverse=True)

print(names) # ['Eric', 'Alice', 'Peter', 'Zed']
print(sorted_names) # ['Alice', 'Eric', 'Peter', 'Zed']
print(descending_sorted_names) # ['Zed', 'Peter', 'Eric', 'Alice']
```

[/slide]

[slide]
# Using Lambda Functions

**Lambda functions** can be used in the `sorted()` method.

The `key` parameter is the one that **accepts** the **lambda function**.

Passing a **lambda function** allows you to **sort** the elements in a **custom way**.

Example:

```python live
people_ages = {'Annie': 21, 'George': 18, 'John': 45}
sorted_by_name = dict(sorted(people_ages.items(), key=lambda x: x[0]))
sorted_by_age = dict(sorted(people_ages.items(), key=lambda x: x[1]))

print(sorted_by_name) # {'Annie': 21, 'George': 18, 'John': 45}
print(sorted_by_age) # {'George': 18, 'Annie': 21, 'John': 45}
```

In the example above, there is a dictionary that consists of **names** of people (**keys**) and their **age** (**values**).

The **lambda function** tells the `sorted()` method to sort the dictionary by **index**.

The `x[0]` means to sort the dictionary by **keys** (because **keys** are **first**, they are at **index 0**).

The `x[1]` means to sort the dictionary by **values** (because **values** are **second**, they are at **index 1**).

Another more complex example:

```python live
class Person:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

people = [Person("Xin", "Chang", 17),
          Person("Nicholas", "Grey", 24),
          Person("Amy", "Willson", 20)]

people = sorted(people, key=lambda x: x.first_name)

for person in people:
    print(f"{person.first_name} {person.last_name} is {person.age} years old.")
```

In this one, there is a **class** `Person` and **list of objects** of it.

The sort there is by `Person`'s `first_name`.

Probably you can already guess that it can be sorted by `last_name` and `age`.

**Note:** If you **don't specify** how a **list of custom objects** to be sorted, the `sorted()` method **raises an error**.

```python live
class Person:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

people = [Person("Xin", "Chang", 17),
          Person("Nicholas", "Grey", 24),
          Person("Amy", "Willson", 20)]

people = sorted(people)

for person in people:
    print(f"{person.first_name} {person.last_name} is {person.age} years old.")
```

[/slide]

[slide hideTitle]
# Problem: Odd Occurrences
[code-task title="Odd Occurrences" taskId="python-fundamentals-Associative-Arrays-04" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that extracts all elements from a given sequence of words that are present in it an **odd number of times** (case-insensitive).

 - Words are given on a single line, space separated.
 - Print the result elements in lowercase, in their order of appearance.

## Examples
| **Input** | **Output** |
| --- | --- |
| Java C# PHP PHP JAVA C java | java c# c |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 3 5 5 hi pi HO Hi 5 ho 3 hi pi | 5 hi |
|  |  |

| **Input** | **Output** |
| --- | --- |
| a a A SQL xx a xx a A a XX c | a sql xx c |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Java C\# PHP PHP JAVA C java
[/input]
[output]
java c\# c
[/output]
[/test]
[test]
[input]
3 5 5 hi pi HO Hi 5 ho 3 hi pi
[/input]
[output]
5 hi
[/output]
[/test]
[test]
[input]
a a A SQL xx a xx a A a XX c
[/input]
[output]
a sql xx c
[/output]
[/test]
[test]
[input]
as AS b BB HHH H SAD bbb asbsad sadjsdadshhds dh sdaghdghhsa h hsaj sad as dH H HH BBb
[/input]
[output]
as b bb hhh h asbsad sadjsdadshhds sdaghdghhsa hsaj hh
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Odd Occurrences
[code-task title="Odd Occurrences" taskId="2d929508-98bd-4d91-a079-ca4e2808c8bd" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
words = input().split(" ")

dictionary = {}

for word in words:
    word_lower = word.lower()

    if word_lower not in dictionary:
        dictionary[word_lower] = 0

    dictionary[word_lower] += 1

for (key, value) in dictionary.items():
    if value % 2 != 0:
        print(key, end=" ")
```
[/code-editor]
[task-description]
## Description
Write a program that extracts all elements from a given sequence of words that are present in it an **odd number of times** (case-insensitive).

 - Words are given on a single line, space separated.
 - Print the result elements in lowercase, in their order of appearance.

## Examples
| **Input** | **Output** |
| --- | --- |
| Java C# PHP PHP JAVA C java | java c# c |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 3 5 5 hi pi HO Hi 5 ho 3 hi pi | 5 hi |
|  |  |

| **Input** | **Output** |
| --- | --- |
| a a A SQL xx a xx a A a XX c | a sql xx c |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Java C\# PHP PHP JAVA C java
[/input]
[output]
java c\# c
[/output]
[/test]
[test]
[input]
3 5 5 hi pi HO Hi 5 ho 3 hi pi
[/input]
[output]
5 hi
[/output]
[/test]
[test]
[input]
a a A SQL xx a xx a A a XX c
[/input]
[output]
a sql xx c
[/output]
[/test]
[test]
[input]
as AS b BB HHH H SAD bbb asbsad sadjsdadshhds dh sdaghdghhsa h hsaj sad as dH H HH BBb
[/input]
[output]
as b bb hhh h asbsad sadjsdadshhds sdaghdghhsa hsaj hh
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Word Synonyms
[code-task title="Word Synonyms" taskId="python-fundamentals-Associative-Arrays-05" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program, which keeps a dictionary with synonyms.

The **key** of the dictionary will be the **word**.

The **value** will be a **list of all the synonyms of that word**.

You will be given a number **n – the count of the words**.

After each word, you will be given a synonym, so the count of lines you have to read from the console is **2 * n**.

**You will be receiving a word** and a **synonym** each on a separate line like this:

 - {**word**}
 - {**synonym**}

If you get the same word twice, just add the new synonym to the list.

Print the words in the following format:

"**{word} - {synonym1, synonym2… synonymN}**"

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | cute - adorable, charming |
| cute | smart - clever |
| adorable |  |
| cute |  |
| charming |  |
| smart |  |
| clever |  |

| **Input** | **Output** |
| --- | --- |
| 2 | task – problem, assignment |
| task |  |
| problem |  |
| task |  |
| assignment |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
cute
adorable
cute
charming
smart
clever
[/input]
[output]
cute - adorable, charming
smart - clever
[/output]
[/test]
[test open]
[input]
2
task
problem
task
assignment
[/input]
[output]
task - problem, assignment
[/output]
[/test]
[test]
[input]
4
fashion
trend
fashion
model
fashion
look
cute
adorable
[/input]
[output]
fashion - trend, model, look
cute - adorable
[/output]
[/test]
[test]
[input]
7
fashion
trend
fashion
model
fashion
look
elegant
grand
elegant
fancy
elegant
classic
cute
adorable
[/input]
[output]
fashion - trend, model, look
elegant - grand, fancy, classic
cute - adorable
[/output]
[/test]
[test]
[input]
9
addicted
obsessed
addicted
hooked
addicted
attached
fashion
model
fashion
look
elegant
grand
elegant
fancy
elegant
classic
cute
adorable
[/input]
[output]
addicted - obsessed, hooked, attached
fashion - model, look
elegant - grand, fancy, classic
cute - adorable
[/output]
[/test]
[test]
[input]
8
fat
big
feedback
assessment
fat
plump
develop
advance
develop
establish
feedback
comment
feedback
criticism
fat
bulky
[/input]
[output]
fat - big, plump, bulky
feedback - assessment, comment, criticism
develop - advance, establish
[/output]
[/test]
[test]
[input]
8
condition
action
condition
case
condition
position
greet
accost
hello
greetings
hell
inferno
customer
client
customer
purchaser
[/input]
[output]
condition - action, case, position
greet - accost
hello - greetings
hell - inferno
customer - client, purchaser
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Word Synonyms
[code-task title="Word Synonyms" taskId="8e88ace6-1c47-43e9-9e0e-7c2b741517f6" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
n = int(input())
synonyms = {}
for i in range(n):
    word = input()
    synonym = input()
    if word not in synonyms:
        synonyms[word] = []
    synonyms[word].append(synonym)
for word in synonyms:
    print(f"{word} - {', '.join(synonyms[word])}")
```
[/code-editor]
[task-description]
## Description
Write a program, which keeps a dictionary with synonyms.

The **key** of the dictionary will be the **word**.

The **value** will be a **list of all the synonyms of that word**.

You will be given a number **n – the count of the words**.

After each word, you will be given a synonym, so the count of lines you have to read from the console is **2 * n**.

**You will be receiving a word** and a **synonym** each on a separate line like this:

 - {**word**}
 - {**synonym**}

If you get the same word twice, just add the new synonym to the list.

Print the words in the following format:

"**{word} - {synonym1, synonym2… synonymN}**"

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | cute - adorable, charming |
| cute | smart - clever |
| adorable |  |
| cute |  |
| charming |  |
| smart |  |
| clever |  |

| **Input** | **Output** |
| --- | --- |
| 2 | task – problem, assignment |
| task |  |
| problem |  |
| task |  |
| assignment |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
cute
adorable
cute
charming
smart
clever
[/input]
[output]
cute - adorable, charming
smart - clever
[/output]
[/test]
[test open]
[input]
2
task
problem
task
assignment
[/input]
[output]
task - problem, assignment
[/output]
[/test]
[test]
[input]
4
fashion
trend
fashion
model
fashion
look
cute
adorable
[/input]
[output]
fashion - trend, model, look
cute - adorable
[/output]
[/test]
[test]
[input]
7
fashion
trend
fashion
model
fashion
look
elegant
grand
elegant
fancy
elegant
classic
cute
adorable
[/input]
[output]
fashion - trend, model, look
elegant - grand, fancy, classic
cute - adorable
[/output]
[/test]
[test]
[input]
9
addicted
obsessed
addicted
hooked
addicted
attached
fashion
model
fashion
look
elegant
grand
elegant
fancy
elegant
classic
cute
adorable
[/input]
[output]
addicted - obsessed, hooked, attached
fashion - model, look
elegant - grand, fancy, classic
cute - adorable
[/output]
[/test]
[test]
[input]
8
fat
big
feedback
assessment
fat
plump
develop
advance
develop
establish
feedback
comment
feedback
criticism
fat
bulky
[/input]
[output]
fat - big, plump, bulky
feedback - assessment, comment, criticism
develop - advance, establish
[/output]
[/test]
[test]
[input]
8
condition
action
condition
case
condition
position
greet
accost
hello
greetings
hell
inferno
customer
client
customer
purchaser
[/input]
[output]
condition - action, case, position
greet - accost
hello - greetings
hell - inferno
customer - client, purchaser
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
