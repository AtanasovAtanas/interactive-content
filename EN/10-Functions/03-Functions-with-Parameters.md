# Functions with Parameters

[slide]
# Function Parameters

Data can be given to functions through **parameters**.

They are declared in the **braces after the function's name**.

Parameters can be **zero** or **several**.

They can be of **any data type**.

Each parameter has a **name**.

```python live
def print_name(name):
    print("Hello, " + name)

print_name("Jason")
```

Make sure you pass to the function **just as many parameters as it needs**.

You **cannot** invoke a function by passing **less or more** parameters than it needs.

```python live
def print_name(name):
    print("Hello, " + name)

print_name("Jason") # Hello, Jason
print_name() # TypeError, missing argument
print_name("Jason", "Oprah") # TypeError, more arguments
```

[/slide]

[slide]
# Optional Parameters

Parameters can accept **default values**.

```python
def print_numbers(start=0, end=100):
   for i in range(start, end + 1):
      print(i, end=' ')
```

Giving an argument a **default value**, gives you the possibility to **omit it when calling the function**.

Doing this, the function will be executed with its **default argument values**.

There are a few ways to call a function which has optional parameters:

```python live
def print_information(name="John Doe", location="London"):
  print(f"{name} is located in {location}")

print_information()
print_information("Peter", "New York")
print_information("Michael")
print_information(location="New Orleans")
```

[/slide]