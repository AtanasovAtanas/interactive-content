# Accessing Elements

[slide]
# Using Indices

Each element in a list has its own **index** (**position**) by which it can be **accessed**. **Indeces** in lists **always start from 0** and the **last index** is *equal* to the **number of elements minus 1**. To access a list element use **square brackets and its index**. See the example for better understanding:
```python live
my_list = [3, 6, 9]
print(my_list[0]) # 3; always start from 0
print(my_list[1]) # 6; the second element is at index 1
print(my_list[2]) # 9; the last element is at index 2
```
In the example above, we access the **last element at index 2**, because we **subtract 1 from the number of elements** (3 - 1 = 2).

[/slide]

[slide]
# Negative Indices

In Python, **negative indices** can be used to access elements. Using negative index, starts counting **from the end** of the list, for example the **-1 index** will give you the **last element**.
```python live
my_list = [3, 6, 9]
print(my_list[-1]) # 9
print(my_list[-2]) # 6
print(my_list[-3]) # 3
```

[/slide]

[slide]
# Range of Indices

You can specify a **range of indices** that you want to access by defining from which one to **start** and **end** the range. This results in returning a **new list** with the elements in that range. Note that the element at the **end** specified **index won't be included**.
```python live
my_list = [3, 6, 9, 12, 15, 18, 21]
print(my_list[0:3]) # returns the elements at indices 0, 1 and 2, but not the one at index 3
print(my_list[3:5]) # [12, 15]
```
However, if you don't specify the **start index**, it will **start from the first element**. If you don't specify the **end index** - the range will go on **to the end of the list**.
```python live
my_list = [3, 6, 9, 12, 15, 18, 21]
print(my_list[:3]) # [3, 6, 9]
print(my_list[3:]) # [12, 15, 18, 21]
```
You can use **negative indices** to specify the range. It will act as expected, **start from the end** of the list.
```python live
my_list = [3, 6, 9, 12, 15, 18, 21]
print(my_list[-4:-1]) # [12, 15, 18]
```
[/slide]

[slide]
# Invalid Indices

You **cannot** access any index. **Valid** indices are those which **have a value**. Valid **positive** indices are **from 0 to** `[number of list elements] - 1`. Valid **negative** indices are **from -1 to the negative of** `[number of list elements]`. Accessing **invalid** index will cause an **error**.

In this example we are accessing **only valid indices**, the first and the last:
```python live
my_list = [3, 6, 9, 12, 15, 18, 21]
number_of_elements = 7
print(my_list[0])
print(my_list[number_of_elements - 1])
print(my_list[-1])
print(my_list[(number_of_elements) * -1]) # multiplying by -1 to make it a negative number
```

Now let's try to access a **positive invalid index**. An **error** is **expected** to be thrown.
```python live
my_list = [3, 6, 9, 12, 15, 18, 21]
number_of_elements = 7
print(my_list[number_of_elements])
```

What is left is to try to access a **negative invalid index**, let's do it. As in the previous example, an **error** is expected.
```python live
my_list = [3, 6, 9, 12, 15, 18, 21]
number_of_elements = 7
print(my_list[(number_of_elements + 1) * -1] ) # multiplying by -1 to make it a negative number
```
[/slide]