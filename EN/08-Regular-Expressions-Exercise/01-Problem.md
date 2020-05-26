[slide hideTitle]
# Problem: Furniture
[code-task title="Furniture" taskId="a0a7d9e4-1ed9-4ef9-86ab-d6161baeadc8" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program to **calculate the total cost** of different types of furniture.

You will be given some lines of input **until you receive the line** "Purchase". 

For the **line to be valid** it should be in the following **format**:
- ">>\{furniture name\}<<\{price\}!\{quantity\}"

The price can be a **floating-point number or a whole number**. 

Store the **names of the furniture and the total price**. 

At the end **print each bought furniture on a separate line** in the format:

"Bought furniture:

\{1st name\}

\{2nd name\}

…"

And **on the last line print** the following: 
- "Total money spent: \{spent money\}" **formatted** to the second decimal point.


### Example
| **Input** | **Output** |
| --- | --- |
| >>Sofa<<312.23!3 | Bought furniture: |
| >>TV<<300!5 | Sofa |
| >Invalid<<!5 | TV |
| Purchase | Total money spent: 2436.69 |

### Comments
- Only the Sofa and the TV are valid.
- For each of them we multiply the price by the quantity.
- Print the result.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
>>Sofa<<312.23!3
>>TV<<300!5
>Invalid<<!5
Purchase
[/input]
[output]
Bought furniture:
Sofa
TV
Total money spent: 2436.69
[/output]
[/test]
[test]
[input]
>>Televizor<<312.23!3
>>Monitor<<300!5
>>Invalid<<<<!5
>>Sink<<220!10
>>>>>>Invalid<<!5
Purchase
[/input]
[output]
Bought furniture:
Televizor
Monitor
Sink
Total money spent: 4636.69
[/output]
[/test]
[test]
[input]
>Invalid<<!5
>Invalid<<!5
>Invalid<<!5
Purchase
[/input]
[output]
Bought furniture:
Total money spent: 0.00
[/output]
[/test]
[test]
[input]
>>Sofa<<316.12!10
>>Couch<<31!12
>>Table<<31!12
>Masichka<<5
Purchase
[/input]
[output]
Bought furniture:
Sofa
Couch
Table
Total money spent: 3905.20
[/output]
[/test]
[test]
[input]
>>Sofa<<312.23!3
>>Sofa<<312.23!3
>>Sofa<<312.23!3
>>Sofa<<312.23!3
>>Sofa<<312.23!3
Purchase
[/input]
[output]
Bought furniture:
Sofa
Sofa
Sofa
Sofa
Sofa
Total money spent: 4683.45
[/output]
[/test]
[test]
[input]
>>Laptop<<312.2323!3
>>TV<<300.21314!5
>Invalid<<!5
>>TV<<300.21314!20
>>Invalid<!5
>>TV<<30.21314!5
>>Invalid<<!!5
Purchase
[/input]
[output]
Bought furniture:
Laptop
TV
TV
TV
Total money spent: 8593.09
[/output]
[/test]
[/tests]
[/code-task]
[/slide]