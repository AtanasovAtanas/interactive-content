# Formatting

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