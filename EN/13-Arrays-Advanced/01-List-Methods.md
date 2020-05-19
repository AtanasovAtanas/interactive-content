# List Methods

[slide]
# Adding Elements

We can add an element to the **end of the list** with the `append([element])` function.

```python live
my_list = [1, 2, 3]
my_list.append(4)
print(my_list) # [1, 2, 3, 4]
```

To add an element to a **specific index**, use the `insert(index, element)` function.

The first parameter is the index and the second - the element to be added.

```python live
my_list = [1, 3, 4]
my_list.insert(1, 2)
print(my_list) # [1, 2, 3, 4]
```

There is also a way to **merge two lists**.

This is done by using the `extend(list)` function.

**All** of the elements of the list **given as a parameter** will be appended to the **end** of the list that this function is being **executed over**.

```python live
my_list = [1, 2, 3]
my_list.extend([4, 5, 6])
print(my_list)
```

[/slide]

[slide]
# Removing Elements

To remove an element from a list, the function `remove(element)` can be used.

It removes the **first occurrence** of the element given in the braces.

If such element **doesn't exist** in the list, a `ValueError` will be raised.

```python live
my_list = [1, 2, 3, 2]
my_list.remove(2)
print(my_list) # [1, 3, 2]
```

To remove **all** elements of a list, use the `clear()` function.

```python live
my_list = [1, 2, 3]
my_list.clear()
print(my_list) # []
```

There is also a way to remove an element at a **given index**, which also **returns** it.

For this purpose, the `pop([index])` function is used.

**Note:** The parameter `index` is between **square brackets**, it means that the parameter is **optional**. If **no index** is passed as a parameter, the function will remove (and return) the **last** element of the list.

```python live
my_list = [1, 2, 3, 4, 5, 6]
print(my_list.pop(2)) # 3
print(my_list.pop()) # 6
print(my_list) # [1, 2, 4, 5]
```

[/slide]

[slide]
# Problem: Trains
[code-task title="Trains" taskId="python-fundamentals-Lists-Advanced-01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive how many **wagons** the train has.

Create a **list** with that length **with all zeros**.

Until you receive the command "**End**", you get some of the following commands:

 - **add {people}** -> adds the people in the last wagon
 - **insert {index} {people}** -> adds the people at the given wagon
 - **leave {index} {people}** -> removes the people from the wagon

After you receive the "**End**" command print the train.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | [10, 0, 20] |
| add 20 |  |
| insert 0 15 |  |
| leave 0 5 |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| 5 | [16, 32, 100, 0, 105] |
| add 10 |  |
| add 20 |  |
| insert 0 16 |  |
| insert 1 44 |  |
| leave 1 12 |  |
| insert 2 100 |  |
| insert 4 61 |  |
| leave 4 1 |  |
| add 15 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
add 20
insert 0 15
leave 0 5
End
[/input]
[output]
\[10, 0, 20\]
[/output]
[/test]
[test open]
[input]
5
add 10
add 20
insert 0 16
insert 1 44
leave 1 12
insert 2 100
insert 4 61
leave 4 1
add 15
End
[/input]
[output]
\[16, 32, 100, 0, 105\]
[/output]
[/test]
[test]
[input]
1
add 10
add 5
End
[/input]
[output]
\[15\]
[/output]
[/test]
[test]
[input]
2
insert 0 5
insert 1 10
End
[/input]
[output]
\[5, 10\]
[/output]
[/test]
[test]
[input]
1
add 10
leave 0 5
End
[/input]
[output]
\[5\]
[/output]
[/test]
[test]
[input]
4
add 10
add 4
insert 0 7
insert 1 4
insert 2 5
End
[/input]
[output]
\[7, 4, 5, 14\]
[/output]
[/test]
[test]
[input]
10
insert 0 10
insert 1 5
leave 1 5
insert 5 9
insert 8 11
add 20
add 5
End
[/input]
[output]
\[10, 0, 0, 0, 0, 9, 0, 0, 11, 25\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Trains
[code-task title="Trains" taskId="bca88243-e96e-4ff6-96b8-b0a62678cbda" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
train_length = int(input())
train = [0] * train_length

command = input()
while command != "End":
    tokens = command.split(" ")
    key_word = tokens[0]
    if key_word == "add":
        people = int(tokens[1])
        train[train_length - 1] += people
    elif key_word == "insert":
        position = int(tokens[1])
        people = int(tokens[2])
        train[position] += people
    elif key_word == "leave":
        position = int(tokens[1])
        people = int(tokens[2])
        train[position] -= people
    command = input()
print(train)
```
[/code-editor]
[task-description]
## Description
You will receive how many **wagons** the train has.

Create a **list** with that length **with all zeros**.

Until you receive the command "**End**", you get some of the following commands:

 - **add {people}** -> adds the people in the last wagon
 - **insert {index} {people}** -> adds the people at the given wagon
 - **leave {index} {people}** -> removes the people from the wagon

After you receive the "**End**" command print the train.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | [10, 0, 20] |
| add 20 |  |
| insert 0 15 |  |
| leave 0 5 |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| 5 | [16, 32, 100, 0, 105] |
| add 10 |  |
| add 20 |  |
| insert 0 16 |  |
| insert 1 44 |  |
| leave 1 12 |  |
| insert 2 100 |  |
| insert 4 61 |  |
| leave 4 1 |  |
| add 15 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
add 20
insert 0 15
leave 0 5
End
[/input]
[output]
\[10, 0, 20\]
[/output]
[/test]
[test open]
[input]
5
add 10
add 20
insert 0 16
insert 1 44
leave 1 12
insert 2 100
insert 4 61
leave 4 1
add 15
End
[/input]
[output]
\[16, 32, 100, 0, 105\]
[/output]
[/test]
[test]
[input]
1
add 10
add 5
End
[/input]
[output]
\[15\]
[/output]
[/test]
[test]
[input]
2
insert 0 5
insert 1 10
End
[/input]
[output]
\[5, 10\]
[/output]
[/test]
[test]
[input]
1
add 10
leave 0 5
End
[/input]
[output]
\[5\]
[/output]
[/test]
[test]
[input]
4
add 10
add 4
insert 0 7
insert 1 4
insert 2 5
End
[/input]
[output]
\[7, 4, 5, 14\]
[/output]
[/test]
[test]
[input]
10
insert 0 10
insert 1 5
leave 1 5
insert 5 9
insert 8 11
add 20
add 5
End
[/input]
[output]
\[10, 0, 0, 0, 0, 9, 0, 0, 11, 25\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Todo List
[code-task title="Todo List" taskId="python-fundamentals-Lists-Advanced-02" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will receive a **todo-notes** until you get the command "**End**".

The notes will be in the format: "**{importance}-{value}**".

Return the list of **todo-notes** sorted by **importance**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2-Walk the dog | ['Drink coffee', 'Walk the dog', 'Work', Dinner'] |
| 1-Drink coffee |  |
| 6-Dinner |  |
| 5-Work |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2-Walk the dog
1-Drink coffee
6-Dinner
5-Work
End
[/input]
[output]
\['Drink coffee', 'Walk the dog', 'Work', 'Dinner'\]
[/output]
[/test]
[test]
[input]
1-A
4-B
3-C
End
[/input]
[output]
\['A', 'C', 'B'\]
[/output]
[/test]
[test]
[input]
3-C
2-A
1-B
6-V
End
[/input]
[output]
\['B', 'A', 'C', 'V'\]
[/output]
[/test]
[test]
[input]
3-C
2-B
1-A
End
[/input]
[output]
\['A', 'B', 'C'\]
[/output]
[/test]
[test]
[input]
10-C
5-F
4-H
6-I
1-O
End
[/input]
[output]
\['O', 'H', 'I', 'F', 'C'\]
[/output]
[/test]
[test]
[input]
9-H
5-H
1-U
4-G
End
[/input]
[output]
\['U', 'G', 'H', 'H'\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Todo List
[code-task title="Todo List" taskId="5cf70246-9af4-44c6-9ed3-e01904febd3b" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
command = input()
notes = [0] * 10
while command != "End":
    tokens = command.split("-")
    priority = int(tokens[0])
    note = tokens[1]
    notes.insert(priority, note)
    command = input()
result = []
for element in notes:
    if element != 0:
        result.append(element)
print(result)
```
[/code-editor]
[task-description]
## Description
You will receive a **todo-notes** until you get the command "**End**".

The notes will be in the format: "**{importance}-{value}**".

Return the list of **todo-notes** sorted by **importance**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2-Walk the dog | ['Drink coffee', 'Walk the dog', 'Work', Dinner'] |
| 1-Drink coffee |  |
| 6-Dinner |  |
| 5-Work |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2-Walk the dog
1-Drink coffee
6-Dinner
5-Work
End
[/input]
[output]
\['Drink coffee', 'Walk the dog', 'Work', 'Dinner'\]
[/output]
[/test]
[test]
[input]
1-A
4-B
3-C
End
[/input]
[output]
\['A', 'C', 'B'\]
[/output]
[/test]
[test]
[input]
3-C
2-A
1-B
6-V
End
[/input]
[output]
\['B', 'A', 'C', 'V'\]
[/output]
[/test]
[test]
[input]
3-C
2-B
1-A
End
[/input]
[output]
\['A', 'B', 'C'\]
[/output]
[/test]
[test]
[input]
10-C
5-F
4-H
6-I
1-O
End
[/input]
[output]
\['O', 'H', 'I', 'F', 'C'\]
[/output]
[/test]
[test]
[input]
9-H
5-H
1-U
4-G
End
[/input]
[output]
\['U', 'G', 'H', 'H'\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Palindrome
[code-task title="Palindrome" taskId="python-fundamentals-Lists-Advanced-03" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program that receives on the **first line** words separated by a **space** and a **searched palindrome** on the **second**.

Print **all the palindromes** on the first line.

Print all the **occurrences** of the **searched** palindrome in the format: "**Found palindrome {count} times**".

## Examples
| **Input** | **Output** |
| --- | --- |
| wow father mom wow shirt stats | ['wow', 'mom', 'wow', 'stats'] |
| wow | Found palindrome 2 times |
|  |  |

| **Input** | **Output** |
| --- | --- |
| hey how you doin? lol | ['lol'] |
| mom | Found palindrome 0 times |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
wow father mom wow shirt stats
wow
[/input]
[output]
\['wow', 'mom', 'wow', 'stats'\]
Found palindrome 2 times
[/output]
[/test]
[test open]
[input]
hey how you doin? lol
mom
[/input]
[output]
\['lol'\]
Found palindrome 0 times
[/output]
[/test]
[test]
[input]
willy billy silly milly
wow
[/input]
[output]
\[\]
Found palindrome 0 times
[/output]
[/test]
[test]
[input]
ala bala alabala
lol
[/input]
[output]
\['ala', 'alabala'\]
Found palindrome 0 times
[/output]
[/test]
[test]
[input]
alabala portokala wow alabala
wow
[/input]
[output]
\['alabala', 'wow', 'alabala'\]
Found palindrome 1 times
[/output]
[/test]
[test]
[input]
alabala wow wow alabala portokala
alabala
[/input]
[output]
\['alabala', 'wow', 'wow', 'alabala'\]
Found palindrome 2 times
[/output]
[/test]
[test]
[input]
stats tats stats mats stats
stats
[/input]
[output]
\['stats', 'stats', 'stats'\]
Found palindrome 3 times
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Palindrome
[code-task title="Palindrome" taskId="e09fbe59-d85d-4f2a-b0e2-b11cbe43eb9b" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
strings = input().split(" ")
searched_palindrome = input()
palindromes = []

for word in strings:
    if word == "".join(reversed(word)):
        palindromes.append(word)

print(f"{palindromes}")
print(f"Found palindrome {palindromes.count(searched_palindrome)} times")
```
[/code-editor]
[task-description]
## Description
Write a program that receives on the **first line** words separated by a **space** and a **searched palindrome** on the **second**.

Print **all the palindromes** on the first line.

Print all the **occurrences** of the **searched** palindrome in the format: "**Found palindrome {count} times**".

## Examples
| **Input** | **Output** |
| --- | --- |
| wow father mom wow shirt stats | ['wow', 'mom', 'wow', 'stats'] |
| wow | Found palindrome 2 times |
|  |  |

| **Input** | **Output** |
| --- | --- |
| hey how you doin? lol | ['lol'] |
| mom | Found palindrome 0 times |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
wow father mom wow shirt stats
wow
[/input]
[output]
\['wow', 'mom', 'wow', 'stats'\]
Found palindrome 2 times
[/output]
[/test]
[test open]
[input]
hey how you doin? lol
mom
[/input]
[output]
\['lol'\]
Found palindrome 0 times
[/output]
[/test]
[test]
[input]
willy billy silly milly
wow
[/input]
[output]
\[\]
Found palindrome 0 times
[/output]
[/test]
[test]
[input]
ala bala alabala
lol
[/input]
[output]
\['ala', 'alabala'\]
Found palindrome 0 times
[/output]
[/test]
[test]
[input]
alabala portokala wow alabala
wow
[/input]
[output]
\['alabala', 'wow', 'alabala'\]
Found palindrome 1 times
[/output]
[/test]
[test]
[input]
alabala wow wow alabala portokala
alabala
[/input]
[output]
\['alabala', 'wow', 'wow', 'alabala'\]
Found palindrome 2 times
[/output]
[/test]
[test]
[input]
stats tats stats mats stats
stats
[/input]
[output]
\['stats', 'stats', 'stats'\]
Found palindrome 3 times
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# More Methods

The `count(element)` function is used to get the **number of occurrences of an element**.

```python live
my_list = [1, 2, 3, 4, 4, 4]
print(my_list.count(4)) # 3
print(my_list.count(7)) # 0
```

The `index(element)` function is used to find at **which index an element is located**.

```python live
my_list = [1, 2, 3, 4]
print(my_list.index(2)) # 1
```

If there is **no such element** in the list, a `ValueError` will be raised.

```python live
my_list = [1, 2, 3, 4]
print(my_list.index(7)) # ValueError
```

The `reverse()` method reverses the elements of the list upon which it is called.

```python live
my_list = [1, 2, 3, 4, 5]
my_list.reverse()
print(my_list) # [5, 4, 3, 2, 1]
```

[/slide]