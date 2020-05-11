# Searching in Lists

[slide]
# In Keyword

With the `in` keyword you can check **if an element is in a list**.

This is usually used with `if-else` statements.

```python live
my_list = [1, 2, 3, 4]
if 3 in my_list:
   print("The number 3 is in the list")
```

# Not in keywords

Combining the `in` keyword with the `not` one gives you the possibility to check if an element is **not** in a list.

Also usually used with `if-else` statements.

```python live
my_list = [1, 2, 3, 4]
if 5 not in my_list:
   print("The number 5 is not in the list")
```
[/slide]

[slide]
# Index of Element

The `index(element)` function is used to find at **which index an element is located**.

```python live
my_list = [1, 2, 3, 4]
print(my_list.index(2)) # 1
```

If there is **no such element** in the list, an `ValueError` will be raised.

[/slide]

[slide]
# Element Occurences

The `count(element)` function is used to get the **number of occurences of an element**.

```python live
my_list = [1, 2, 3, 4, 4, 4]
print(my_list.count(4)) # 3
print(my_list.count(7)) # 0
```

[/slide]