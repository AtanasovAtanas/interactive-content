# Looping through Lists

[slide]
# For-Loop

There are two ways you can loop through a list using `for` loops.

One of them is to indices to access each element in the list.

This is done by using the `range()` function and passing the number of elements.

It will iterate from index 0 to the last valid one.

```python live
my_list = ["dog", "cat", "fish"]
for index in range(len(my_list)):
   print(my_list[index], end=" ") # dog cat fish 
```

The other way is to iterate over the elements.

Notice that using this way, indices are not needed because the loop iterates over the elements themselves, accessing them directly.

```python live
my_list = ["dog", "cat", "fish"]
for element in my_list:
   print(element, end=" ") # dog cat fish
```

[/slide]

[slide]
# While-Loop

The `while` loop can be used to iterate through a list too.

One way is by using the `pop()` function and iterating while there are still elements in the list.

```python live
my_list = ["dog", "cat", "fish"]
while len(my_list) > 0:
    print(my_list.pop(0), end=" ")
```

**Note:** It is recommended to always pop the first or last element of the list.

The way demonstrated above will leave the list empty.

You most likely don't want that to happen, so there is other way which won't remove any of the elements.

You'll need to keep track of the accessed index outside of the loop.

```python live
my_list = ["dog", "cat", "fish"]
index = 0
while index < len(my_list):
    print(my_list[index], end=" ")
    index += 1
```

[/slide]

[slide]
# Problem: List Statistics
[code-task title="List Statistics" taskId="python-fund-07-Arrays-problem-5" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will be given a number **n**.

On the next **n lines** you will receive **integers**.

You have to create and print **two lists**:

 - One with all the **positives** (including 0)
 - One with all the **negatives**

Finally print the following message: "Count of positives: {count_positives}. Sum of negatives: {sum_of_negatives}"

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 | [10, 3, 2] |
| 10 | [-15, -4] |
| 3 | Count of positives: 3. Sum of negatives: -19 |
| 2 |  |
| -15 |  |
| -4 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
10
3
2
-15
-4
[/input]
[output]
\[10, 3, 2\]
\[-15, -4\]
Count of positives: 3. Sum of negatives: -19
[/output]
[/test]
[test]
[input]
5
10
45
-5
-10
55
[/input]
[output]
\[10, 45, 55\]
\[-5, -10\]
Count of positives: 3. Sum of negatives: -15
[/output]
[/test]
[test]
[input]
10
53
985
-188
95
-42
-1
41
-9
-11
41
[/input]
[output]
\[53, 985, 95, 41, 41\]
\[-188, -42, -1, -9, -11\]
Count of positives: 5. Sum of negatives: -251
[/output]
[/test]
[test]
[input]
6
11
2
35
599
31
20
[/input]
[output]
\[11, 2, 35, 599, 31, 20\]
\[\]
Count of positives: 6. Sum of negatives: 0
[/output]
[/test]
[test]
[input]
4
-16
-99
-51
-88
[/input]
[output]
\[\]
\[-16, -99, -51, -88\]
Count of positives: 0. Sum of negatives: -254
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
\[\]
\[\]
Count of positives: 0. Sum of negatives: 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: List Statistics
[code-task title="List Statistics" taskId="python-fund-07-Arrays-problem-6" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
n = int(input())
positives = []
negatives = []
for n in range(n):
    current_number = int(input())
    if current_number >= 0:
        positives.append(current_number)
    else:
        negatives.append(current_number)
print(positives)
print(negatives)
print(f"Count of positives: {len(positives)}. Sum of negatives: {sum(negatives)}")
```
[/code-editor]
[task-description]
## Description
You will be given a number **n**.

On the next **n lines** you will receive **integers**.

You have to create and print **two lists**:

 - One with all the **positives** (including 0)
 - One with all the **negatives**

Finally print the following message: "Count of positives: {count_positives}. Sum of negatives: {sum_of_negatives}"

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 | [10, 3, 2] |
| 10 | [-15, -4] |
| 3 | Count of positives: 3. Sum of negatives: -19 |
| 2 |  |
| -15 |  |
| -4 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
10
3
2
-15
-4
[/input]
[output]
\[10, 3, 2\]
\[-15, -4\]
Count of positives: 3. Sum of negatives: -19
[/output]
[/test]
[test]
[input]
5
10
45
-5
-10
55
[/input]
[output]
\[10, 45, 55\]
\[-5, -10\]
Count of positives: 3. Sum of negatives: -15
[/output]
[/test]
[test]
[input]
10
53
985
-188
95
-42
-1
41
-9
-11
41
[/input]
[output]
\[53, 985, 95, 41, 41\]
\[-188, -42, -1, -9, -11\]
Count of positives: 5. Sum of negatives: -251
[/output]
[/test]
[test]
[input]
6
11
2
35
599
31
20
[/input]
[output]
\[11, 2, 35, 599, 31, 20\]
\[\]
Count of positives: 6. Sum of negatives: 0
[/output]
[/test]
[test]
[input]
4
-16
-99
-51
-88
[/input]
[output]
\[\]
\[-16, -99, -51, -88\]
Count of positives: 0. Sum of negatives: -254
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
\[\]
\[\]
Count of positives: 0. Sum of negatives: 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]