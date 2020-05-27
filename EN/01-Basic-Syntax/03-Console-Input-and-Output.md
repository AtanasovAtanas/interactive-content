# Console Input and Output

[slide]
# Video

[vimeo-video startTimeInSeconds="2641" endTimeInSeconds="3974"]
[stream language="EN" videoId="421699623" default /]
[stream language="RO" videoId="422883581" /]
[/video-vimeo]
[/slide]

[slide]
# Printing on the Console
Printing on the console is simple. Type `print()` and whatever you want to print between the braces.

Both `'` and `"` can be used to write a string.

```python live
print('Hello from the console.')
print("Hello from the console, again.")
```
By default, after printing, the console goes to a new line.

If you want to prevent this from happening, or print something else in the end, you have to use the `end` parameter:

```python live
print('Hello from the console.')
print('This line will be on a new line.')

print('Hello from the console, again.', end=' ')
print('This line will not be on a new line because of using the end parameter.')
```

[/slide]

[slide]
# Reading from the Console
Reading from the console can be achieved by using `input()`.

Whatever you read can be **saved** into **variables** (as a `string`):

```python live
name = input()
print('Hello, ' + name)
```

Also, if possible, you can convert it into another data type:

```python live
number = int(input())
print(type(number)) # output: <class 'int'>
```

The `input()` function can print a string on the console before requiring the user to enter the input:
```python live
name = input('enter your name: ')
print('Hello, ' + name)
```
[/slide]

[slide]
# String Formatting
In Python, **strings** can be formatted with **placeholders**. There are different ways to **format a string**:

 - String formatting:

 ```python live
 animal = 'dog'
 age = 2
 formatted_string = 'This %s is %d years old.' % (animal, age)
 print(formatted_string)
 ```
We use `%s` for strings and `%d` for numbers.

 - `format` function:

 ```python live
 animal = 'dog'
 age = 2
 formatted_string = 'This {0} is {1} years old.'.format(animal, age)
 print(formatted_string)
 ```

 - Interpolation:

 ```python live
 animal = 'dog'
 age = 2
 interpolated_string = f'This {animal} is {age} years old.'
 print(interpolated_string)
 ```

[/slide]

[slide]
# Number Formatting
There are also different ways to **format a number**:

The default way is to format up to the 15th decimal place, shown below:
 ```python live
 pi = 3.141592653589793238462643383279
 default_format = '{}'.format(pi)

 print(default_format) # output: 3.141592653589793
 ```

There is also a custom formatting, where you can say to which decimal place the number to be formatted:
 ```python live
 pi = 3.141592653589793238462643383279
 formatted = '{:.3f}'.format(pi)

 print(formatted) # output: 3.142
 ```
[/slide]