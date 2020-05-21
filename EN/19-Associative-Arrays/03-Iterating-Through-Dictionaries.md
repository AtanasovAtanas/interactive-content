# Iterating Through Dictionaries

[slide]
# Iterating Through Keys

You can **get all the keys** of a dictionary with the `keys()` method.

Doing this allows you to **iterate through all of them**.

Accessing keys:

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

for key in grades.keys():
   print(key, end=" ")
```

Accessing values by key:

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

for key in grades.keys():
   print(grades[key], end=" ")
```

Changing values by iterating through the keys:

```python live
grades = {"Stephen": 2.55, "Bellamy": 2.74, "Amy": 2.22}

for key in grades.keys():
   grades[key] *= 2

print(grades)
```

[/slide]

[slide]
# Iterating Through Values

There is an **easier way** to **access all values** of a dictionary.

Use the `values()` method to **get all the values**.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

for value in grades.values():
   print(value, end=" ")
```

[/slide]

[slide]
# Iterating Through Pairs

Use the `items()` method to **iterate through key-value pairs**.

It returns **tuple** (**key**, **value**) **pairs**.

You will learn about **tuples** in the following courses.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

for (key, value) in grades.items():
    print(f"{key}'s grade is {value}")
```

[/slide]