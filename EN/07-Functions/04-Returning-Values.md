# Returning Values

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

[slide]
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

[slide]
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

[slide]
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

[slide]
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

[slide]
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

[slide]
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

[slide]
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

[slide]
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