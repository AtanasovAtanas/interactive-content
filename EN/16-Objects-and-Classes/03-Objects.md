# Objects

[slide]
# Definition

An **instance** (object) is a copy of the class with **actual** values.

Objects encapsulate variables and methods **into a single entity**.

This is where we use the classes. Objects' **variables and methods are copied from the class**.

[/slide]

[slide]
# Object Initialization

Now that we know how to create a class, we can make use of it.

In order to do that, the `__init__()` method is used, **giving it parameters** if needed.

Just like normal functions, if a parameter is **optional**, we **don't** need to **pass** it when calling the function.

To **initialize** an object of the class, type the **class name** and pass the **parameters** in the **braces** after it:

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
cat_two = Cat('Purr')
```

[/slide]

[slide]
# Accessing Attributes

In order to access an attribute of the object directly, type the **variable name** plus **dot** ( `.` ) and the **attribute name**.

For better understanding, look at the example below, specifically where the **attributes are printed**:

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
cat_two = Cat('Purr')

print(cat_one.name)
print(cat_one.age)
print(cat_two.name)
print(cat_two.age)
```

[/slide]

[slide]
# Modifying Attributes

You can change the values of the attributes of an object after it's been initialized.

To do that, you have to access it and then give it a value, with the `=` operator.

```python live
class Cat:
    owner = 'Feral'

    def __init__(self, name, age=0):
        self.name = name
        self.age = age

cat_one = Cat('Baley', 7)
print(cat_one.name)
cat_one.name = 'Shady'
print(cat_one.name)
```

[/slide]