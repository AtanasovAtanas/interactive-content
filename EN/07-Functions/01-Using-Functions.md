# Using Functions

[slide]
# Video

[vimeo-video startTimeInSeconds="966" endTimeInSeconds="3104"]
[stream language="EN" videoId="421666838" default /]
[stream language="RO" videoId="427293221" /]
[/video-vimeo]

[/slide]

[slide]
# Definition and Benefits

```python
def function_name(parameter_name):
  print(parameter_name)
```

A function is a **block of code** that is **executed only when called**.

Data can be **passed to it**, as known as **parameters**.

Functions can **return data too**, as **their result**.

The reasons functions should be used are:
 - Splits large problems **into small pieces**
 - **Better organization** of the program code
 - Improves code **readiblity**
 - Improves code **understandability**
 - Improves code **maintainability**
 - Code **reusability**; using existing functions multiple times

[/slide]

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