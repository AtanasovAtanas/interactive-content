# Sorting

[slide]
# sorted()

The `sorted()` method **sorts the elements** of a **given iterable** in **ascending** or **descending** order.

The syntax of the method is `sorted(iterable, [key], [reverse])`:
 - `iterable` - **sequence**, **collection** or **any iterator**; **required**
 - `key` - **function** that serves as a key for the **sort comparison**; **optional**
 - `reverse` - if **true**, the sorted collection is **reversed** (in **descending** order); **optional**

It **returns** a **sorted list** of the **given iterable object**.

By **default** the `sorted()` method **sorts** in **ascending** order.

**Strings** are sorted **alphabetically**.

**Numbers** are sorted **numerically**.

**Note:** A list that contains **both strings** and **numbers cannot** be **sorted**.

Sorting numbers example:

```python live
numbers = [2, 5, 7, 1, -8, 0]
sorted_numbers = sorted(numbers)
descending_sorted_numbers = sorted(numbers, reverse=True)

print(numbers) # [2, 5, 7, 1, -8, 0]
print(sorted_numbers) # [-8, 0, 1, 2, 5, 7]
print(descending_sorted_numbers) # [7, 5, 2, 1, 0, -8]
```

Sorting strings example:

```python live
names = ["Eric", "Alice", "Peter", "Zed"]
sorted_names = sorted(names)
descending_sorted_names = sorted(names, reverse=True)

print(names) # ['Eric', 'Alice', 'Peter', 'Zed']
print(sorted_names) # ['Alice', 'Eric', 'Peter', 'Zed']
print(descending_sorted_names) # ['Zed', 'Peter', 'Eric', 'Alice']
```

[/slide]

[slide]
# Using Lambda Functions

**Lambda functions** can be used in the `sorted()` method.

The `key` parameter is the one that **accepts** the **lambda function**.

Passing a **lambda function** allows you to **sort** the elements in a **custom way**.

Example:

```python live
people_ages = {'Annie': 21, 'George': 18, 'John': 45}
sorted_by_name = dict(sorted(people_ages.items(), key=lambda x: x[0]))
sorted_by_age = dict(sorted(people_ages.items(), key=lambda x: x[1]))

print(sorted_by_name) # {'Annie': 21, 'George': 18, 'John': 45}
print(sorted_by_age) # {'George': 18, 'Annie': 21, 'John': 45}
```

In the example above, there is a dictionary that consists of **names** of people (**keys**) and their **age** (**values**).

The **lambda function** tells the `sorted()` method to sort the dictionary by **index**.

The `x[0]` means to sort the dictionary by **keys** (because **keys** are **first**, they are at **index 0**).

The `x[1]` means to sort the dictionary by **values** (because **values** are **second**, they are at **index 1**).

Another more complex example:

```python live
class Person:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

people = [Person("Xin", "Chang", 17),
          Person("Nicholas", "Grey", 24),
          Person("Amy", "Willson", 20)]

people = sorted(people, key=lambda x: x.first_name)

for person in people:
    print(f"{person.first_name} {person.last_name} is {person.age} years old.")
```

In this one, there is a **class** `Person` and **list of objects** of it.

The sort there is by `Person`'s `first_name`.

Probably you can already guess that it can be sorted by `last_name` and `age`.

**Note:** If you **don't specify** how a **list of custom objects** to be sorted, the `sorted()` method **raises an error**.

```python live
class Person:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

people = [Person("Xin", "Chang", 17),
          Person("Nicholas", "Grey", 24),
          Person("Amy", "Willson", 20)]

people = sorted(people)

for person in people:
    print(f"{person.first_name} {person.last_name} is {person.age} years old.")
```

[/slide]