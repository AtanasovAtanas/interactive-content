[slide]
# Problem 1. Password Reset
[code-task title="Problem 1. Password Reset" taskId="e05c4cd7-f301-4a55-b976-941431c61753" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description

Write a password reset program that performs a series of commands upon a **predefined string**.

First, you will receive a string, and afterward, until the command `Done` is given, you will be receiving strings with **commands split by a single space**.

The commands will be the following:

- `TakeOdd`:

 Takes only the characters at **odd indices** and concatenates them together to obtain the **new raw password** and then prints it.

- `Cut {index} {length}`:

 Gets the substring with the **given length** starting from the given index from the password and removes its first occurrence of it, then prints the password on the console.

The given index and length will **always be valid**.

- `Substitute {substring} {substitute}`:

If the raw password **contains** the given substring, **replaces** all of its occurrences with the substitute text given and **prints** the result.

If **it doesn't**, prints `Nothing to replace!`

### Input

- You will be receiving strings until the `Done` command is given.

### Output

- After the `Done` command is received, print:

`Your password is: {password}`

### Constraints

- The indexes from the `Cut {index} {length}` command will always be valid.


## Examples
| **Input** | **Output** |
| --- | --- |
| Siiceercaroetavm\!:\?:ahsott.:i:nstupmomceqr  | icecream::hot::summer |
| TakeOdd | icecream::hot::mer |
| Cut 15 3 | icecream-hot-mer |
| Substitute :: \- | Nothing to replace! |
| Substitute \| \^ | Your password is: icecream-hot-mer |
| Done |  |

### Comments
S`i`i`c`e`e`r`c`a`r`o`e`t`a`v`m`\!`:`?`:`a`h`s`o`t`t`.`:`i`:`n`s`t`u`p`m`o`m`c`e`q`r` \-\> `icecream::hot::summer`

We only take the chars at odd indices 1, 3, 5 etc.

`Cut 15  3` \-\> icecream::hot::`sum`mer \-\> `sum`

`icecream::hot::mer`

We cut a substring starting at index `15` with length `3`, **remove** it from the raw password and **print it**.

Then, on a new line, we print the resulting new raw password.

`Substitute :: -` \-\> icecream`::`hot`::`summer \-\> icream`-`hot`-`summer

We replace `::` with `-`.

`Substitute | ^` \-\> `Nothing to replace!`

`|` is not found anywhere in the raw password.

Finally, after receiving the `Done` command, we **print** the resulting password in the proper format.


| **Input** | **Output** |
| --- | --- |
| up8rgoyg3r1atmlmpiunagt\!\-irs7!1fgulnnnqy | programming!is!funny |
| TakeOdd | programming!is!fun |
| Cut 18 2 | programming\*\*\*is\*\*\*fun |
| Substitute \! \*\*\* | Nothing to replace! |
| Substitute ? .!. | Your password is: programming\*\*\*is\*\*\*fun |
| Done |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Siiceercaroetavm!:?:ahsott.:i:nstupmomceqr 
TakeOdd
Cut 15 3
Substitute :: -
Substitute \| ^
Done
[/input]
[output]
icecream::hot::summer
icecream::hot::mer
icecream-hot-mer
Nothing to replace!
Your password is: icecream-hot-mer
[/output]
[/test]
[test open]
[input]
up8rgoyg3r1atmlmpiunagt!-irs7!1fgulnnnqy
TakeOdd
Cut 18 2
Substitute ! \*\*\*
Substitute ? .!.
Done
[/input]
[output]
programming!is!funny
programming!is!fun
programming\*\*\*is\*\*\*fun
Nothing to replace!
Your password is: programming\*\*\*is\*\*\*fun
[/output]
[/test]
[test]
[input]
abcd
TakeOdd
Done
[/input]
[output]
bd
Your password is: bd
[/output]
[/test]
[test]
[input]
abcdefg
TakeOdd
Done
[/input]
[output]
bdf
Your password is: bdf
[/output]
[/test]
[test]
[input]
abcdefg
TakeOdd
Cut 0 2
Done
[/input]
[output]
bdf
f
Your password is: f
[/output]
[/test]
[test]
[input]
abcdefg
TakeOdd
Substitute b y
Done
[/input]
[output]
bdf
ydf
Your password is: ydf
[/output]
[/test]
[test]
[input]
abcdefg
TakeOdd
Substitute z y
Done
[/input]
[output]
bdf
Nothing to replace!
Your password is: bdf
[/output]
[/test]
[test]
[input]
abcdefg
Cut 0 3
Done
[/input]
[output]
defg
Your password is: defg
[/output]
[/test]
[test]
[input]
abcdefg
Cut 0 6
Done
[/input]
[output]
g
Your password is: g
[/output]
[/test]
[test]
[input]
abcdefg
Cut 3 1
Done
[/input]
[output]
abcefg
Your password is: abcefg
[/output]
[/test]
[test]
[input]
abcdefg
Cut 4 2
Done
[/input]
[output]
abcdg
Your password is: abcdg
[/output]
[/test]
[test]
[input]
AABBCCDDEEFFGG
TakeOdd
Cut 2 3
Substitute B A
Done
[/input]
[output]
ABCDEFG
ABFG
AAFG
Your password is: AAFG
[/output]
[/test]
[test]
[input]
AAABBBCCCDDDEEEFFFGGG
Cut 0 1
Cut 0 1
Cut 0 1
Cut 1 1
Cut 3 2
Substitute G Y
TakeOdd
Done
[/input]
[output]
AABBBCCCDDDEEEFFFGGG
ABBBCCCDDDEEEFFFGGG
BBBCCCDDDEEEFFFGGG
BBCCCDDDEEEFFFGGG
BBCDDDEEEFFFGGG
BBCDDDEEEFFFYYY
BDDEFFY
Your password is: BDDEFFY
[/output]
[/test]
[test]
[input]
AAABBBCCCDDD
Cut 2 3
Substitute C J
Substitute Z M
TakeOdd
Done
[/input]
[output]
AABCCCDDD
AABJJJDDD
Nothing to replace!
AJJD
Your password is: AJJD
[/output]
[/test]
[/tests]
[/code-task]
[/slide]