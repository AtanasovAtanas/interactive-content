[slide]
# Problem: Matrix Shuffling
[code-task title="Problem: Matrix Shuffling" taskId="52ef2b01-c6e8-42ca-bb12-7fa69625f36a" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program which reads a string matrix from the console and performs certain operations with its elements.

User input is provided in a similar way like in the problems above – first you read the **dimensions** and then the **data**.

Your program should then receive commands in format: **"swap row1 col1 row2c col2"** where row1, row2, col1, col2 are **coordinates** in the matrix. 

In order for a command to be valid, it should start with the **"swap"** keyword along with **four valid coordinates** (no more, no less). 

You should **swap the values** at the given coordinates (cell [row1, col1] with cell [row2, col2]) **and print the matrix at each step** (thus you will be able to check if the operation was performed correctly).

If the **command is not valid** (does not contain the keyword "swap", has fewer or more coordinates entered or the given coordinates do not exist), print **"Invalid input!"** and move on to the next command. Your program should finish when the string **"END"** is entered.

## Hints

Think about Exception Handling

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 3 | 5 2 3 |
| 1 2 3 | 4 1 6 |
| 4 5 6 | Invalid input! |
| swap 0 0 1 1 | 5 4 3 |
| swap 10 9 8 7 | 2 1 6 |
| swap 0 1 1 0 |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| 1 2 | Invalid input! |
| Hello World | World Hello |
| 0 0 0 1 | Hello World |
| swap 0 0 0 1 |  |
| swap 0 1 0 0 |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2 3
1 2 3
4 5 6
swap 0 0 1 1
swap 10 9 8 7
swap 0 1 1 0
END
[/input]
[output]
5 2 3 
4 1 6 
Invalid input!
5 4 3 
2 1 6
[/output]
[/test]
[test open]
[input]
1 2
Hello World
0 0 0 1
swap 0 0 0 1
swap 0 1 0 0
END
[/input]
[output]
Invalid input!
World Hello 
Hello World
[/output]
[/test]
[test]
[input]
20 10
1 1 1 2 2 0 1 0 0 0 
1 0 1 0 2 1 2 2 0 2 
0 0 0 1 0 0 2 0 2 1 
1 2 0 0 2 0 2 1 0 1 
0 2 1 2 0 1 1 0 2 2 
1 1 1 0 0 1 2 2 1 1 
0 2 2 1 2 0 1 1 2 2 
0 2 0 2 0 0 1 0 1 0 
0 0 2 2 1 2 2 1 0 1 
2 1 2 1 1 0 0 2 1 2 
2 0 1 0 2 2 0 1 2 1 
1 2 0 2 0 2 1 1 1 1 
2 2 0 2 1 1 2 0 0 0 
2 0 0 0 2 1 1 1 2 2 
2 2 0 1 0 0 2 0 0 0 
0 0 0 1 2 1 2 1 0 1 
2 1 1 0 1 0 1 2 0 1 
0 0 0 2 0 1 0 1 2 1 
0 0 0 2 1 2 0 0 1 2 
1 0 1 2 0 1 1 2 1 1 
END
[/input]
[output]

[/output]
[/test]
[test]
[input]
20 10
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
swap 0 0 1 1
swap 10 9 8 7
swap 0 1 1 0
END
[/input]
[output]
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0
[/output]
[/test]
[test]
[input]
5 6
1 1 1 0 1 1 
0 1 1 1 0 0 
1 0 1 0 0 1 
0 0 0 1 1 1 
1 1 1 0 1 0 
swap 0 0 1 1
swap 10 9 8 7
swap 0 1 1 0swap 0 0 1 1
swap 10 9 8 7
swap 0 1 1 0
END
[/input]
[output]
1 1 1 0 1 1 
0 1 1 1 0 0 
1 0 1 0 0 1 
0 0 0 1 1 1 
1 1 1 0 1 0 
Invalid input!
Invalid input!
Invalid input!
1 0 1 0 1 1 
1 1 1 1 0 0 
1 0 1 0 0 1 
0 0 0 1 1 1 
1 1 1 0 1 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]