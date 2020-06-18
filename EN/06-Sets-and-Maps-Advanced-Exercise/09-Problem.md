[slide]
# Problem: User Logs
[code-task title="Problem: User Logs" taskId="b541fef2-5fe6-4107-aedf-588697d7a672" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
John is a famous system administrator.

The person to overcome the security of his servers has not yet been born.

However, there is a new type of threat where users flood the server with messages and are hard to be detected since they change their IP address all the time.

Well, Marian is a system administrator and is not so into programming.

Therefore, he needs a skillful programmer to track the user logs of his servers.

You are the chosen one to help him!

You are given an input in the format:

**IP=(IP.Address) message=(A&sample&message) user=(username)**

Your task is to **parse** the **IP** and the **username** from the input and for **every user** , you have to display **every IP** from which the corresponding user has sent a message and the **count of the messages** sent with the corresponding IP. In the output, the usernames must be **sorted alphabetically** while their IP addresses should be displayed in the **order of their first appearance.** The output should be in the following format:

**username:**

**IP => count, IP => count.**

For example, given the following input - **IP=192.23.30.40 message='Hello&derps.' user=destroyer** , you have to get theusername **destroyer** and the IP **192.23.30.40** and display it in the following format:

**destroyer:**

**192.23.30.40 => 1.**

The username destroyer has sent a message from IP 192.23.30.40 once.

Check the examples below. They will further clarify the assignment.

## Input

The input comes from the console as **varying number** of lines. You have to parse every command until the command that follows is **end.** The input will be in the format displayed above, there is no need to check it explicitly.

## Output

For every user found, you have to display each log in the format:

**username:**

**IP => count, IP => count…**

The IP addresses must be split with a comma, and each line of IP addresses must end with a dot.

## Constraints

- The number of commands will be in the range [1 ... 50]
- The IP addresses will be in the format of either **IPv4** or **IPv6.**
- The messages will be in the format: **This&is&a&message**
- The username will be a string with length in the range [3 ... 50]
- Time limit: 0.3 sec. Memory limit: 16 MB.

## Examples
| **Input** | **Output** |
| --- | --- |
| IP=192.23.30.40 message='Hello&derps.' user=destroyer | destroyer:  |
| IP=192.23.30.41 message='Hello&yall.' user=destroyer | 192.23.30.40 => 2, 192.23.30.41 => 1, 192.23.30.42 => 1. |
| IP=192.23.30.40 message='Hello&hi.' user=destroyer |  |
| IP=192.23.30.42 message='Hello&People.' user=destroyer |  |
| end |  |

| **Input** | **Output** |
| --- | --- |
| IP=FE80:0000:0000:0000:0202:B3FF:FE1E:8329 message='Hey&son' user=mother | child0:  |
| IP=192.23.33.40 message='Hi&mom!' user=child0 | 192.23.33.40 => 1. |
| IP=192.23.30.40 message='Hi&from&me&too' user=child1 | child1:  |
| IP=192.23.30.42 message='spam' user=destroyer | 192.23.30.40 => 1. |
| IP=192.23.30.42 message='spam' user=destroyer | destroyer:  |
| IP=192.23.50.40 message='' user=yetAnotherUsername | 192.23.30.42 => 2. |
| IP=192.23.50.40 message='comment' user=yetAnotherUsername | mother:  |
| IP=192.23.155.40 message='Hello.' user=unknown | FE80:0000:0000:0000:0202:B3FF:FE1E:8329 => 1. |
| end | unknown:  |
|  | 192.23.155.40 => 1. |
|  | yetAnotherUsername:  |
|  | 192.23.50.40 => 2. |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.41 message='Hello&yall.' user=destroyer
IP=192.23.30.40 message='Hello&hi.' user=destroyer
IP=192.23.30.42 message='Hello&Dudes.' user=destroyer
end
[/input]
[output]
destroyer: 
192.23.30.40 =\> 2, 192.23.30.41 =\> 1, 192.23.30.42 =\> 1.
[/output]
[/test]
[test open]
[input]
IP=FE80:0000:0000:0000:0202:B3FF:FE1E:8329 message='Hey&son' user=mother
IP=192.23.33.40 message='Hi&mom!' user=child0
IP=192.23.30.40 message='Hi&from&me&too' user=child1
IP=192.23.30.42 message='spam' user=destroyer
IP=192.23.30.42 message='spam' user=destroyer
IP=192.23.50.40 message='' user=yetAnotherUsername
IP=192.23.50.40 message='comment' user=yetAnotherUsername
IP=192.23.155.40 message='Hello.' user=unknown
end
[/input]
[output]
child0: 
192.23.33.40 =\> 1.
child1: 
192.23.30.40 =\> 1.
destroyer: 
192.23.30.42 =\> 2.
mother: 
FE80:0000:0000:0000:0202:B3FF:FE1E:8329 =\> 1.
unknown: 
192.23.155.40 =\> 1.
yetAnotherUsername: 
192.23.50.40 =\> 2.
[/output]
[/test]
[test]
[input]
IP=192.23.30.44 message='hiiiii' user=hier
IP=192.23.33.45 message='Hi&mom!' user=blabla
IP=192.23.30.42 message='Hi&from&me&too' user=someone
IP=192.23.30.42 message='spam' user=destroyer
IP=192.23.30.42 message='spam' user=destroyer
IP=192.23.50.44 message='' user=yetAnotherUsername
IP=192.23.50.40 message='comment' user=yetAnotherUsername
IP=192.23.155.40 message='Hello.' user=mario
end
[/input]
[output]
blabla: 
192.23.33.45 =\> 1.
destroyer: 
192.23.30.42 =\> 2.
hier: 
192.23.30.44 =\> 1.
mario: 
192.23.155.40 =\> 1.
someone: 
192.23.30.42 =\> 1.
yetAnotherUsername: 
192.23.50.44 =\> 1, 192.23.50.40 =\> 1.
[/output]
[/test]
[test]
[input]
end
[/input]
[output]

[/output]
[/test]
[test]
[input]
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=mario
IP=192.23.30.44 message='Hello&derps.' user=mario
IP=192.23.30.40 message='Hello&derps.' user=destroyer
end
[/input]
[output]
destroyer: 
192.23.30.40 =\> 4, 192.23.30.42 =\> 2.
mario: 
192.23.30.40 =\> 1, 192.23.30.44 =\> 1.
[/output]
[/test]
[test]
[input]
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=mario
IP=192.23.30.44 message='Hello&derps.' user=mario
IP=192.23.30.40 message='Hello&derps.' user=destroyer
end
[/input]
[output]
destroyer: 
192.23.30.40 =\> 4, 192.23.30.42 =\> 2.
mario: 
192.23.30.40 =\> 1, 192.23.30.44 =\> 1.
[/output]
[/test]
[test]
[input]
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=592.23.300.40 message='Hello&derps.' user=destroyer
IP=192.222.30.40 message='Hello&derps.' user=destroyer
IP=192.234.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=mario
IP=422.23.30.44 message='Hello&derps.' user=mario
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=592.23.300.40 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=mario
IP=192.234.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
end
[/input]
[output]
destroyer: 
192.23.30.40 =\> 4, 592.23.300.40 =\> 2, 192.222.30.40 =\> 1, 192.234.30.42 =\> 1, 192.23.30.42 =\> 3, 192.234.30.40 =\> 1.
mario: 
192.23.30.40 =\> 2, 422.23.30.44 =\> 1.
[/output]
[/test]
[test]
[input]
IP=192.23.500.40 message='Hello&derps.' user=destroyer
IP=192.23.366.40 message='asdasdasd' user=greetings
IP=192.23.111.40 message='sdfsdfsd' user=bojo
IP=192.245.30.42 message='Hello&derps.' user=bojo
IP=192.254.30.42 message='Hello&derps.' user=marian
IP=192.666.30.40 message='Aloha' user=hello9
IP=192.999.30.44 message='asfdsfdsf' user=hello
IP=192.120.30.40 message='ggdsfdsfsd' user=zzzzzzzzzzz
IP=192.23.30.500 message='spampamapmapa' user=bbbbbbbb
IP=192.23.30.666 message='yoooooo' user=aaaa
IP=192.23.30.642 message='heyooo' user=sdfsdf
IP=192.23.30.123 message='fgfgfgfgd' user=destroyer
IP=192.23.245.545 message='grrrrrrrrr' user=mario
IP=192.23.123.40 message='aaaaaaaa' user=destroyer
IP=192.23.467.40 message='aaaaaaaaa' user=destroyer
end
[/input]
[output]
aaaa: 
192.23.30.666 =\> 1.
bbbbbbbb: 
192.23.30.500 =\> 1.
bojo: 
192.23.111.40 =\> 1, 192.245.30.42 =\> 1.
destroyer: 
192.23.500.40 =\> 1, 192.23.30.123 =\> 1, 192.23.123.40 =\> 1, 192.23.467.40 =\> 1.
greetings: 
192.23.366.40 =\> 1.
hello: 
192.999.30.44 =\> 1.
hello9: 
192.666.30.40 =\> 1.
marian: 
192.254.30.42 =\> 1.
mario: 
192.23.245.545 =\> 1.
sdfsdf: 
192.23.30.642 =\> 1.
zzzzzzzzzzz: 
192.120.30.40 =\> 1.
[/output]
[/test]
[test]
[input]
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=destroyer
end
[/input]
[output]
destroyer: 
192.23.30.40 =\> 5.
[/output]
[/test]
[test]
[input]
IP=192.23.30.42 message='Hello&derps.' user=destroyer
IP=192.23.30.40 message='Hello&derps.' user=mario
IP=192.23.30.44 message='Hello&derps.' user=mario
IP=192.23.30.40 message='Hello&derps.' user=destroyer
end
[/input]
[output]
destroyer: 
192.23.30.42 =\> 1, 192.23.30.40 =\> 1.
mario: 
192.23.30.40 =\> 1, 192.23.30.44 =\> 1.
[/output]
[/test]
[test]
[input]
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=nasko
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=nasko
IP=192.239.500.123 message='spam' user=hello
IP=192.239.500.123 message='spam' user=mario
IP=192.239.500.123 message='spam' user=mario
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=borko
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=krasi
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=mario
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=mitko
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=destroyer
IP=192.239.500.123 message='spam' user=mario
IP=2001:0000:5ef5:79fd:8aa:9D2:3f57:860a message='spam' user=asshole
end
[/input]
[output]
asshole: 
2001:0000:5ef5:79fd:8aa:9D2:3f57:860a =\> 1.
borko: 
192.239.500.123 =\> 1.
destroyer: 
192.239.500.123 =\> 9.
hello: 
192.239.500.123 =\> 1.
krasi: 
192.239.500.123 =\> 1.
mario: 
192.239.500.123 =\> 4.
mitko: 
192.239.500.123 =\> 1.
nasko: 
192.239.500.123 =\> 2.
[/output]
[/test]
[test]
[input]
IP=192.23.500.40 message='Hello&derps.' user=hello
IP=192.23.362.46 message='asdasdasd' user=greetings
IP=192.23.111.40 message='sdfsdfsd' user=bojo
IP=192.245.30.42 message='Hello&derps.' user=bojo
IP=192.254.345.42 message='Hello&derps.' user=fdgdfgdfgdf
IP=192.666.30.40 message='Aloha' user=hello
IP=192.999.30.44 message='asfdsfdsf' user=dsfdgdfg
IP=192.120.30.40 message='ggdsfdsfsd' user=zzzzzzzzzzz
IP=192.23.362.500 message='spampamapmapa' user=bbbbbbbb
IP=FE80:0000:0000:0000:0202:B3FF:FE1E:8329 message='yoooooo' user=aaaa
IP=192.23.30.642 message='heyooo' user=sdfsdf
IP=192.23.30.123 message='fgfgfgfgd' user=fgdfgdfgdfg
IP=192.232.245.545 message='grrrrrrrrr' user=mario
IP=192.231.123.59 message='aaaaaaaa' user=aaaaaaaaa
IP=192.231.467.40 message='aaaaaaaaa' user=destroyer
end
[/input]
[output]
aaaa: 
FE80:0000:0000:0000:0202:B3FF:FE1E:8329 =\> 1.
aaaaaaaaa: 
192.231.123.59 =\> 1.
bbbbbbbb: 
192.23.362.500 =\> 1.
bojo: 
192.23.111.40 =\> 1, 192.245.30.42 =\> 1.
destroyer: 
192.231.467.40 =\> 1.
dsfdgdfg: 
192.999.30.44 =\> 1.
fdgdfgdfgdf: 
192.254.345.42 =\> 1.
fgdfgdfgdfg: 
192.23.30.123 =\> 1.
greetings: 
192.23.362.46 =\> 1.
hello: 
192.23.500.40 =\> 1, 192.666.30.40 =\> 1.
mario: 
192.232.245.545 =\> 1.
sdfsdf: 
192.23.30.642 =\> 1.
zzzzzzzzzzz: 
192.120.30.40 =\> 1.
[/output]
[/test]
[test]
[input]
IP=192.23.500.40 message='Hello&derps.' user=hello
IP=192.23.362.46 message='asdasdasd' user=greetings
IP=192.23.111.40 message='sdfsdfsd' user=bojo
IP=192.245.30.42 message='Hello&derps.' user=bojo
IP=192.254.345.42 message='Hello&derps.' user=fdgdfgdfgdf
IP=192.666.30.40 message='Aloha' user=hello
IP=192.999.30.44 message='asfdsfdsf' user=dsfdgdfg
IP=192.120.30.40 message='ggdsfdsfsd' user=zzzzzzzzzzz
IP=192.23.362.500 message='spampamapmapa' user=bbbbbbbb
IP=192.234.30.666 message='yoooooo' user=aaaa
IP=192.23.30.642 message='heyooo' user=sdfsdf
IP=192.23.30.123 message='fgfgfgfgd' user=fgdfgdfgdfg
IP=192.232.245.545 message='grrrrrrrrr' user=mario
IP=192.231.123.59 message='aaaaaaaa' user=aaaaaaaaa
IP=192.231.467.40 message='aaaaaaaaa' user=destroyer
IP=192.23.500.40 message='Hello&derps.' user=hello
IP=192.23.362.46 message='asdasdasd' user=greetings
IP=192.23.111.40 message='sdfsdfsd' user=bojo
IP=192.245.30.42 message='Hello&derps.' user=bojo
IP=192.254.345.42 message='Hello&derps.' user=fdgdfgdfgdf
IP=192.666.30.40 message='Aloha' user=hello
IP=192.999.30.44 message='asfdsfdsf' user=dsfdgdfg
IP=192.120.30.40 message='ggdsfdsfsd' user=zzzzzzzzzzz
IP=192.23.362.500 message='spampamapmapa' user=bbbbbbbb
IP=192.234.30.666 message='yoooooo' user=aaaa
IP=192.23.30.642 message='heyooo' user=sdfsdf
IP=192.23.30.123 message='fgfgfgfgd' user=fgdfgdfgdfg
IP=192.232.245.545 message='grrrrrrrrr' user=mario
IP=192.231.123.59 message='aaaaaaaa' user=aaaaaaaaa
IP=192.231.467.40 message='aaaaaaaaa' user=destroyer
end
[/input]
[output]
aaaa: 
192.234.30.666 =\> 2.
aaaaaaaaa: 
192.231.123.59 =\> 2.
bbbbbbbb: 
192.23.362.500 =\> 2.
bojo: 
192.23.111.40 =\> 2, 192.245.30.42 =\> 2.
destroyer: 
192.231.467.40 =\> 2.
dsfdgdfg: 
192.999.30.44 =\> 2.
fdgdfgdfgdf: 
192.254.345.42 =\> 2.
fgdfgdfgdfg: 
192.23.30.123 =\> 2.
greetings: 
192.23.362.46 =\> 2.
hello: 
192.23.500.40 =\> 2, 192.666.30.40 =\> 2.
mario: 
192.232.245.545 =\> 2.
sdfsdf: 
192.23.30.642 =\> 2.
zzzzzzzzzzz: 
192.120.30.40 =\> 2.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]