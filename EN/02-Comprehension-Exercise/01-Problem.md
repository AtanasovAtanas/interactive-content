# Problem: Word Filter

[slide]
# Video

[vimeo-video]
[stream language="EN" videoId="435704899" default /]
[stream language="RO" videoId="436342716"  /]
[/video-vimeo]
[/slide]

[slide hideTitle]
# Problem: Word Filter
[code-task title="Problem: Word Filter" taskId="42bca445-e044-41e2-8b58-2605aa599bb5" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Using **comprehension**, write a program that receives some **strings** separated by **space** and take only those words, whose length is even.

Print each word on a new line.

## Examples
| **Input** | **Output** |
| --- | --- |
| kiwi orange banana apple | kiwi |
|  | orange |
|  | banana |
|  |  |

| **Input** | **Output** |
| --- | --- |
| pizza cake pasta chips | cake |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
kiwi orange banana apple
[/input]
[output]
kiwi
orange
banana
[/output]
[/test]
[test open]
[input]
pizza cake pasta chips
[/input]
[output]
cake
[/output]
[/test]
[test]
[input]
deal guide counter seat hobby
[/input]
[output]
deal
seat
[/output]
[/test]
[test]
[input]
deal guide counter seat hobby acute switch car widen criticism painter unfortunate pause boat
[/input]
[output]
deal
seat
switch
boat
[/output]
[/test]
[test]
[input]
photograph architect literature wardrobe hobby locate upset explosion extension favour gravel crutch misery resort leaf
[/input]
[output]
photograph
literature
wardrobe
locate
favour
gravel
crutch
misery
resort
leaf
[/output]
[/test]
[test]
[input]
adult visible strike dialect graduate issue bracket critical rest ignorant witness contract paint
[/input]
[output]
strike
graduate
critical
rest
ignorant
contract
[/output]
[/test]
[test]
[input]
adult visible strike dialect graduate issue bracket critical rest ignorant witness contract paint guerrilla jam diagram anticipation muggy rhetoric invite parade manage aid bank smooth native snub image injury real east storm sell
[/input]
[output]
strike
graduate
critical
rest
ignorant
contract
anticipation
rhetoric
invite
parade
manage
bank
smooth
native
snub
injury
real
east
sell
[/output]
[/test]
[/tests]
[/code-task]
[/slide]