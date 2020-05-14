# Declaring and Invoking Functions

[slide]
# Simple Functions

In order to **declare** a function, use the `def` keyword:

```python
def print_greeting():
  print("Good morning!")
```

Notice there is a colon (`:`) after the braces.

[/slide]

[slide]
# Invoking Functions

A function can be invoked from **everywhere in the scope**, where it is defined.

```python live
def print_greeting():
  print("Good morning!")

print_greeting()
```

It can be called from **another function**:

```python live
def print_name():
  print("Hello, John Doe!")
  print_greeting()

def print_greeting():
  print("Good morning!")

print_name()
```

It can also be called **in its own body**:

```python
def print_name():
  print("Hello, John Doe!")
  print_name()
```

The example above will raise a `RecursionError` because there is **no end condition**.

A recursion means that **a functions calls itself**.

Take a look at the example below:

```python live
def increment(number):
  if number >= 10:
    return

  print(number, end=" ")
  number += 1
  increment(number)

increment(1)
```

That's all you need to know about recursion for the moment.

[/slide]