[slide hideTitle]
# Problem: Heroes Inventory
[code-task title="Problem: Heroes Inventory" taskId="1a7c8b7f-3d6b-4ab2-80c6-381a9a769df0" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Using **comprehension** write a program that receives some **hero names and items** that need to be added in their inventory (item **name** and item **cost**).

Print the total **amount of items** with their **total cost** for each hero.

On the first line you will receive the **names of the heroes** separated by **comma and space** ", ".

On the next lines until the command "**End**", you will be given **items** with their **cost** in the following format: "\{name\}-\{item\}-\{cost\}".

If an item **already exists** in a hero inventory - **ignore** it.

For each hero print his **name**, the total **items** and the total **cost** of the items in the format: "\{name\} -> Items: \{items_count\}, Cost: \{items_cost\}"

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter, George | Peter -> Items: 2, Cost: 30 |
| Peter-Sword-20 | George -> Items: 2, Cost: 120 |
| Peter-Shield-10 |  |
| George-Gem-100 |  |
| Peter-Sword-15 |  |
| George-Sword-20 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter, George
Peter-Sword-20
Peter-Shield-10
George-Gem-100
Peter-Sword-15
George-Sword-20
End
[/input]
[output]
Peter -\> Items\: 2, Cost\: 30
George -\> Items\: 2, Cost\: 120
[/output]
[/test]
[test]
[input]
a, b
a-g-15
a-l-5
b-o-2
End
[/input]
[output]
a -\> Items\: 2, Cost\: 20
b -\> Items\: 1, Cost\: 2
[/output]
[/test]
[test]
[input]
g
g-f-10
End
[/input]
[output]
g -\> Items\: 1, Cost\: 10
[/output]
[/test]
[test]
[input]
g, e, w
g-p-10
g-p-5
e-l-9
w-i-3
e-y-8
End
[/input]
[output]
g -\> Items\: 1, Cost\: 10
e -\> Items\: 2, Cost\: 17
w -\> Items\: 1, Cost\: 3
[/output]
[/test]
[test]
[input]
b, g
b-f-10
b-q-5
g-e-6
g-n-4
g-o-7
b-l-1
b-l-15
End
[/input]
[output]
b -\> Items\: 3, Cost\: 16
g -\> Items\: 3, Cost\: 17
[/output]
[/test]
[test]
[input]
r, q, t, w
r-p-10
r-i-5
t-y-1
t-o-10
q-m-6
t-k-9
w-v-8
q-n-9
w-z-7
End
[/input]
[output]
r -\> Items\: 2, Cost\: 15
q -\> Items\: 2, Cost\: 15
t -\> Items\: 3, Cost\: 20
w -\> Items\: 2, Cost\: 15
[/output]
[/test]
[/tests]
[/code-task]
[/slide]