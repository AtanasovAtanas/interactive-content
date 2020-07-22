# Problem: Words Lengths

[slide]
# Video

[vimeo-video]
[stream language="EN" videoId="435705200" default /]
[stream language="RO" videoId="436342735"  /]
[/video-vimeo]
[/slide]

[slide hideTitle]
# Problem: Words Lengths
[code-task title="Problem: Words Lengths" taskId="5a115324-381d-4527-af3a-9240985b54ea" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Using **list comprehension**, write a program that receives some **strings** separated by comma and space ", " and prints on the console each **string** with its **length** in the format: "\{first_str\} -> \{first_str_len\}, \{second_str\} -> \{second_str_len\},…"

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter, George, Bill, Lilly, Katy | Peter -> 5, George -> 6, Bill -> 4, Lilly -> 5, Katy -> 4 |
|  |  |

| **Input** | **Output** |
| --- | --- |
| Some, Random, Text | Some -> 4, Random -> 6, Text -> 4 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter, George, Bill, Lilly, Katy
[/input]
[output]
Peter -\> 5, George -\> 6, Bill -\> 4, Lilly -\> 5, Katy -\> 4
[/output]
[/test]
[test open]
[input]
Some, Random, Text
[/input]
[output]
Some -\> 4, Random -\> 6, Text -\> 4
[/output]
[/test]
[test]
[input]
ab, cde, fghi
[/input]
[output]
ab -\> 2, cde -\> 3, fghi -\> 4
[/output]
[/test]
[test]
[input]
ffff, wewqe, trr, dsafas
[/input]
[output]
ffff -\> 4, wewqe -\> 5, trr -\> 3, dsafas -\> 6
[/output]
[/test]
[test]
[input]
a, rwq, fas
[/input]
[output]
a -\> 1, rwq -\> 3, fas -\> 3
[/output]
[/test]
[test]
[input]
kqwlw, foeoqp, dksall, djakslfhfoqp
[/input]
[output]
kqwlw -\> 5, foeoqp -\> 6, dksall -\> 6, djakslfhfoqp -\> 12
[/output]
[/test]
[test]
[input]
djaslkjfaklfja, jwquifhweiufhqoi, faijfdsnjfafklajfkql, rjqiofhweiofjqfpoqefk
[/input]
[output]
djaslkjfaklfja -\> 14, jwquifhweiufhqoi -\> 16, faijfdsnjfafklajfkql -\> 20, rjqiofhweiofjqfpoqefk -\> 21
[/output]
[/test]
[/tests]
[/code-task]
[/slide]