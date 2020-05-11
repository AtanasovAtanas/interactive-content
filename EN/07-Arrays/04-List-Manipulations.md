# List Manipulations

[slide]
# Add Elements

We can add an element to the **end of the list** with the `append([element])` function.

```python live
my_list = [1, 2, 3]
my_list.append(4)
print(my_list) # [1, 2, 3, 4]
```

To add an element to a **specific index**, use the `insert(index, element)` function.

The first parameter is the index and the second - the element to be added.

```python live
my_list = [1, 3, 4]
my_list.insert(1, 2)
print(my_list) # [1, 2, 3, 4]
```

There is also a way to **merge two lists**.

This is done by using the `extend(list)` function.

**All** of the elements of the list **given as a parameter** will be appended to the **end** of the list that this function is being **executed over**.

```python live
my_list = [1, 2, 3]
my_list.extend([4, 5, 6])
print(my_list)
```

[/slide]

[slide]
# Remove Elements

To remove an element from a list, the function `remove(element)` can be used.

It removes the **first occurence** of the element given in the braces.

If such element **doesn't exist** in the list, a `ValueError` will be raised.

```python live
my_list = [1, 2, 3, 2]
my_list.remove(2)
print(my_list) # [1, 3, 2]
```

To remove **all** elements of a list, use the `clear()` function.

```python live
my_list = [1, 2, 3]
my_list.clear()
print(my_list) # []
```

There is also a way to remove an element at a **given index**, which also **returns** it.

For this purpose, the `pop([index])` function is used.

**Note:** The parameter `index` is between **square brackets**, it means that the parameter is **optional**. If **no index** is passed as a parameter, the function will remove (and return) the **last** element of the list.

```python live
my_list = [1, 2, 3, 4, 5, 6]
print(my_list.pop(2)) # 3
print(my_list.pop()) # 6
print(my_list) # [1, 2, 4, 5]
```

[/slide]