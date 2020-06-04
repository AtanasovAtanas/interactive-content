[slide]
# Problem 2. Emoji Detector
[code-task title="Problem 2. Emoji Detector" taskId="04713618-24c3-4523-aea6-0a6df0e8be05" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Your task is to write a program which extracts emojis from a text and find the threshold based on the input.

You have to get your **cool threshold**.

It is obtained by multiplying all the digits found in the input.

The cool threshold could be a **very big number**, so be mindful.

An emoji is valid when:

- Is surrounded by either `::` or `**` (exactly 2)

- Is **at least 3** characters long (**without** the surrounding symbols)

- **Starts** with a **capital letter**

- Continues with **lowercase** letters **only**

- Examples of valid emojis: `::Joy::`, `**Banana**`, `::Wink::`

- Examples of **invalid** emojis: \:\:Joy\*\*, \:\:fox:es\:, \*\*Monk3ys\*\*, \:Snak\:\:Es\:\:

You need to count **all valid emojis** in the text and calculate their **coolness**.

The coolness of the emoji is **determined** by summing all the **ASCII values of all letters** in the emoji.

- Examples: \:\:`Joy`\:\: - 306, \*\*`Banana`\*\* - 577, \:\:`Wink`\:\: - 409

You need to print the result of the cool threshold and after that to take all emojis out of the text, count them and print the **only the cool ones** on the console.

### Input

- On the single input, you will receive a piece of string.

### Output

- On the first line of the output print the obtained Cool threshold in format:

`Cool threshold: {coolThresholdSum}`

- On the next line print the count of all emojis found in the text in format:

`{countOfAllEmojis}` **emojis found in the text. The cool ones are**:

`{cool emoji 1}`

`{cool emoji 2}`

`{…}`

If there are **no cool ones**, just don't print anything in the end.

### Constraints

There will always be at least one digit in the text!


## Examples
| **Input** | **Output** |
| --- | --- |
| In the Sofia Zoo there are **311** animals in total\! `::Smiley::` This includes **3** `**Tigers**`, **1** \:\:Elephant\:, **12** \*\*Monk3ys\*\*, a \*\*Gorilla\:\:, **5** \:\:fox\:es\: and **21** different types of \:Snak\:\:Es\:\:\. `::Mooning::` `**Shy**` | Cool threshold: 540 |
|  | 4 emojis found in the text. The cool ones are: |
|  | \:\:Smiley\:\:  |
|  | \*\*Tigers\*\*  |
|  | \:\:Mooning\:\: |
|  |  |

### Comments

You can see all the valid emojis are marked.

There are various reasons why the rest are `not valid`, examine them carefully.

The **cool threshold** is 3\*1\*1\*3\*1\*1\*2\*3\*5\*2\*1 = 540.

`::Smiley::` -\> 83 + 109 + 105 + 108 + 101 + 121 = 627 \> 540 -\> **cool**

`**Tigers**` -\> 84 + 105 + 103 + 101 + 114 + 115 = 622 \> 540 -\> **cool**

`::Mooning::` -\> 77 + 111 + 111 + 112 + 105 + 112 + 103 = 727 \> 540 -\> **cool**

`**Shy**` \-\> 83 + 104 + 121 = 308 \< 540 \-\> not cool

At the end we print the count of all valid emojis found and each of the cool ones on a new line.


| **Input** | **Output** |
| --- | --- |
| 5, 4, 3, 2, 1, go\! The 1\-th consecutive banana\-eating contest has begun\! \:\:Joy:: \*\*Banana\*\* \:\:Wink\:\: \*\*Vali\*\* \:\:valid_emoji\:\: | Cool threshold: 120 |
|  | 4 emojis found in the text. The cool ones are: |
|  | \:\:Joy\:\: |
|  | \*\*Banana\*\* |
|  | \:\:Wink\:\: |
|  | \*\*Vali\*\* |
|  |  |

| **Input** | **Output** |
| --- | --- |
| It is a long fact that 1 a reader will be distracted by 9 the readable content of a page when looking at its layout. The point of using \:\:LoremIpsum\:\: is that it has a more-or-less normal 3 distribution of 8 letters, as opposed to using 'Content here, content 99 here', making it look like readable `**English**`. | Cool threshold: 17496 |
|  | 1 emojis found in the text. The cool ones are: |

### Comments

You can see `**English**` is a valid emoji, but the sum of ascii is not bigger than cool threshold, that's why we don't print anything in the end.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
In the Sofia Zoo there are 311 animals in total! \:\:Smiley\:\: This includes 3 \*\*Tigers\*\*, 1 \:\:Elephant\:, 12 \*\*Monk3ys\*\*, a \*\*Gorilla\:\:, 5 \:\:fox\:es\: and 21 different types of \:Snak\:\:Es\:\:. \:\:Mooning\:\: \*\*Shy\*\*
[/input]
[output]
Cool threshold: 540
4 emojis found in the text. The cool ones are:
\:\:Smiley\:\:
\*\*Tigers\*\*
\:\:Mooning\:\:
[/output]
[/test]
[test open]
[input]
5, 4, 3, 2, 1, go! The 1-th consecutive banana-eating contest has begun! \:\:Joy\:\: \*\*Banana\*\* \:\:Wink\:\: \*\*Vali\*\* \:\:valid_emoji\:\:
[/input]
[output]
Cool threshold: 120
4 emojis found in the text. The cool ones are:
\:\:Joy\:\:
\*\*Banana\*\*
\:\:Wink\:\:
\*\*Vali\*\*
[/output]
[/test]
[test open]
[input]
It is a long established fact that 1 a reader will be distracted by 9 the readable content of a page when looking at its layout. The point of using \:\:LoremIpsum\:\: is that it has a more-or-less normal 3 distribution of 8 letters, as opposed to using 'Content here, content 99 here', making it look like readable \*\*English\*\*.
[/input]
[output]
Cool threshold: 17496
1 emojis found in the text. The cool ones are:
[/output]
[/test]
[test]
[input]
Test text 1 ... \*\*Done\*\*!
[/input]
[output]
Cool threshold: 1
1 emojis found in the text. The cool ones are:
\*\*Done\*\*
[/output]
[/test]
[test]
[input]
Test text 3 2 ... "\:\:Testone\:\:"!
[/input]
[output]
Cool threshold: 6
1 emojis found in the text. The cool ones are:
\:\:Testone\:\:
[/output]
[/test]
[test]
[input]
2\:\:cat\:\:2 2\*\*Me\*\*2 2\:\:Anteater\:\:2 2\*\*D0g\*\*2 2\:\*Thisisatrickyone\:\*2 2\*Bumblebee\*2 2\:\:Koala\*\*2
[/input]
[output]
Cool threshold: 0
1 emojis found in the text. The cool ones are:
\:\:Anteater\:\:
[/output]
[/test]
[test]
[input]
\:\:Fubar\:\: 1
[/input]
[output]
Cool threshold: 1
1 emojis found in the text. The cool ones are:
\:\:Fubar\:\:
[/output]
[/test]
[test]
[input]
\*\*Xxxxxx\*\* 253 \:\:Yyy\:\: 148 \*\*Zzzzzz\*\*
[/input]
[output]
Cool threshold: 960
3 emojis found in the text. The cool ones are:
[/output]
[/test]
[test]
[input]
2 \*\*Cool\*\* \:\:Verycool\:\: \*\*Megacool\*\* \:\:Gigacool\:\: \*\*Ultracool\*\* 2
[/input]
[output]
Cool threshold: 4
5 emojis found in the text. The cool ones are:
\*\*Cool\*\*
\:\:Verycool\:\:
\*\*Megacool\*\*
\:\:Gigacool\:\:
\*\*Ultracool\*\*
[/output]
[/test]
[test]
[input]
473\:\:Wtf\:\:82\:\:Wow\:\:\*\*Great\*\*07
[/input]
[output]
Cool threshold: 0
3 emojis found in the text. The cool ones are:
\:\:Wtf\:\:
\:\:Wow\:\:
\*\*Great\*\*
[/output]
[/test]
[test]
[input]
Th3\:\:Quick\:\:brown\*\*Fox\*\*jumped\#over@the\:\:Lazy\:\:\:\:Dog\:\:654times!
[/input]
[output]
Cool threshold: 360
4 emojis found in the text. The cool ones are:
\:\:Quick\:\:
\:\:Lazy\:\:
[/output]
[/test]
[test]
[input]
I`ve really gotta \:\*Come\:\* up with some \*\*Fancy\*\*\:\:@ss\:\:\*\*Logic\*\*to\:\:Put:\*\*In\*\*\:\:HerE\:\:... Well,there\*\*You\:\:have\:it.69\*\*Ti_mes\*\*out_of_71_it_is\:\:Easy\:\:but-not\*\*Now\*\*!
[/input]
[output]
Cool threshold: 378
4 emojis found in the text. The cool ones are:
\*\*Fancy\*\*
\*\*Logic\*\*
\:\:Easy\:\:
[/output]
[/test]
[test]
[input]
I've really gotta \:\*Come\:\* up with some \*\*Fancy\*\*\:\:@ss\:\:\*\*Logic\*\*to\:\:Put\:\*\*In\*\*\:\:HerE\:\:\.\.\. Well,there\*\*You\:\:have\:it.222222\*\*Ti_mes\*\*out_of_2222_it_is\:\:Easy\:\:but-not\*\*Now\*\*!\*\*Wzzzzzzzzzzzzzzzz\*\*\:\:Zwwwwwwwwwwwwww\:\:
[/input]
[output]
Cool threshold: 1024
6 emojis found in the text. The cool ones are:
\*\*Wzzzzzzzzzzzzzzzz\*\*
\:\:Zwwwwwwwwwwwwww\:\:
[/output]
[/test]
[/tests]
[/code-task]
[/slide]