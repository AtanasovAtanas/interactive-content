# Existence in Dictionaries

[slide]
# Check for Key Existence

Just like with lists, we can use the `in` keyword to check if a key is persistent in a dictionary.

The `not` keyword can be paired with `in` in order to check if a key isn't contained in a dictionary.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

if 'Stephen' in grades:
    print('Persistent.')

if 'Jason' not in grades:
    print('Not persistent')
```

You can use the `keys()` method although it isn't necessary, the result is the same:

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

if 'Stephen' in grades.keys():
    print('Persistent.')

if 'Jason' not in grades.keys():
    print('Not persistent')
```

By **default** when checking **directly the dictionary variable**, it checks the **keys**, not the values.

[/slide]

[slide]
# Check for Value Existence

To check if a **value** is **contained** in a dictionary, you **must** use the `values()` method, otherwise you'd be checking the **keys**.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

if 4.55 in grades.values():
    print('Persistent.')

if 4.56 not in grades.values():
    print('Not persistent')
```

[/slide]