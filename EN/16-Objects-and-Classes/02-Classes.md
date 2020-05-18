# Classes

[slide]
# Definition

A **class** is like a **blueprint** (or template) for creating **objects**.

Classes provide means of **bundling data and functionality** together.

Each class instance can have **attributes** attached to it.

Class instances can also have **methods** for **modifying its state**, they are its **behavior**.

Look at the example below, in the next slides it will be explained.

```python
class Person:
    def __init__(self, first_name, last_name, age=0):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age
```

[/slide]

[slide]
# The init function

All classes create objects, and all objects contain **characteristics** called **attributes**.

When an object is being initialized, the `__init__()` method of the class is automatically invoked and sets the object's attributes to their default values.

The double leading and trailing underscore ( `__` ) is used for **special variables** or **methods**.

[/slide]

[slide]
# The self Variable

The `self` parameter is a reference to the current **instance** of the class.

It is used to access variables that belong to the class.

When defining an **instance** method, the **first parameter** of the method should **always** be `self`.

[/slide]

[slide]
# Class Creation

The `class` keyword is used to create a class.

**Class attributes** are **same for all instances of the class**.

**Instance attributes** are **unique to each instance of the class**.

```python
class Cat:
    owner = 'Feral' # class attribute

    def __init__(self, name, age=0):
        self.name = name # instance attribute
        self.age = age # instance attribute
```

[/slide]