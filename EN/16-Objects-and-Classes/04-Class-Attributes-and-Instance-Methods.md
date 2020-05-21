# Class Attributes and Instance Methods

[slide]
# Class Attributes

While instance attributes are specific to each object, class attributes are the same for all instances.

Having that in mind, you have to be careful and avoid situations like this example:

```python live
class Cat:
    owner = 'Feral'
    fav_treats = []

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
cat_one.fav_treats.append('Seafood')
cat_one.fav_treats.append('Chicken')
cat_two = Cat('Jason')
print(cat_two.fav_treats)
print(cat_one.fav_treats)
```

Both `Cat` objects have the same favorite treats while they have been added only to `cat_one`.

It would be correct the `fav_treats` list to be an instance attribute instead:

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age
        self.fav_treats = []

cat_one = Cat('Baley', 7)
cat_one.fav_treats.append('Seafood')
cat_one.fav_treats.append('Chicken')
cat_two = Cat('Jason')
print(cat_two.fav_treats)
print(cat_one.fav_treats)
```

[/slide]

[slide]
# Instance Methods

**Instance methods** are defined **inside a class**. Like the `__init__()` method, the **first argument** should **always** be `self`.

They are used to get the **contents of an instance**.

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

    def get_info(self):
        return f'{self.name} is {self.age} years old.'

cat_one = Cat('Baley', 7)
print(cat_one.get_info())
```

They can also be used to perform **operations** with the **attributes** of the object.

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

    def adopt(self, owner_name):
        self.owner = owner_name

cat_one = Cat('Baley', 7)
cat_one.adopt('Michael')
print(cat_one.owner)
```

[/slide]

[slide]
# Problem: Email
[code-task title="Email" taskId="python-fundamentals-Objects-and-Classes-03" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Create **class Email**.

The \_\_init\_\_ method should receive **sender**, **receiver** and a **content**.

It should also have a **default** set to **False attribute** called **is_sent**.

The class should have two **additional methods**:

 - **send()** - sets the **is_sent** attribute to **True**
 - **get_info()** - returns the following string: "\{sender\} says to \{receiver\}: \{content\}. Sent: \{is_sent\}"

You will receive some emails until you receive "**Stop**" (separated by single space).

The first will be the **sender**, the second one – the **receiver** and the third one – the **content**.

On the final line you will be given the **indices** of the **sent emails** separated by **comma and space**.

Call the **send()** method for the given emails.

For each email call the **get_info()** method.

**Note:** Submit all of your code including the class.

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter John Hi,John | Peter says to John: Hi,John. Sent: True |
| John Peter Hi,Peter! | John says to Peter: Hi,Peter!. Sent: False |
| Katy Lilly Hello,Lilly | Katy says to Lilly: Hello,Lilly. Sent: True |
| Stop |  |
| 0, 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter John Hi,John
John Peter Hi,Peter!
Katy Lilly Hello,Lilly
Stop
0, 2
[/input]
[output]
Peter says to John: Hi,John. Sent: True
John says to Peter: Hi,Peter!. Sent: False
Katy says to Lilly: Hello,Lilly. Sent: True
[/output]
[/test]
[test]
[input]
a, b, hi
c, d, pesho
f, m, bye
Stop
0
[/input]
[output]
a, says to b,: hi. Sent: True
c, says to d,: pesho. Sent: False
f, says to m,: bye. Sent: False
[/output]
[/test]
[test]
[input]
pesho, gosho, hi
Stop
0
[/input]
[output]
pesho, says to gosho,: hi. Sent: True
[/output]
[/test]
[test]
[input]
a, b, c
e, f, g
h, i, j
k, l, m
Stop
1, 2
[/input]
[output]
a, says to b,: c. Sent: False
e, says to f,: g. Sent: True
h, says to i,: j. Sent: True
k, says to l,: m. Sent: False
[/output]
[/test]
[test]
[input]
a, b, c
e, f, h
Stop
1
[/input]
[output]
a, says to b,: c. Sent: False
e, says to f,: h. Sent: True
[/output]
[/test]
[test]
[input]
a, b, c
e, f, g
h, i, j
k, l, m
o, p, q
Stop
0, 1, 2, 3, 4
[/input]
[output]
a, says to b,: c. Sent: True
e, says to f,: g. Sent: True
h, says to i,: j. Sent: True
k, says to l,: m. Sent: True
o, says to p,: q. Sent: True
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Email
[code-task title="Email" taskId="7c4164f5-ef27-496a-9760-81330cb66ee4" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
class Email:
    def __init__(self, sender, receiver, content):
        self.sender = sender
        self.receiver = receiver
        self.content = content
        self.is_sent = False

    def send(self):
        self.is_sent = True

    def get_info(self):
        return f"{self.sender} says to {self.receiver}: {self.content}. Sent: {self.is_sent}"


emails = []

line = input()
while line != "Stop":
    tokens = line.split(" ")
    sender = tokens[0]
    receiver = tokens[1]
    content = tokens[2]
    email = Email(sender, receiver, content)
    emails.append(email)
    line = input()

send_emails = list(map(lambda x: int(x), input().split(", ")))

for x in send_emails:
    emails[x].send()

for email in emails:
    print(email.get_info())
```
[/code-editor]
[task-description]
## Description
Create **class Email**.

The \_\_init\_\_ method should receive **sender**, **receiver** and a **content**.

It should also have a **default** set to **False attribute** called **is_sent**.

The class should have two **additional methods**:

 - **send()** - sets the **is_sent** attribute to **True**
 - **get_info()** - returns the following string: "\{sender\} says to \{receiver\}: \{content\}. Sent: \{is_sent\}"

You will receive some emails until you receive "**Stop**" (separated by single space).

The first will be the **sender**, the second one – the **receiver** and the third one – the **content**.

On the final line you will be given the **indices** of the **sent emails** separated by **comma and space**.

Call the **send()** method for the given emails.

For each email call the **get_info()** method.

**Note:** Submit all of your code including the class.

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter John Hi,John | Peter says to John: Hi,John. Sent: True |
| John Peter Hi,Peter! | John says to Peter: Hi,Peter!. Sent: False |
| Katy Lilly Hello,Lilly | Katy says to Lilly: Hello,Lilly. Sent: True |
| Stop |  |
| 0, 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter John Hi,John
John Peter Hi,Peter!
Katy Lilly Hello,Lilly
Stop
0, 2
[/input]
[output]
Peter says to John: Hi,John. Sent: True
John says to Peter: Hi,Peter!. Sent: False
Katy says to Lilly: Hello,Lilly. Sent: True
[/output]
[/test]
[test]
[input]
a, b, hi
c, d, pesho
f, m, bye
Stop
0
[/input]
[output]
a, says to b,: hi. Sent: True
c, says to d,: pesho. Sent: False
f, says to m,: bye. Sent: False
[/output]
[/test]
[test]
[input]
pesho, gosho, hi
Stop
0
[/input]
[output]
pesho, says to gosho,: hi. Sent: True
[/output]
[/test]
[test]
[input]
a, b, c
e, f, g
h, i, j
k, l, m
Stop
1, 2
[/input]
[output]
a, says to b,: c. Sent: False
e, says to f,: g. Sent: True
h, says to i,: j. Sent: True
k, says to l,: m. Sent: False
[/output]
[/test]
[test]
[input]
a, b, c
e, f, h
Stop
1
[/input]
[output]
a, says to b,: c. Sent: False
e, says to f,: h. Sent: True
[/output]
[/test]
[test]
[input]
a, b, c
e, f, g
h, i, j
k, l, m
o, p, q
Stop
0, 1, 2, 3, 4
[/input]
[output]
a, says to b,: c. Sent: True
e, says to f,: g. Sent: True
h, says to i,: j. Sent: True
k, says to l,: m. Sent: True
o, says to p,: q. Sent: True
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Zoo
[code-task title="Zoo" taskId="python-fundamentals-Objects-and-Classes-04" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Create a **class Zoo**.

It should have a **class attribute** called \_\_animals that stores the **total count of the animals** in the zoo.

The \_\_init\_\_ method should only receive the **name** of the zoo.

There you should also create **3 empty lists (mammals, fishes, birds)**.

The class should also have **2 more methods**:

 - **add_animal(species, name)** - based on the species adds the name to the corresponding list
 - **get_info(species)** - based on the species returns a string in the following format: "\{Species\} in \{zoo_name\}: \{names\}" and on another line "Total animals: \{total_animals\}"

On the **first line** you will receive the **name** of the zoo.

On the **second line** you will receive number **n**.

On the next **n lines** you will receive animal info in the format: "\{species\} \{name\}".

**Add** the animal to the **zoo** to the **corresponding list**.

On the **final line** you will receive a **species**.

At the end, print all the info for that species and the total count of animals.

## Examples
| **Input** | **Output** |
| --- | --- |
| Great Zoo | Mammals in Great Zoo: lion, bear, tiger |
| 5 | Total animals: 5 |
| mammal lion |  |
| mammal bear |  |
| fish salmon |  |
| bird owl |  |
| mammal tiger |  |
| mammal |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Great Zoo
5
mammal lion
mammal bear
fish salmon
bird owl
mammal tiger
mammal
[/input]
[output]
Mammals in Great Zoo: lion, bear, tiger
Total animals: 5
[/output]
[/test]
[test]
[input]
Blah
1
mammal bear
mammal
[/input]
[output]
Mammals in Blah: bear
Total animals: 1
[/output]
[/test]
[test]
[input]
BB
1
fish fishy
fish
[/input]
[output]
Fishes in BB: fishy
Total animals: 1
[/output]
[/test]
[test]
[input]
P
2
bird b
bird c
bird
[/input]
[output]
Birds in P: b, c
Total animals: 2
[/output]
[/test]
[test]
[input]
Ka
3
mammal a
fish b
bird c
mammal
[/input]
[output]
Mammals in Ka: a
Total animals: 3
[/output]
[/test]
[test]
[input]
Baba
5
mammal a
mammal b
bird c
fish n
fish l
fish
[/input]
[output]
Fishes in Baba: n, l
Total animals: 5
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Zoo
[code-task title="Zoo" taskId="1f4c2321-ff1c-48ff-ae3d-d49d10811687" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
class Zoo:
    __animals = 0

    def __init__(self, name):
        self.name = name
        self.mammals = []
        self.fish = []
        self.birds = []

    def get_animals_by_species(self, species):
        animals = []
        if species == 'mammal':
            animals = self.mammals
        elif species == 'fish':
            animals = self.fish
        elif species == 'bird':
            animals = self.birds
        return animals

    def add_animal(self, species, animal):
        animals = self.get_animals_by_species(species)
        animals.append(animal)
        self.__animals += 1

    def get_info(self, species):
        animals = self.get_animals_by_species(species)
        if species == 'mammal':
            print(f'Mammals in {self.name}: {", ".join(animals)}')
        elif species == 'fish':
            print(f'Fishes in {self.name}: {", ".join(animals)}')
        elif species == 'bird':
            print(f'Birds in {self.name}: {", ".join(animals)}')
        # print(animals)
        print(f'Total animals: {self.__animals}')



zoo = Zoo(input())
animals_count = int(input())

for i in range(animals_count):
    [species, animal] = input().split()
    zoo.add_animal(species, animal)

species = input()
zoo.get_info(species)
```
[/code-editor]
[task-description]
## Description
Create a **class Zoo**.

It should have a **class attribute** called \_\_animals that stores the **total count of the animals** in the zoo.

The \_\_init\_\_ method should only receive the **name** of the zoo.

There you should also create **3 empty lists (mammals, fishes, birds)**.

The class should also have **2 more methods**:

 - **add_animal(species, name)** - based on the species adds the name to the corresponding list
 - **get_info(species)** - based on the species returns a string in the following format: "\{Species\} in \{zoo_name\}: \{names\}" and on another line "Total animals: \{total_animals\}"

On the **first line** you will receive the **name** of the zoo.

On the **second line** you will receive number **n**.

On the next **n lines** you will receive animal info in the format: "\{species\} \{name\}".

**Add** the animal to the **zoo** to the **corresponding list**.

On the **final line** you will receive a **species**.

At the end, print all the info for that species and the total count of animals.

## Examples
| **Input** | **Output** |
| --- | --- |
| Great Zoo | Mammals in Great Zoo: lion, bear, tiger |
| 5 | Total animals: 5 |
| mammal lion |  |
| mammal bear |  |
| fish salmon |  |
| bird owl |  |
| mammal tiger |  |
| mammal |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Great Zoo
5
mammal lion
mammal bear
fish salmon
bird owl
mammal tiger
mammal
[/input]
[output]
Mammals in Great Zoo: lion, bear, tiger
Total animals: 5
[/output]
[/test]
[test]
[input]
Blah
1
mammal bear
mammal
[/input]
[output]
Mammals in Blah: bear
Total animals: 1
[/output]
[/test]
[test]
[input]
BB
1
fish fishy
fish
[/input]
[output]
Fishes in BB: fishy
Total animals: 1
[/output]
[/test]
[test]
[input]
P
2
bird b
bird c
bird
[/input]
[output]
Birds in P: b, c
Total animals: 2
[/output]
[/test]
[test]
[input]
Ka
3
mammal a
fish b
bird c
mammal
[/input]
[output]
Mammals in Ka: a
Total animals: 3
[/output]
[/test]
[test]
[input]
Baba
5
mammal a
mammal b
bird c
fish n
fish l
fish
[/input]
[output]
Fishes in Baba: n, l
Total animals: 5
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Circle
[code-task title="Circle" taskId="python-fundamentals-Objects-and-Classes-05" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Create a **class Circle**.

In the \_\_init\_\_ method the circle should only receive **one parameter** (its diameter).

Create a **class attribute** called \_\_pi that is equal to **3.14**.

The class should also have the following methods:

 - **calculate_circumference()** - returns the circumference of the circle
 - **calculate_area()** - returns the area of the circle
 - **calculate_area_of_sector(angle)** - given the central angle in degrees, returns the area that fills the sector

On the **first line** you will receive the **circle diameter**.

On the **second line** you will receive the **central angle**.

Print the **result of each method formatted to the second decimal place** in the **order above**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 10 | 31.40 |
| 5 | 78.50 |
|  | 1.09 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
10
5
[/input]
[output]
31.40
78.50
1.09
[/output]
[/test]
[test]
[input]
15
3
[/input]
[output]
47.10
176.62
1.47
[/output]
[/test]
[test]
[input]
88
8
[/input]
[output]
276.32
6079.04
135.09
[/output]
[/test]
[test]
[input]
7
2
[/input]
[output]
21.98
38.47
0.21
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Circle
[code-task title="Circle" taskId="62971e4a-28ec-408a-9890-0acf3634f594" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
class Circle:
    __pi = 3.14

    def __init__(self, diameter = 0.0):
        self.radius = diameter/2
        self.diameter = diameter

    def calculate_circumference(self):
        return Circle.__pi * self.diameter
    def calculate_area(self):
        return Circle.__pi * self.radius * self.radius
    def calculate_area_of_sector(self, angle):
        return Circle.__pi * self.radius * self.radius * (angle/360)

circle = Circle(int(input()))
angle = int(input())
print(f"{circle.calculate_circumference():.2f}")
print(f"{circle.calculate_area():.2f}")
print(f"{circle.calculate_area_of_sector(angle):.2f}")
```
[/code-editor]
[task-description]
## Description
Create a **class Circle**.

In the \_\_init\_\_ method the circle should only receive **one parameter** (its diameter).

Create a **class attribute** called \_\_pi that is equal to **3.14**.

The class should also have the following methods:

 - **calculate_circumference()** - returns the circumference of the circle
 - **calculate_area()** - returns the area of the circle
 - **calculate_area_of_sector(angle)** - given the central angle in degrees, returns the area that fills the sector

On the **first line** you will receive the **circle diameter**.

On the **second line** you will receive the **central angle**.

Print the **result of each method formatted to the second decimal place** in the **order above**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 10 | 31.40 |
| 5 | 78.50 |
|  | 1.09 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
10
5
[/input]
[output]
31.40
78.50
1.09
[/output]
[/test]
[test]
[input]
15
3
[/input]
[output]
47.10
176.62
1.47
[/output]
[/test]
[test]
[input]
88
8
[/input]
[output]
276.32
6079.04
135.09
[/output]
[/test]
[test]
[input]
7
2
[/input]
[output]
21.98
38.47
0.21
[/output]
[/test]
[/tests]
[/code-task]
[/slide]