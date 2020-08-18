[slide hideTitle]
# Problem: Linked List Traversal
[code-task title="Linked List Traversal" taskId="265b381e-c557-4cd1-ab88-2253f8722edb" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
You need to write your simplified implementation of a generic Linked List which has an Iterator.

The list should support the `Add` and `Remove` operations, should reveal the number of elements it has with a `getSize` function, and should have an implemented iterator (should be **foreachable**).

The `add` method should add the new element at the end of the collection.

The `remove` method should remove the first occurrence of the item starting at the beginning of the collection, if the element is successfully removed the method **returns true**, alternatively, if the element passed is not in the collection the method should **return false**.

The `getSize` method should **return** the number of elements currently in the list.

The **iterator** should iterate over the collection starting from the first entered element.


## Input

On the first line of input, you will receive a number **N**. 

On each of the next **N** lines you will receive a command in one of the following formats:

- `Add {number}` - adds a number to your linked list.
- `Remove {number}` - removes the first occurrence of the number from the linked list. If there is no such element this command leaves the collection **unchanged**.

## Output

The output should consist of exactly 2 lines. 

On the first, you should print the result of calling the `getSize` function on the Linked list. 

On the next lines, you should print **all elements** of the collection by calling **for each** on the collection.

## Constraints

- All numbers in the input will be **valid** integers **between** [2 ^ -32 ... 2 ^ 32 - 1].
- All commands received through the input will be **valid** (will be only `Add` or `Remove`).
- The number **N** will be a positive integer **between** [1 ... 500].

## Hint

You can use the Linked List from your **Workshop**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 | 2 |
| Add 7 | -50 20 |
| Add -50 |  |
| Remove 3 |  |
| Remove 7 |  |
| Add 20 |  |

| **Input** | **Output** |
| --- | --- |
| 6 | 4 |
| Add 13 | 13 20 4 4 |
| Add 4 |  |
| Add 20 |  |
| Add 4 |  |
| Remove 4 |  |
| Add 4 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
Add 7
Add -50
Remove 3
Remove 7
Add 20
[/input]
[output]
2
-50 20
[/output]
[/test]
[test open]
[input]
6
Add 13
Add 4
Add 20
Add 4
Remove 4
Add 4
[/input]
[output]
4
13 20 4 4
[/output]
[/test]
[test]
[input]
5
Add 8
Add -50
Remove 3
Remove 7
Add 20
[/input]
[output]
3
8 -50 20
[/output]
[/test]
[test]
[input]
6
Add 11
Add 4
Add 20
Add 4
Remove 4
Add 4
[/input]
[output]
4
11 20 4 4
[/output]
[/test]
[test]
[input]
11
Add 13
Add 4
Add 0
Add 333333
Add 20
Add 4
Add 4
Add 0
Add 0
Add -10
Add -12335435
[/input]
[output]
11
13 4 0 333333 20 4 4 0 0 -10 -12335435
[/output]
[/test]
[test]
[input]
9
Add 13
Add 4
Add 0
Add 333333
Add 20
Add 4
Remove 4
Remove 0
Add 4
[/input]
[output]
5
13 333333 20 4 4
[/output]
[/test]
[test]
[input]
11
Add 13
Add 4
Add 0
Add 333333
Add 20
Add 4
Remove 4
Remove 0
Add 4
Add 0
Add 0
[/input]
[output]
7
13 333333 20 4 4 0 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]