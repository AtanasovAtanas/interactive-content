# Dictionary Methods

[slide]
# clear()

The `clear()` method removes all pairs from a dictionary, makes it empty.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

grades.clear()

print(grades) # {}
```

[/slide]

[slide]
# copy()

The `copy()` method **returns** an **exact copy** of the dictionary.

Any **changes** made to the **copy** will **not** be applied to the **original dictionary** and vice versa.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}
grades_copy = grades.copy()

grades["Peter"] = 5.14
grades_copy["Jason"] = 3.22

print(grades) # {'Stephen': 4.55, 'Bellamy': 5.74, 'Amy': 5.22, 'Peter': 5.14}
print(grades_copy) # {'Stephen': 4.55, 'Bellamy': 5.74, 'Amy': 5.22, 'Jason': 3.22}
```

[/slide]

[slide]
# pop()

The `pop()` method **removes a pair** by **given key** from the dictionary and **returns** its **value**.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

stephen_grade = grades.pop('Stephen')

print(grades) # {'Bellamy': 5.74, 'Amy': 5.22}
print(stephen_grade) # 4.55
```

If such **key doesn't exist** in the dictionary, a `KeyError` is raised:

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

grade = grades.pop('inexistent')
```

[/slide]

[slide]
# popitem()

The `popitem()` method **removes the last inserted pair**.

**Returns** the pair as a **tuple**, both its **key** and **value**.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

last_grade = grades.popitem()

print(grades) # {'Stephen': 4.55, 'Bellamy': 5.74}
print(last_grade) # ('Amy', 5.22)
```

[/slide]