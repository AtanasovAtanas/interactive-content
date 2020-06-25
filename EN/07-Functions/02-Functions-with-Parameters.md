# Functions with Parameters

[slide]
# Video

[vimeo-video startTimeInSeconds="3664" endTimeInSeconds="6765"]
[stream language="EN" videoId="421666838" default /]
[stream language="RO" videoId="427293221" /]
[/video-vimeo]

[/slide]

[slide]
# Function Parameters

Data can be given to functions through **parameters**, thus the **function will make use of it**.

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

[slide hideTitle]
# Problem: Grades
[code-task title="Grades" taskId="python-fund-10-Functions-problem-1" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a function that receives a grade between 2.00 and 6.00 and prints the corresponding grade in words.
 - 2.00 – 2.99 - "Fail"
 - 3.00 – 3.49 - "Poor"
 - 3.50 – 4.49 - "Good"
 - 4.50 – 5.49 - "Very good"
 - 5.50 – 6.00 - "Excellent"

## Examples
| **Input** | **Output** |
| --- | --- |
| 3.33 | Poor |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 4.50 | Very good |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2.99 | Fail |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3.33
[/input]
[output]
Poor
[/output]
[/test]
[test open]
[input]
4.50
[/input]
[output]
Very Good
[/output]
[/test]
[test open]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
3.49
[/input]
[output]
Poor
[/output]
[/test]
[test]
[input]
4.40
[/input]
[output]
Good
[/output]
[/test]
[test]
[input]
5.50
[/input]
[output]
Excellent
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Grades
[code-task title="Grades" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
grade_data = float(input())

def solve(grade):
    if 2.00 <= grade <= 2.99:
        print('Fail')
    elif 3.00 <= grade <= 3.49:
        print('Poor')
    elif 3.50 <= grade <= 4.49:
        print('Good')
    elif 4.50 <= grade <= 5.49:
        print('Very Good')
    elif 5.50 <= grade <= 6.00:
        print('Excellent')

solve(grade_data)
```
[/code-editor]
[task-description]
## Description
Write a function that receives a grade between 2.00 and 6.00 and prints the corresponding grade in words.
 - 2.00 – 2.99 - "Fail"
 - 3.00 – 3.49 - "Poor"
 - 3.50 – 4.49 - "Good"
 - 4.50 – 5.49 - "Very good"
 - 5.50 – 6.00 - "Excellent"

## Examples
| **Input** | **Output** |
| --- | --- |
| 3.33 | Poor |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 4.50 | Very good |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2.99 | Fail |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3.33
[/input]
[output]
Poor
[/output]
[/test]
[test open]
[input]
4.50
[/input]
[output]
Very Good
[/output]
[/test]
[test open]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
2.99
[/input]
[output]
Fail
[/output]
[/test]
[test]
[input]
3.49
[/input]
[output]
Poor
[/output]
[/test]
[test]
[input]
4.40
[/input]
[output]
Good
[/output]
[/test]
[test]
[input]
5.50
[/input]
[output]
Excellent
[/output]
[/test]
[/tests]
[/code-task]
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

[slide]
# The Return Keyword

The `return` keyword **immediately stops** the function's execution.

```python live
def print_numbers(start, end):
    for i in range(start, end):
        if (i == 5):
            return
        print(i, end=" ")

print_numbers(1, 10) # 1 2 3 4
```

In the example above, the printing **stops** at 4 because **if the number is 5**, the `return` keyword is used.

This can be used to make the **function return a value**, which can be used somehow **outside of the function**.

```python live
def sum(number_one, number_two):
    return number_one + number_two

print(sum(3, 6))
```
[/slide]

[slide]
# Using the Return Values

The **returned values** from functions can be used in many ways:
 - Assigned to a variable
 ```python live
def sum(number_one, number_two):
   return number_one + number_two

sum = sum(4, 8)
print(sum) # 12
```
 - Used in expression
```python live
def sum(number_one, number_two):
   return number_one + number_two

multiplied = sum(3, 2) * 2
print(multiplied) # 10
```
 - Passed to another function
```python live
def sum(number_one, number_two):
   return number_one + number_two

def multiply(number, multiplier):
   return number * multiplier

multiplied = multiply(sum(3, 2), 2)
print(multiplied) # 10
```
[/slide]

[slide hideTitle]
# Problem: Calculations
[code-task title="Calculations" taskId="python-fund-10-Functions-problem-3" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
**Create a function** that receives **three parameters** and **calculates** a result depending on **operator**.

The operator can be  '**multiply**', '**divide**', '**add**', '**subtract**' .

The input comes as three parameters – **two integers** and an operator as **a string**.

## Examples
| **Input** | **Output** |
| --- | --- |
| subtract | 1 |
| 5 |  |
| 4 |  |

| **Input** | **Output** |
| --- | --- |
| divide | 2 |
| 8 |  |
| 4 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
subtract
5
4
[/input]
[output]
1
[/output]
[/test]
[test open]
[input]
divide
8
4
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
multiply
2
2
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
divide
10
2
[/input]
[output]
5
[/output]
[/test]
[test]
[input]
add
10
20
[/input]
[output]
30
[/output]
[/test]
[test]
[input]
subtract
10
6
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
divide
12
2
[/input]
[output]
6
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Calculations
[code-task title="Calculations" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
input_operator = input()
first_num = int(input())
second_num = int(input())

def solve(a, b, operator):
    result = None
    if operator == 'multiply':
        result = a * b
    elif operator == 'divide':
        result = int(a / b)
    elif operator == 'add':
        result = a + b
    elif operator == 'subtract':
        result = a - b
    return result

print(solve(first_num, second_num, input_operator))
```
[/code-editor]
[task-description]
## Description
**Create a function** that receives **three parameters** and **calculates** a result depending on **operator**.

The operator can be  '**multiply**', '**divide**', '**add**', '**subtract**' .

The input comes as three parameters – **two integers** and an operator as **a string**.

## Examples
| **Input** | **Output** |
| --- | --- |
| subtract | 1 |
| 5 |  |
| 4 |  |

| **Input** | **Output** |
| --- | --- |
| divide | 2 |
| 8 |  |
| 4 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
subtract
5
4
[/input]
[output]
1
[/output]
[/test]
[test open]
[input]
divide
8
4
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
multiply
2
2
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
divide
10
2
[/input]
[output]
5
[/output]
[/test]
[test]
[input]
add
10
20
[/input]
[output]
30
[/output]
[/test]
[test]
[input]
subtract
10
6
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
divide
12
2
[/input]
[output]
6
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Repeat String
[code-task title="Repeat String" taskId="python-fund-10-Functions-problem-5" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a function that receives a **string** and a **repeat count n**.

The function should return a new **string** (**the old one repeated n times**).

## Examples
| **Input** | **Output** |
| --- | --- |
| abc | abcabcabc |
| 3 |  |

| **Input** | **Output** |
| --- | --- |
| String | StringString |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
abc
3
[/input]
[output]
abcabcabc
[/output]
[/test]
[test open]
[input]
String
2
[/input]
[output]
StringString
[/output]
[/test]
[test]
[input]
a
5
[/input]
[output]
aaaaa
[/output]
[/test]
[test]
[input]
AbAc
3
[/input]
[output]
AbAcAbAcAbAc
[/output]
[/test]
[test]
[input]
hey
9
[/input]
[output]
heyheyheyheyheyheyheyheyhey
[/output]
[/test]
[test]
[input]
lol
14
[/input]
[output]
lollollollollollollollollollollollollollol
[/output]
[/test]
[test]
[input]
po
44
[/input]
[output]
popopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopo
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Repeat String
[code-task title="Repeat String" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
input_string = input()
repeat_times = int(input())

def repeat_string(string, rep):
    result = ''
    for i in range(0, rep):
        result += string
    return result

print(repeat_string(input_string, repeat_times))
```
[/code-editor]
[task-description]
## Description
Write a function that receives a **string** and a **repeat count n**.

The function should return a new **string** (**the old one repeated n times**).

## Examples
| **Input** | **Output** |
| --- | --- |
| abc | abcabcabc |
| 3 |  |

| **Input** | **Output** |
| --- | --- |
| String | StringString |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
abc
3
[/input]
[output]
abcabcabc
[/output]
[/test]
[test open]
[input]
String
2
[/input]
[output]
StringString
[/output]
[/test]
[test]
[input]
a
5
[/input]
[output]
aaaaa
[/output]
[/test]
[test]
[input]
AbAc
3
[/input]
[output]
AbAcAbAcAbAc
[/output]
[/test]
[test]
[input]
hey
9
[/input]
[output]
heyheyheyheyheyheyheyheyhey
[/output]
[/test]
[test]
[input]
lol
14
[/input]
[output]
lollollollollollollollollollollollollollol
[/output]
[/test]
[test]
[input]
po
44
[/input]
[output]
popopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopopo
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Orders
[code-task title="Orders" taskId="python-fund-10-Functions-problem-7" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a function that calculates the **total price** of an order and prints it on the console.

The function should receive one of the following products: **coffee**, **coke**, **water**, **snacks**; and a **quantity** of the product.

The **prices** for a **single piece** of each product are:

 - coffee - 1.50
 - water - 1.00
 - coke - 1.40
 - snacks - 2.00

## Examples
| **Input** | **Output** |
| --- | --- |
| water | 5.00 |
| 5 |  |

| **Input** | **Output** |
| --- | --- |
| coffee | 3.00 |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
water
5
[/input]
[output]
5.00
[/output]
[/test]
[test open]
[input]
coffee
2
[/input]
[output]
3.00
[/output]
[/test]
[test]
[input]
coffee
5
[/input]
[output]
7.50
[/output]
[/test]
[test]
[input]
water
4
[/input]
[output]
4.00
[/output]
[/test]
[test]
[input]
coke
7
[/input]
[output]
9.80
[/output]
[/test]
[test]
[input]
snacks
5
[/input]
[output]
10.00
[/output]
[/test]
[test]
[input]
coffee
0
[/input]
[output]
0.00
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Orders
[code-task title="Orders" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
input_product = input()
input_quantity = int(input())

def solve(product,quantity):
    if product == 'snacks':
        return quantity * 2.00
    elif product == 'water':
        return quantity * 1.00
    elif product == 'coffee':
        return quantity * 1.50
    elif product == 'coke':
        return quantity * 1.40

print(f'{(solve(input_product,input_quantity)):.2f}')
```
[/code-editor]
[task-description]
## Description
Write a function that calculates the **total price** of an order and prints it on the console.

The function should receive one of the following products: **coffee**, **coke**, **water**, **snacks**; and a **quantity** of the product.

The **prices** for a **single piece** of each product are:

 - coffee - 1.50
 - water - 1.00
 - coke - 1.40
 - snacks - 2.00

## Examples
| **Input** | **Output** |
| --- | --- |
| water | 5.00 |
| 5 |  |

| **Input** | **Output** |
| --- | --- |
| coffee | 3.00 |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
water
5
[/input]
[output]
5.00
[/output]
[/test]
[test open]
[input]
coffee
2
[/input]
[output]
3.00
[/output]
[/test]
[test]
[input]
coffee
5
[/input]
[output]
7.50
[/output]
[/test]
[test]
[input]
water
4
[/input]
[output]
4.00
[/output]
[/test]
[test]
[input]
coke
7
[/input]
[output]
9.80
[/output]
[/test]
[test]
[input]
snacks
5
[/input]
[output]
10.00
[/output]
[/test]
[test]
[input]
coffee
0
[/input]
[output]
0.00
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Calculate Rectangle Area
[code-task title="Calculate Rectangle Area" taskId="python-fund-10-Functions-problem-9" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
**Create a function** that **calculates** and **returns** the **area of a rectangle** by given **width** and **height**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | 12 |
| 4 |  |

| **Input** | **Output** |
| --- | --- |
| 6 | 12 |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
4
[/input]
[output]
12
[/output]
[/test]
[test open]
[input]
6
2
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
7
10
[/input]
[output]
70
[/output]
[/test]
[test]
[input]
5
6
[/input]
[output]
30
[/output]
[/test]
[test]
[input]
6
4
[/input]
[output]
24
[/output]
[/test]
[test]
[input]
112
598
[/input]
[output]
66976
[/output]
[/test]
[test]
[input]
18
90
[/input]
[output]
1620
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Calculate Rectangle Area
[code-task title="Calculate Rectangle Area" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
input_width = int(input())
input_height = int(input())

def calculate_area(width, height):
    return width * height

print(calculate_area(input_width,input_height))
```
[/code-editor]
[task-description]
## Description
**Create a function** that **calculates** and **returns** the **area of a rectangle** by given **width** and **height**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | 12 |
| 4 |  |

| **Input** | **Output** |
| --- | --- |
| 6 | 12 |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
4
[/input]
[output]
12
[/output]
[/test]
[test open]
[input]
6
2
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
7
10
[/input]
[output]
70
[/output]
[/test]
[test]
[input]
5
6
[/input]
[output]
30
[/output]
[/test]
[test]
[input]
6
4
[/input]
[output]
24
[/output]
[/test]
[test]
[input]
112
598
[/input]
[output]
66976
[/output]
[/test]
[test]
[input]
18
90
[/input]
[output]
1620
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
