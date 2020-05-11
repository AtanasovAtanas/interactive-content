# Console Input and Output

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