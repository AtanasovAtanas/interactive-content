[slide hideTitle]
# Problem: Pet Clinics
[code-task title="Pet Clinics" taskId="2a998846-89d5-4c6a-a557-c46c93631d52" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are a young and ambitious owner of a Pet Clinics Holding.

You ask your employees to create a program which will store all information about the pets in the database.

Each pet should have **name**, **age** and **kind**.


Your application should support a few basic operations such as **creating** a pet, **creating** a clinic, **adding** a pet to a clinic, **releasing** a pet from a clinic, **printing** information about a **specific** room in a clinic or printing information about **all** rooms in a clinic.

Clinics should have an **odd** number of rooms, attempting to create a clinic with an **even** number of should **fail** and **throw** an appropriate **exception**.

## Accommodation Order

For example, let us take a look at a clinic with 5 rooms. 

The **first** room where a pet will be treated is the **central** one (room 3). 

So the order of which an animal is entering is: the first animal is going to the **center** (3) room and after that the next pets are entering first to the **left** (2) and then to the **right** (4) room. 

The last rooms in which pets can enter are room 1 and room 5. 

In case a room is already occupied, we skip it and go to the next room in the above order. Your task is to model the application and make it support some commands.

The first pet enters room 3. -> 1 2 **3** 4 5

After that, the next pet enters room 2. -> 1 **2** 3 4 5

The third pet would enter room 4. -> 1 2 3 **4** 5

And the last two pets would be going to rooms - 1 and 5. -> **1** 2 3 4 **5**

Now when we have covered adding the pets, it is time to find a way to release them. 

The process of releasing them is not so simple when the release method is called, we start from the **center** room (3) and continue **right** (4, 5… and so on) until we find a pet or reach the **last** room. 

If we reach the last room, we start from the **first** (1) and again move right until we reach the ** center** room (3). 

If a pet is found, we **remove** it from the collection, stop the further search, and **return** `true`, if a pet is **NOT** found, the operation **returns** `false`.

When a print command for a room is called, if the room contains a pet we print the pet on a single line in the format `{pet name} {pet age} {pet kind}`. 

Alternatively, if the room is empty print **"Room empty"** instead. 

When a `Print` command for a clinic is called it should print **all** rooms in the clinic in **order** of their number.

### Commands

| **Command** | **Return Type** | **Description** |
| --- | --- | --- |
| `Create Pet {name} {age} {kind}` | void | Creates a pet with the specified name and age.(true if the operation is successful and false if it isn't) |
| Create Clinic \{name} \{rooms} | void | Creates a Clinic with the specified name and number of rooms.(if the rooms are not odd, throws an exception) |
| Add {pet's name} {clinic's name} | boolean | This command should add the given pet in the specified clinic.(true if the operation is successful and false if it isn't). |
| Release {clinic's name} | boolean | This command should release an animal from the specified clinic. (true if the operation is successful and false if it isn't). |
| HasEmptyRooms {clinic's name} | boolean | Returns whether the clinic has any empty rooms.(true if it has and false if it doesn't). |
| Print {clinic's name} | void | This command should print each room in the specified clinic, ordered by room number. |
| Print {clinic's name} {room} | void | Prints on a single line the content of the specified room. |

## Input

On the first line, you will be given an integer **N** - the number of commands you will receive. On each of the next **N** lines, you will receive a command. 

Commands and parameters will always be **correct** ( `Add`, `Release`, `HasEmptyRooms` and `Print` commands will always be passed to **existing** clinics/pets), except for the number of rooms in the **Create Clinic** command which can be any **valid** integer **between 1 and 101**.

## Output

For each command with a boolean **return** type received through the input, you should print its return value on a **separate** line. 

In case of a method **throwing** an **exception** (such as trying to create a clinic with even number of rooms or trying to add a pet that doesn't exist) you should **catch** the exceptions and instead, print `Invalid Operation!`. 

The Print command with a clinic and a room should print information for that room in the format **specified** above. 

The Print command with only a clinic should print information **for each** room in the clinic in **order** of their numbers.

## Constraints

- The number of commands **N** - will be a valid integer **between** [1 ... 1000], no need to check it explicitly.
- **Pet names** , **Clinic names** , and **kind** will be strings consisting only of alphabetical characters with length **between** [1 ... 50] characters.
- **Pet age** will be a positive integer **between** [1 ... 100].
- **Clinic rooms** will be a positive integer **between** [1 ... 101].
- **Room number** in a **Print** command will always be **between 1** and the **number of rooms** in that Clinic.
- Input will consist **only** of **correct commands** and they will **always** have the correct type of parameters.

## Examples
| **Input** | **Output** |
| --- | --- |
| 9 | Invalid Operation! |
| Create Pet Garet 7 Cat | true |
| Create Clinic VetClinic 4 | false |
| Create Clinic PetClinic 1 | true |
| HasEmptyRooms PetClinic | false |
| Release PetClinic | false |
| Add Garet PetClinic |  |
| HasEmptyRooms PetClinic |  |
| Create Pet Shabby 2 Dog |  |
| Add Shabby PetClinic |  |

| **Input** | **Output** |
| --- | --- |
| 8 | true |
| Create Pet Sherry 7 Cat | true |
| Create Pet Tom 1 Cata | Sherry 7 Cat |
| Create Clinic PetClinic 5 | true |
| Add Sherry PetClinic | Room empty |
| Add Tom PetClinic | Tom 1 Cata |
| Print PetClinic 3 | Room empty |
| Release PetClinic | Room empty |
| Print PetClinic | Room empty |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
9
Create Pet Garet 7 Cat
Create Clinic VetClinic 4
Create Clinic PetClinic 1
HasEmptyRooms PetClinic
Release PetClinic
Add Garet PetClinic
HasEmptyRooms PetClinic
Create Pet Shabby 2 Dog
Add Shabby PetClinic
[/input]
[output]
Invalid Operation!
true
false
true
false
false
[/output]
[/test]
[test open]
[input]
8
Create Pet Sherry 7 Cat
Create Pet Tom 1 Cata
Create Clinic PetClinic 5
Add Sherry PetClinic
Add Tom PetClinic
Print PetClinic 3
Release PetClinic
Print PetClinic
[/input]
[output]
true
true
Sherry 7 Cat
true
Room empty
Tom 1 Cata
Room empty
Room empty
Room empty
[/output]
[/test]
[test]
[input]
9
Create Pet Garet 8 Cat
Create Clinic VetClinic 4
Create Clinic PetClinic 1
HasEmptyRooms PetClinic
Release PetClinic
Add Garet PetClinic
HasEmptyRooms PetClinic
Create Pet Shabby 2 Dog
Add Shabby PetClinic
[/input]
[output]
Invalid Operation!
true
false
true
false
false
[/output]
[/test]
[test]
[input]
8
Create Pet Sherry 9 Cat
Create Pet Tom 1 Cata
Create Clinic PetClinic 5
Add Sherry PetClinic
Add Tom PetClinic
Print PetClinic 3
Release PetClinic
Print PetClinic
[/input]
[output]
true
true
Sherry 9 Cat
true
Room empty
Tom 1 Cata
Room empty
Room empty
Room empty
[/output]
[/test]
[test]
[input]
14
Create Pet Garet 7 Cat
Create Pet Sherry 1 Cat
Create Pet Shabby 3 Dog
Create Pet Tom 4 Cat
Create Pet Victor 17 Giraffe
Create Clinic PetClinic 5
Add Garet PetClinic
Add Sherry PetClinic
Add Shabby PetClinic
Add Tom PetClinic
Add Victor PetClinic
Release PetClinic
Release PetClinic
Print PetClinic
[/input]
[output]
true
true
true
true
true
true
true
Tom 4 Cat
Sherry 1 Cat
Room empty
Room empty
Victor 17 Giraffe
[/output]
[/test]
[test]
[input]
12
Create Pet Garet 7 Cat
Create Pet Sam 1 Cat
Create Pet Graf 100 Wolf
Create Clinic PetClinic 5
Add Garet PetClinic
Add Sam PetClinic
Add Graf PetClinic
Print PetClinic 3
Print PetClinic 1
Print PetClinic 2
Release PetClinic
Print PetClinic
[/input]
[output]
true
true
true
Garet 7 Cat
Room empty
Sam 1 Cat
true
Room empty
Sam 1 Cat
Room empty
Graf 100 Wolf
Room empty
[/output]
[/test]
[test]
[input]
11
Create Pet Doggy 1 Dog
Create Pet Cat 2 Cat
Create Pet Turtle 3 Turle
Create Pet Elephant 4 Elephant
Create Clinic Random 3
Create Clinic OtherRandom 17
Add Doggy Random
Add Cat Random
Add Elephant Random
Add Turtle Random
Print Random
[/input]
[output]
true
true
true
false
Cat 2 Cat
Doggy 1 Dog
Elephant 4 Elephant
[/output]
[/test]
[/tests]
[/code-task]
[/slide]