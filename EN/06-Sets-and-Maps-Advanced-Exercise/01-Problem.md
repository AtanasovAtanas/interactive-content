[slide]
# Problem: Unique Usernames
[code-task title="Problem: Unique Usernames" taskId="ff894dc0-6258-47e0-8267-87efe4851e1c" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a simple program that reads from the console a sequence of usernames and keeps a collection with only the unique ones.

Print the collection on the console in order of insertion:

## Examples
| **Input** | **Output** |
| --- | --- |
| 6 | Hello |
| Hello | World |
| Hello | Greeting |
| Hello |  |
| World |  |
| Hello |  |
| Greetings |  |

| **Input** | **Output** |
| --- | --- |
| 10 | Peter |
| Peter | Maria |
| Maria | George |
| Peter | Stephen |
| George | Alexander |
| Stephen |  |
| Maria |  |
| Alexander |  |
| Peter |  |
| Stephen |  |
| George |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
6
Hello
Hello
Hello
World
Hello
Greetings
[/input]
[output]
Hello
World
Greetings
[/output]
[/test]
[test open]
[input]
10
Peter
Maria
Peter
George
Stephen
Maria
Alexander
Peter
Stephen
George
[/input]
[output]
Peter
Maria
George
Stephen
Alexander
[/output]
[/test]
[test]
[input]
0
[/input]
[output]

[/output]
[/test]
[test]
[input]
10
&hhecee&
heehhech
eehddd&e
deddheh&
hddhcc&e
&&&hed&h
eedcc&d&
hedhdeed
edhdcehd
&&&&hedc
[/input]
[output]
&hhecee&
heehhech
eehddd&e
deddheh&
hddhcc&e
&&&hed&h
eedcc&d&
hedhdeed
edhdcehd
&&&&hedc
[/output]
[/test]
[test]
[input]
20
ecdeee&&
c&hhchhc
d&hhdedc
&&e&ehdh
cee&e&ce
decdhd&h
&hd&hdc&
e&dd&hc&
ccec&ehc
ehdhce&h
ec&dedee
hed&hddd
c&hccchd
d&&eecee
eehh&eec
hdhhdchd
ehc&ehee
cc&cdedh
&echh&dh
h&ehd&ce
[/input]
[output]
ecdeee&&
c&hhchhc
d&hhdedc
&&e&ehdh
cee&e&ce
decdhd&h
&hd&hdc&
e&dd&hc&
ccec&ehc
ehdhce&h
ec&dedee
hed&hddd
c&hccchd
d&&eecee
eehh&eec
hdhhdchd
ehc&ehee
cc&cdedh
&echh&dh
h&ehd&ce
[/output]
[/test]
[test]
[input]
100
ehd&ee&e
hcheddhh
&chcedec
&eehdd&d
&he&dedd
&eecc&h&
hededchc
hcdhd&&e
h&hcdehd
ee&h&ce&
eeeece&d
hd&hhh&h
de&h&dhe
hhdhe&he
c&deechh
c&decc&d
cd&&dd&e
c&hcehdh
&&&ed&h&
cdee&cde
ddheh&dc
&dh&hh&h
hc&eh&he
ehhdd&eh
&hddhhce
d&ch&de&
&cechhc&
ecddcdcc
dcedc&&&
cceedecc
cedc&d&d
&cdhedc&
&d&hd&h&
&cddddh&
ededhhhe
hdhcedd&
dhehhdch
h&&de&d&
e&dhhc&c
ed&&&dh&
c&&&ddee
&c&hed&h
&cchhdhc
dchceee&
&hh&d&&e
dhdheh&c
h&hh&h&&
echcdehh
hhhchc&h
ce&cecd&
ecdddcce
ccdeec&d
cc&eehhh
&eec&c&d
ccd&ddeh
cdedh&h&
c&c&hdee
cd&chdch
h&eccdhh
hch&&che
ecc&&dee
&hdddc&d
&eccd&dh
&ch&&dhh
c&hdd&cd
cce&e&he
h&dh&dh&
&&cceced
&hc&hhdd
&ec&h&&&
hd&d&ed&
dcechhce
ecehec&d
ecdcddcc
&&&&&ddd
ddcchecc
&&eee&ec
dhh&cdhh
dhe&cdee
cc&ecedh
eceh&ee&
&dehehdd
ccedc&c&
c&hdecec
dddeddde
hdedc&&h
c&eeeedd
&eeece&d
cc&hhd&c
dhhec&hd
d&&ecech
ddc&hde&
e&&&e&d&
hd&dd&de
dcehcce&
h&hdeh&d
ceh&c&&c
ehdeh&&d
h&hhec&e
c&&c&che
[/input]
[output]
ehd&ee&e
hcheddhh
&chcedec
&eehdd&d
&he&dedd
&eecc&h&
hededchc
hcdhd&&e
h&hcdehd
ee&h&ce&
eeeece&d
hd&hhh&h
de&h&dhe
hhdhe&he
c&deechh
c&decc&d
cd&&dd&e
c&hcehdh
&&&ed&h&
cdee&cde
ddheh&dc
&dh&hh&h
hc&eh&he
ehhdd&eh
&hddhhce
d&ch&de&
&cechhc&
ecddcdcc
dcedc&&&
cceedecc
cedc&d&d
&cdhedc&
&d&hd&h&
&cddddh&
ededhhhe
hdhcedd&
dhehhdch
h&&de&d&
e&dhhc&c
ed&&&dh&
c&&&ddee
&c&hed&h
&cchhdhc
dchceee&
&hh&d&&e
dhdheh&c
h&hh&h&&
echcdehh
hhhchc&h
ce&cecd&
ecdddcce
ccdeec&d
cc&eehhh
&eec&c&d
ccd&ddeh
cdedh&h&
c&c&hdee
cd&chdch
h&eccdhh
hch&&che
ecc&&dee
&hdddc&d
&eccd&dh
&ch&&dhh
c&hdd&cd
cce&e&he
h&dh&dh&
&&cceced
&hc&hhdd
&ec&h&&&
hd&d&ed&
dcechhce
ecehec&d
ecdcddcc
&&&&&ddd
ddcchecc
&&eee&ec
dhh&cdhh
dhe&cdee
cc&ecedh
eceh&ee&
&dehehdd
ccedc&c&
c&hdecec
dddeddde
hdedc&&h
c&eeeedd
&eeece&d
cc&hhd&c
dhhec&hd
d&&ecech
ddc&hde&
e&&&e&d&
hd&dd&de
dcehcce&
h&hdeh&d
ceh&c&&c
ehdeh&&d
h&hhec&e
c&&c&che
[/output]
[/test]
[test]
[input]
10
c&&c&che
c&&c&che
c&&c&che
c&&c&che
c&&c&che
c&&c&che
c&&c&che
c&&c&che
c&&c&che
c&&c&che
[/input]
[output]
c&&c&che
[/output]
[/test]
[/tests]
[/code-task]
[/slide]