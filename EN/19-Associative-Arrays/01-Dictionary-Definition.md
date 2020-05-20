# Dictionary Definition

[slide]
# Definition

A dictionary is **unordered collection** of items.

While other data types have only value as an element, a dictionary has **key-value pairs**.

**Values** can be of any type and **can be duplicate**.

Keys must be of **immutable type** (for example strings) and **must be unique**.

You can imagine dictionary as **a list that has custom indices**.

A **phonebook** would be a good **real-life** example:

A **single person** (**string** for their **name**, which is the **key**) has **one or more phone numbers** (a **string** or **list of strings**, which is the **value**).

Code example:

```python
# empty dictionary
my_empty_dict = {}
# dictionary with integer and string keys
my_dict = {1: 'apple', 'vegetable': 'cucumber'}
```

In the example above, there are two pairs:
 - key: `1`, value: `apple`
 - key: `vegetable`, value: `cucumber`

[/slide]