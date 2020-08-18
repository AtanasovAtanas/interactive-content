[slide hideTitle]
# Problem: The Party Reservation Filter Module
[code-task title="The Party Reservation Filter Module" taskId="e483e892-9ef3-48ad-b316-d8a29e327fa8" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are a young and talented **developer**.

The first task you need to do is to implement a **filtering module** to a party reservation software.

First, The Party Reservation Filter Module ( **TPRF** Module for short) is passed a **list** with invitations.

Next, the **TPRF** receives a sequence of **commands** that specify if you need to add or remove a given filter.

**TPRF** Commands are in the given format `{command;filter type;filter parameter}`

You can receive the following **TPRF** commands: `Add filter`, `Remove filter`, or `Print`. 

The possible **TPRF** filter types are: `Starts with`, `Ends with`, `Length` and `Contains`. 

All **TPRF** filter parameters will be a **String**(or an **Integer** for the length filter).

The input will end with a `Print` command. 

See the examples below:

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter Michael Steven | Steven |
| Add filter;Starts with;P |  |
| Add filter;Starts with;M |  |
| Print |  |

| **Input** | **Output** |
| --- | --- |
| Pete Mich John | Mich John  |
| Add filter;Starts with;P |  |
| Add filter;Starts with;M |  |
| Remove filter;Starts with;M |  |
| Print |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter Michael Steven
Add filter;Starts with;P
Add filter;Starts with;M
Print
[/input]
[output]
Steven
[/output]
[/test]
[test open]
[input]
Pete Mich John
Add filter;Starts with;P
Add filter;Starts with;M
Remove filter;Starts with;M
Print
[/input]
[output]
Mich John
[/output]
[/test]
[test]
[input]
Peter
Add filter;Starts with;P
Add filter;Starts with;M
Add filter;Starts with;G
Remove filter;Starts with;P
Print
[/input]
[output]
Peter
[/output]
[/test]
[test]
[input]
G G G G P
Add filter;Contains;G
Print
[/input]
[output]
P
[/output]
[/test]
[test]
[input]
L O S H O M I E
Add filter;Contains;M
Add filter;Starts with;I
Add filter;Ends with;E
Print
[/input]
[output]
L O S H O
[/output]
[/test]
[test]
[input]
Deadpool Spiderman Romanov Fury
Add filter;Starts with;F
Add filter;Contains;man
Add filter;Contains;G
Remove filter;Starts with;F
Print
[/input]
[output]
Deadpool Fury
[/output]
[/test]
[test]
[input]
P
Add filter;Starts with;P
Add filter;Starts with;M
Add filter;Starts with;G
Print
[/input]
[output]

[/output]
[/test]
[/tests]
[/code-task]
[/slide]