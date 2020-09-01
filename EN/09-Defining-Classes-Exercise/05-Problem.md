[slide hideTitle]
# Problem: Pokemon Trainer
[code-task title="Pokemon Trainer" taskId="557a0bbb-06f1-4916-aa67-034874e07cbd" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You wanna be the very best pokemon trainer, like no one ever was, so you set out to catch pokemon.

Define a class **Trainer** and a class **Pokemon**.

Trainer has a **name**, **number of badges** and a **collection of pokemon**.

Pokemon has a **name**, an **element** and **health**, all values are **mandatory**.

Every Trainer **starts with 0 badges**.

From the console you will receive an unknown number of lines until you receive the command `Tournament`. 

Each line will carry information about a pokemon and the trainer who caught it in the format:

`<trainerName> <pokemonName> <pokemonElement> <pokemonHealth>` 

Where **trainerName** is the name of the Trainer who caught the pokemon. 

Names are **unique**, there can not be 2 trainers with the same name. 

After receiving the command `Tournament` an unknown number of lines containing one of three elements **"Fire"**, **"Water"**, **"Electricity"** will follow until the command `End` is received. 

For every command you must check if a trainer has **at least 1** pokemon with the given element. 

If he does, he receives 1 badge, otherwise all his pokemon **lose 10 health**. 

If a pokemon falls **to 0 or less health he dies** and must be deleted from the trainer's collection. 

After the command `End` is received you should print all trainers **sorted by the number of badges they have in descending order**. 

If two trainers have the same amount of badges they should be sorted by order of appearance in the input. 

Print in the format:

`<trainerName> <badges> <numberOfPokemon>`

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter Charizard Fire 100 | Peter 2 2 |
| John Squirtle Water 38 | John 0 1 |
| Peter Pikachu Electricity 10 |  |
| Tournament |  |
| Fire |  |
| Electricity |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| Stan Blastoise Water 18 | Nick 1 1 |
| Nick Pikachu Electricity 22 | Stan 0 0 |
| John Kadabra Psychic 90 | John 0 1 |
| Tournament |  |
| Fire |  |
| Electricity |  |
| Fire |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter Charizard Fire 100
John Squirtle Water 38
Peter Pikachu Electricity 10
Tournament
Fire
Electricity
End
[/input]
[output]
Peter 2 2
John 0 1
[/output]
[/test]
[test open]
[input]
Stan Blastoise Water 18
Nick Pikachu Electricity 22
John Kadabra Psychic 90
Tournament
Fire
Electricity
Fire
End
[/input]
[output]
Nick 1 1
Stan 0 0
John 0 1
[/output]
[/test]
[test]
[input]
P Charizard Fire 100
G Squirtle Water 38
P Pikachu Electricity 10
M Balbazor Fire 101
Tournament
End
[/input]
[output]
P 0 2
G 0 1
M 0 1
[/output]
[/test]
[test]
[input]
P Charizard Fire 100
G Squirtle Water 38
P Pikachu Electricity 10
P Balbazor Electricity 102
G Buterfree Fire 11
Tournament
End
[/input]
[output]
P 0 3
G 0 2
[/output]
[/test]
[test]
[input]
P Charizard Fire 100
M MiniCharizard Fire 50
P BigCharizard Fire 120
P FirePokemon Fire 101
M Char Fire 100
J Turtle Water 100
J BigTurtle Water 250
Tournament
Fire
Fire
Fire
Fire
End
[/input]
[output]
P 4 3
M 4 2
J 0 2
[/output]
[/test]
[test]
[input]
G Golem Water 102
P Charizard Water 100
M MiniCharizard Water 50
P BigCharizard Water 120
P FirePokemon Water 101
M Char Fire 100
J Turtle Electricity 100
J BigTurtle Fire 250
Tournament
Water
Water
Water
Water
Water
Water
End
[/input]
[output]
G 6 1
P 6 3
M 6 2
J 0 2
[/output]
[/test]
[test]
[input]
G Golem Water 102
P Charizard Water 100
M MiniCharizard Water 50
P BigCharizard Water 120
P FirePokemon Water 101
M Char Electricity 100
J Turtle Electricity 100
J BigTurtle Fire 250
Tournament
Electricity
Electricity
Electricity
Electricity
End
[/input]
[output]
M 4 2
J 4 2
G 0 1
P 0 3
[/output]
[/test]
[test]
[input]
G Golem Water 102
P Charizard Water 100
M MiniCharizard Water 30
P BigCharizard Water 120
P FirePokemon Water 101
M Char Electricity 100
J Turtle Electricity 100
J BigTurtle Water 250
Tournament
Fire
Fire
Fire
Fire
Fire
End
[/input]
[output]
G 0 1
P 0 3
M 0 1
J 0 2
[/output]
[/test]
[test]
[input]
G Golem Fire 102
P Charizard Fire 100
M MiniCharizard Fire 30
P BigCharizard Fire 120
P FirePokemon Electricity 101
M Char Electricity 100
J Turtle Electricity 10
J BigTurtle Fire 25
Tournament
Water
Water
Water
Water
Water
Water
Water
End
[/input]
[output]
G 0 1
P 0 3
M 0 1
J 0 0
[/output]
[/test]
[test]
[input]
G Golem Fire 102
P Charizard Fire 100
M MiniCharizard Fire 30
P BigCharizard Fire 120
P FirePokemon Water 11
M Char Water 10
J Turtle Fire 10
J BigTurtle Fire 2500
Tournament
Electricity
Electricity
Electricity
Electricity
Electricity
End
[/input]
[output]
G 0 1
P 0 2
M 0 0
J 0 1
[/output]
[/test]
[test]
[input]
An Balbazor Water 100
A Pikachu Electricity 100
Annie Squirtal Fire 100
P Balbazor Water 100
P Electricity Electricity 100
P Balbazor2 Fire 100
Tournament
Fire
Water
Electricity
End
[/input]
[output]
P 3 3
An 1 1
A 1 1
Annie 1 1
[/output]
[/test]
[test]
[input]
S Blastoise Water 18
N Pikachu Electricity 22
N Pikachu2 Electricity 200
N Pikachu3 Electricity 21
N Pikachu4 Electricity 23
N Pikachu5 Electricity 230
J Kadabra Psychic 90
S Squirtle Water 1200
P TurtoiseSVN Water 500
P Charizard Water 50
G Flower Fire 10
Tournament
Electricity
Fire
Water
Fire
Electricity
Fire
Water
Electricity
Electricity
Water
Water
Water
Water
Electricity
Fire
Fire
End
[/input]
[output]
S 6 1
P 6 1
N 5 2
J 0 0
G 0 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]