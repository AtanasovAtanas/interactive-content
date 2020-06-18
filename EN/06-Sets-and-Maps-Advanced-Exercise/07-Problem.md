[slide]
# Problem: Fix Emails
[code-task title="Problem: Fix Emails" taskId="080f5e63-4e55-4682-9d06-f2017b86419d" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given a sequence of strings, each on a new line, **until you receive "stop" command**.

First string is a **name** of a person.

On the second line you receive his **email**.

Your task is to **collect** their names and emails, and **remove** emails whose domain ends with "us", "uk" or "com" (case insensitive).

Print in the following format: `{name} –> {email}`

Print:

## Examples
| **Input** | **Output** |
| --- | --- |
| John | John -> johnDoe@softuni.org |
| johnDoe@softuni.org | Peter Smith -> smith.peter@softuni.org |
| Peter Smith |  |
| smith.peter@softuni.org |  |
| Taylor Baker |  |
| baker@gmail.com |  |
| stop |  |

| **Input** | **Output** |
| --- | --- |
| Peter Adamas | Duke Jenkins -> jenkins.duke@softuni.org |
| peter_adams@gmail.com |  |
| Anna Foster |  |
| foster.anna@yahoo.com |  |
| Duke Jenkins |  |
| jenkins.duke@softuni.org |  |
| stop |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John
johnDoe@softuni.org
Peter Smith
smith.peter@softuni.org
Taylor Baker
baker@gmail.com
stop
[/input]
[output]
John -\> johnDoe@softuni.org
Peter Smith -\> smith.peter@softuni.org
[/output]
[/test]
[test open]
[input]
Peter Adamas
peter_adams@gmail.com
Anna Foster
foster.anna@yahoo.com
Duke Jenkins
jenkins.duke@softuni.org
stop
[/input]
[output]
Duke Jenkins -\> jenkins.duke@softuni.org
[/output]
[/test]
[test]
[input]
Evelyn Pearce
pearce.evelyn@gamil.com
Jackson Scott
jackson.scott@softuni.org
Harper Moor
moor@gmail.us
stop
[/input]
[output]
Jackson Scott -\> jackson.scott@softuni.org
[/output]
[/test]
[test]
[input]
stop
[/input]
[output]

[/output]
[/test]
[test]
[input]
Mason Howard
howard.mason@gmail.com
William Miller
miller.william@yahoo.com
Kevin Butler
butler.kevin@gmail.us
stop
[/input]
[output]

[/output]
[/test]
[test]
[input]
Susan Kennedy
kennedy.susan@softuni.org
Tracy Adams
adams.tracy@softuni.bg
Miranda Carter
carter.miranda@greenpeace.org
stop
[/input]
[output]
Susan Kennedy -\> kennedy.susan@softuni.org
Tracy Adams -\> adams.tracy@softuni.bg
Miranda Carter -\> carter.miranda@greenpeace.org
[/output]
[/test]
[test]
[input]
Lynda
lynda@gmail.se
Angela
angela@yahoo.it
Ruth
rith@gmail.bg
Cindy
cindy@gmail.de
Amilia
amilia@gmail.com.uk
stop
[/input]
[output]
Lynda -\> lynda@gmail.se
Angela -\> angela@yahoo.it
Ruth -\> rith@gmail.bg
Cindy -\> cindy@gmail.de
[/output]
[/test]
[/tests]
[/code-task]
[/slide]