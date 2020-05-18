# Class Attributes and Instance Methods

[slide]
# Class Attributes

While instance attributes are sepcific to each object, class attributes are the same for all instances.

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

**Instance methods** are defined **inside a class**. Like the `__init__()` method, the **first argument** should **always** be `self`

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