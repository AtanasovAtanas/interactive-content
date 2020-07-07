[slide hideTitle]
# Problem: Cat Catalog
[code-task title="Cat Catalog" taskId="750f758d-a8a6-479e-8d6e-0246f198c1ec" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
*The people from a pet shelter need to have a catalog of their cats with the breed and special characteristics.*

There are 3 special breeds of cats **"Siamese"**, **"Cymric"** and **"DomesticShorthair"**. 

**Each breed** has a special **characteristic**. 

For example, the special characteristic of the **Siamese** cats is their **ear size**, of **Cymric** cats - the **length of their fur** in millimeters and of the DomesticShorthair the **volume of their meowing**.

All the information about the cats, their breed and characteristics should be collected.

From the console you will receive lines of information about a cat until the command `End`.

The information will come in **one of** the following formats:

- `Siamese <name> <earSize>`
- `Cymric <name> <furLength>`
- `DomesticShorthair  <name> <meowingVolume>`

On the last line after the command `End` you will receive а **name** of a cat. 

You should print that cat and round the number of its s **two digits** after the decimal separator.

## Examples
| **Input** | **Output** |
| --- | --- |
| DomesticShorthair Kitty 85 | Cymric Tom 28.00 |
| Siamese Sim 4 |  |
| Cymric Tom 28 |  |
| End |  |
| Tom |  |

| **Input** | **Output** |
| --- | --- |
| DomesticShorthair Tom 80 | DomesticShorthair Kitty 100.00 |
| DomesticShorthair Kitty 100 |  |
| Cymric Tim 31 |  |
| End |  |
| Kitty |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
DomesticShorthair Kitty 85
Siamese Sim 4
Cymric Tom 28
End
Tom
[/input]
[output]
Cymric Tom 28.00
[/output]
[/test]
[test open]
[input]
DomesticShorthair Tom 80
DomesticShorthair Kitty 100
Cymric Tim 31
End
Kitty
[/input]
[output]
DomesticShorthair Kitty 100.00
[/output]
[/test]
[test]
[input]
Siamese Tony 5
Siamese Toncat 6
Siamese Antoan 5
Siamese Antony 5
Siamese Tonny 5
DomesticShorthair Kappa 95
Cymric Keepo 4.41
End
Toncat
[/input]
[output]
Siamese Toncat 6.00
[/output]
[/test]
[test]
[input]
DomesticShorthair Meow 90
DomesticShorthair Moow 91
DomesticShorthair Moew 92
Siamese Simon 5
Siamese Simmy 4
Cymric Kolly 3.20
Cymric Munny 2.30
End
Kolly
[/input]
[output]
Cymric Kolly 3.20
[/output]
[/test]
[test]
[input]
Cymric TommyTheCat 5.10
End
TommyTheCat
[/input]
[output]
Cymric TommyTheCat 5.10
[/output]
[/test]
[test]
[input]
DomesticShorthair Jerry 91
DomesticShorthair Was 92
DomesticShorthair A 93
DomesticShorthair Racecar 94
DomesticShorthair Driver 95
End
Jerry
[/input]
[output]
DomesticShorthair Jerry 91.00
[/output]
[/test]
[test]
[input]
DomesticShorthair Loly 61
Siamese Rony 4
Cymric Tommy 8.20
Cymric Dan 4.20
DomesticShorthair NoCat 1
DomesticShorthair CatCat 120
Cymric Wirehair 5.00
End
CatCat
[/input]
[output]
DomesticShorthair CatCat 120.00
[/output]
[/test]
[/tests]
[/code-task]
[/slide]