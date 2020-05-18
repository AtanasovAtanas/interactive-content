# Advanced Methods

[slide]
# Lambda Basics

A `lambda` operator is used for creating small, **one-time** and **anonymous** function objects in Python.

An **anonymous function** is one that is defined **without a name**.

Normal functions are defined with the `def` keyword, while the anonymous - with the `lambda` keyword.

```python
lambda arguments: expression
```

```python
lambda x: x * 2
```

The above lambda function accepts `x` parameter and return `x * 2`.

Such functions can be saved in variables.

Now let's see it in action:

```python live
multipication = lambda x: x * 2
print(multipication(3)) # 6
```

[/slide]

[slide]
# map() Method

The `map(function, iterable)` function **executes** the **given function** for **each element of an iterable**, for example a **list**.

It returns an **iterator map object** so you need to **convert it into a list**.

There is an example that multiplies each element (number) of the list by 2:
```python live
my_list = [1, 2, 3, 4, 5]
my_list = list(map(lambda x: x * 2, my_list))
print(my_list) # [2, 4, 6, 8, 10]
```

You can pass **as many iterables as you wish**, but for this the **lambda function needs to have one parameter for each iterable**.

There is one example that uses 2 iterables and 2 parameters for the lambda:
```python live
numbers_list_one = [1, 2, 3, 4, 5]
numbers_list_two = [2, 5, 3, 10, 5]
my_list = list(map(lambda x, y: x * y, numbers_list_one, numbers_list_two))
print(my_list) # [2, 10, 9, 40, 25]
```

The example above takes each element of `numbers_list_one` and multiplies it with the element on the same index of `numbers_list_two`.

[/slide]

[slide]
# filter() Method

The `filter(function, iterable)` method **filters elements**, in other words - **removes elements** that **don't fulfill a given condition**.

The lambda function given **should return a boolean value**, so that it can filter the elements.

It returns an **iterator map object** so you need to **convert it into a list**.

There is an example that **filters all the even numbers** of a list:
```python live
numbers_list = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers_list))
print(even_numbers) # [2, 4, 6]
```

[/slide]