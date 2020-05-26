# Creating Lists

[slide]
# Ways to Create a List

There are two ways to create a list:
 - Initialize it with square brackets, if no elements are declared, the list will be empty
```python
empty_list = []
my_list = [1, 2, 3]
```
 - Initialize it with the `list([iterable])` function.
 - The `[iterable]` argument is optional. If it isn't given, the list will be empty, otherwise - it will consist of the elements of the iterable.
```python
empty_list = list()
my_list = list('hey') # this is equal to my_list = ['h', 'e', 'y']
```
[/slide]

[slide]
# Splitting Strings to List

A list can be created by splitting strings.

Use the `split()` function over a string and it will create a list.

The `split()` function accepts a **parameter**, that defines by what it will split the string, a **separator**.

```python
some_text = "a!b!c!d"
my_list = some_text.split("!") # ["a", "b", "c", "d"]
```

In case you don't specify the separator, the function will try to split the string by spaces. See the example below:

```python
some_text = "hello, my name is Stephen."
my_list = some_text.split() # ['hello,', 'my', 'name', 'is', 'Stephen.']
```

The separator can be a whole string, not only a single character.

```python
some_text = "How separate are separate you"
my_list = some_text.split("separate")) # ['How ', ' are ', ' you']
```

[/slide]

[slide]
# Joining Lists into a String

Not only can a string be turned into a list, but a **list** can be **joined into** a **string** too.

This is possible thanks to the `join()` function.

The result of this function is **always** a string.

It **must** be used **on a string** that acts as a **separator** and the **list** that you want to turn into a string, is given as a **parameter between the braces**.

See the example for better understanding:

```python live
my_list = ["a", "b", "c"]
my_list_to_string = "-".join(my_list)
print(my_list_to_string)
```

**Note:** The `join()` function **cannot** be used on anything other than **strings**. If you try joining a list that doesn't contain only strings, an error will be caused.

```python live
my_list = [1, 2, 3]
my_list_to_string = "-".join(my_list)
```

[/slide]