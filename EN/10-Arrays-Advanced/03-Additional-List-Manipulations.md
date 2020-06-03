# Additional List Manipulations

[slide]
# Swapping List Elements

You can use the syntax in the example below in order to **swap as many as you wish list elements**:

```python live
numbers = [3, 5, 7]
numbers[0], numbers[1], numbers[2] = numbers[2], numbers[0], numbers[1]
print(numbers) # [7, 3, 5]
```

 - The `numbers[0]` element was swapped with the `numbers[2]` element.
 - The `numbers[1]` element was swapped with the `numbers[0]` element.
 - The `numbers[2]` element was swapped with the `numbers[1]` element.

[/slide]

[slide]
# Concatenating Lists

You already know a way to append one list to another, with the `extend()` method.

There is one more way, using the `+` operator, just like you concatenate strings.

```python live
nums_list_1 = [1, 2, 3]
nums_list_2 = [4, 5, 6]
final_list = nums_list_1 + nums_list_2
print(final_list) # [1, 2, 3, 4, 5, 6]
```

**Note:** The list on the **right** of the `+` **operator** is **always added at the end** of the **list on the left of the operator**.

[/slide]

[slide]
# set() Method

The `set()` method allows you to **distinct an iterable**, meaning to **extract only the unique elements**.

It returns a **tuple** so you need to **convert it into a list**.

You will learn more about **tuples** in the advanced Python module.

```python live
numbers = [1, 2, 2, 3, 1, 4, 5, 4]
unique_numbers = list(set(numbers))
print(unique_numbers) # [1, 2, 3, 4, 5]
```

[/slide]