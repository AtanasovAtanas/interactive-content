# Keys and Values

[slide]
# Key Definition

While **list** uses **indexing** to access values, **dictionary** uses **keys**.

A **key** can be used either **inside square brackets** or with the `get()` method.

```python live
my_dict = {'cat': 'meow'}

print(my_dict['cat'])
print((my_dict.get('cat')))
```

**Note:** The difference when using `get()` is that it returns `None` instead of raising `KeyError` if the key is not found.

```python live
my_dict = {'cat': 'meow'}

print((my_dict.get('dog')))
```

```python live
my_dict = {'cat': 'meow'}

print(my_dict['dog'])
```

[/slide]

[slide]
# Values

Dictories are **mutable**.

Using the **assignment operator** ( `=` ) **new pairs can be added** or the **value of already existing** can be **changed**.

If the **key** is **already present**, the **value** gets **updated**, **otherwise** a **new pair is added** to the dictionary.

Adding a new pair:

```python live
my_dict = {"name": "Jason", "age": 20}
my_dict["job"] = "Software developer"
print(my_dict["job"])
```

Updating value:

```python live
my_dict = {"name": "Jason", "age": 20}
my_dict["age"] = 22
print(my_dict["age"])
```

[/slide]