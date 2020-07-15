# Intro to Comprehensions

[slide]
# Video

[vimeo-video startTimeInSeconds="976" endTimeInSeconds="1273"]
[stream language="EN" videoId="421712112" default /]
[stream language="RO" videoId="434994638"  /]
[/video-vimeo]

[/slide]

[slide]
# Definition

Comprehensions are **constructs** that allow us to **create sequences from other sequences**.

They provide us a **short syntax** for **constructing new sequences**.

Python supports **4 types of comprehensions**:

 - **List** Comprehensions
 - **Dictionary** Comprehensions
 - **Set** Comprehensions
 - **Generator** Comprehensions

In this lesson we will explain only the **first two**.

Example:

```python live
my_list = [num for num in range(5)]
print(my_list) # [0, 1, 2, 3, 4]
```

We won't explain the example **yet**, it is here just so you know how a **comprehension looks like**.

[/slide]

[slide]
# Benefits

Let's list the **benefits** we get for using **comprehensions**:

 - **Shorter syntax**: you are **reducing code length** to **one line** which is **instanly recognizable** to anyone who understands comprehensions.
 - **Less memory**: Python will **allocate the sequence's memory** first, **before adding elements to it**, instead of **resizing on runtime**.
 - Easier **data manipulation**.
 - Better **performance**.
 - More **Python-like** coding **style**.

[/slide]

[slide]
# Example

Let's have some more examples before diving into explanations.

The example below **filters even numbers** from a list using a **comprehension**:

```python live
x = [1, 2, 3, 4, 5, 6]
filtered = [num for num in x if num % 2 == 0]
print(filtered) # [2, 4, 6]
```

If we didn't use a **comprehension**, the code would look like this:

```python live
x = [1, 2, 3, 4, 5, 6]
filtered = []

for element in x:
   if element % 2 == 0:
       filtered.append(element)

print(filtered)
```

Now, you see how **shorter** the solution **with a comprehension** is compared to the **one without**.

There is another example that takes the first letter of each word from a list:

```python live
items = [word[0] for word in ["this", "is", "a", "list"]]
print(items) # ['t', 'i', 'a', 'l']
```

[/slide]