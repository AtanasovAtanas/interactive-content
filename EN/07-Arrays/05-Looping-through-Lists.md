# Looping through Lists

[slide]
# For-Loop

There are two ways you can loop through a list using `for` loops.

One of them is to indices to access each element in the list.

This is done by using the `range()` function and passing the number of elements.

It will iterate from index 0 to the last valid one.

```python live
my_list = ["dog", "cat", "fish"]
for index in range(len(my_list)):
   print(my_list[index], end=" ") # dog cat fish 
```

The other way is to iterate over the elements.

Notice that using this way, indices are not needed because the loop iterates over the elements themselves, accessing them directly.

```python live
my_list = ["dog", "cat", "fish"]
for element in my_list:
   print(element, end=" ") # dog cat fish
```

[/slide]

[slide]
# While-Loop

The `while` loop can be used to iterate through a list too.

One way is by using the `pop()` function and iterating while there are still elements in the list.

```python live
my_list = ["dog", "cat", "fish"]
while len(my_list) > 0:
    print(my_list.pop(0), end=" ")
```

**Note:** It is recommended to always pop the first or last element of the list.

The way demonstrated above will leave the list empty.

You most likely don't want that to happen, so there is other way which won't remove any of the elements.

You'll need to keep track of the accessed index outside of the loop.

```python live
my_list = ["dog", "cat", "fish"]
index = 0
while index < len(my_list):
    print(my_list[index], end=" ")
    index += 1
```

[/slide]