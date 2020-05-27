# Variables and Data Types

[slide]
# Video

[vimeo-video startTimeInSeconds="1470" endTimeInSeconds="2640"]
[stream language="EN" videoId="421699623" default /]
[stream language="RO" videoId="422883581" /]
[/video-vimeo]
[/slide]

[slide]
# Variables
In Python, we can use **variables** to **store data**, they are containers for storing data values.

[image assetsSrc="boxes-with-variables.png" /]

Declaring a **variable** looks like this:
```python
name = 'Bob'
is_employed = True
age = 35
```
On the **left** is the **variable name** and on the **right** - its **value**.

# Variable Names
In Python, variable names follow the **snake-case** naming convention, which separates words with:
 - one underscore character (`_`)
 - no spaces
 - each element's initial letter usually lowercased within the compound
 - the first letter either upper or lowercase

There are some examples for valid variable names in Python:
```python
users_count
first_name
```

There are several rules for Python variables names:
 - **must start** with a **letter** or an **underscore** (`_`)
 - **cannot start with a number**
 - can contain **only alpha-numeric characters** and **underscores** (`A-z, 0-9, _`)
 - are **case-sensitive**, meaning `name`, `Name` and `NAME` would be **3 different variables**

[/slide]

[slide]
# Data Types
Python has very few but robust data types:
 - `int` - integer (whole) numbers
 ```python
 age = 6
 ```
 - `float` - floating point numbers
 ```python
 pi = 3.14159265
 ```
 - `bool` - boolean logical value (`True`/`False`)
 ```python
 is_alive = False
 ```
 - `str` - string (character sequence)
 ```python
 name = 'John Smith'
 ```
 - `None` - used to define a **null value**, meaning **no value**; equivalent to `null` in other languages
 ```python
 to_be_set_later = None
 ```

**Note:** Unlike other programming languages, in Python the variable's **data type** is **not** declared before its name.

# Data Type Checking
A variable's data type can be checked by using `type()`:
```python live
name = 'Mark'
print(type(name)) # output: <class 'str'>
price = 10.33
print(type(price)) # output: <class 'float'>
```

# Data Type Conversion
A `str` can be converted to an `int`:
```python live
num_as_str = '10'
num = int(num_as_str)
float_num = float('3.33')
print(type(num_as_str)) # output: <class 'str'>
print(type(num)) # output: <class 'int'>
print(type(float_num)) # output: <class 'float'>
```

[/slide]