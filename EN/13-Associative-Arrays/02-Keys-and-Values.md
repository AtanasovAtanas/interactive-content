# Keys and Values

[slide]
# Key Definition

While **list** uses **indexing** to access values, **dictionary** uses **keys**.

A **key** can be used either **inside square brackets** or with the `get()` method.

```python live
my_dict = {'cat': 'meow'}

print(my_dict['cat'])
print((my_dict.get('cat')))
```

**Note:** The difference when using `get()` is that it returns `None` instead of raising `KeyError` if the key is not found.

```python live
my_dict = {'cat': 'meow'}

print((my_dict.get('dog')))
```

```python live
my_dict = {'cat': 'meow'}

print(my_dict['dog'])
```

[/slide]

[slide]
# Values

Dictionaries are **mutable**.

Using the **assignment operator** ( `=` ) **new pairs can be added** or the **value of already existing** can be **changed**.

If the **key** is **already present**, the **value** gets **updated**, **otherwise** a **new pair is added** to the dictionary.

Adding a new pair:

```python live
my_dict = {"name": "Jason", "age": 20}
my_dict["job"] = "Software developer"
print(my_dict["job"])
```

Updating value:

```python live
my_dict = {"name": "Jason", "age": 20}
my_dict["age"] = 22
print(my_dict["age"])
```

[/slide]

[slide hideTitle]
# Problem: Bakery
[code-task title="Bakery" taskId="python-fundamentals-Associative-Arrays-01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive a single line containing some **food** (keys) and **quantities** (values).

They will be separated by a **single space** (the **first** element is the **key**, the **second** – the **value** and so on).

Create a **dictionary** with all the keys and values and **print** it on the console.

## Examples
| **Input** | **Output** |
| --- | --- |
| bread 10 butter 4 sugar 9 jam 12 | {'bread': 10, 'butter': 4, 'sugar': 9, 'jam': 12} |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
bread 10 butter 4 sugar 9 jam 12
[/input]
[output]
\{'bread': 10, 'butter': 4, 'sugar': 9, 'jam': 12\}
[/output]
[/test]
[test]
[input]
a 4 b 10 d 5
[/input]
[output]
\{'a': 4, 'b': 10, 'd': 5\}
[/output]
[/test]
[test]
[input]
n 33 i 9 j 80 y 6 u 8
[/input]
[output]
\{'n': 33, 'i': 9, 'j': 80, 'y': 6, 'u': 8\}
[/output]
[/test]
[test]
[input]
k 0 u 1 y 3
[/input]
[output]
\{'k': 0, 'u': 1, 'y': 3\}
[/output]
[/test]
[test]
[input]
k 1 k 2 k 3
[/input]
[output]
\{'k': 3\}
[/output]
[/test]
[test]
[input]
l 10 l 20 h 8 h 10
[/input]
[output]
\{'l': 20, 'h': 10\}
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Bakery
[code-task title="Bakery" taskId="38676d82-8e14-48a5-9994-2be4004c212f" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
elements = input().split(" ")
bakery = {}  # bakery = dict()
for i in range(0, len(elements), 2):
    key = elements[i]
    value = elements[i + 1]
    bakery[key] = int(value)
print(bakery)
```
[/code-editor]
[task-description]
## Description
You will receive a single line containing some **food** (keys) and **quantities** (values).

They will be separated by a **single space** (the **first** element is the **key**, the **second** – the **value** and so on).

Create a **dictionary** with all the keys and values and **print** it on the console.

## Examples
| **Input** | **Output** |
| --- | --- |
| bread 10 butter 4 sugar 9 jam 12 | {'bread': 10, 'butter': 4, 'sugar': 9, 'jam': 12} |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
bread 10 butter 4 sugar 9 jam 12
[/input]
[output]
\{'bread': 10, 'butter': 4, 'sugar': 9, 'jam': 12\}
[/output]
[/test]
[test]
[input]
a 4 b 10 d 5
[/input]
[output]
\{'a': 4, 'b': 10, 'd': 5\}
[/output]
[/test]
[test]
[input]
n 33 i 9 j 80 y 6 u 8
[/input]
[output]
\{'n': 33, 'i': 9, 'j': 80, 'y': 6, 'u': 8\}
[/output]
[/test]
[test]
[input]
k 0 u 1 y 3
[/input]
[output]
\{'k': 0, 'u': 1, 'y': 3\}
[/output]
[/test]
[test]
[input]
k 1 k 2 k 3
[/input]
[output]
\{'k': 3\}
[/output]
[/test]
[test]
[input]
l 10 l 20 h 8 h 10
[/input]
[output]
\{'l': 20, 'h': 10\}
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
