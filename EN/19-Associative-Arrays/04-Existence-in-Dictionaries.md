# Existence in Dictionaries

[slide]
# Check for Key Existence

Just like with lists, we can use the `in` keyword to check if a key is persistent in a dictionary.

The `not` keyword can be paired with `in` to check if a key isn't contained in a dictionary.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

if 'Stephen' in grades:
    print('Persistent.')

if 'Jason' not in grades:
    print('Not persistent')
```

You can use the `keys()` method although it isn't necessary, the result is the same:

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

if 'Stephen' in grades.keys():
    print('Persistent.')

if 'Jason' not in grades.keys():
    print('Not persistent')
```

By **default** when checking **directly the dictionary variable**, it checks the **keys**, not the values.

[/slide]

[slide]
# Check for Value Existence

To check if a **value** is **contained** in a dictionary, you **must** use the `values()` method, otherwise you'd be checking the **keys**.

```python live
grades = {"Stephen": 4.55, "Bellamy": 5.74, "Amy": 5.22}

if 4.55 in grades.values():
    print('Persistent.')

if 4.56 not in grades.values():
    print('Not persistent')
```

[/slide]

[slide]
# Problem: Stock
[code-task title="Stock" taskId="python-fundamentals-Associative-Arrays-02" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will be given **key-value** pairs of **products** and **quantities** (on a single line **separated by space**).

On the next line you will be given products to **search** for.

Check for each product, you have **2 possibilities**:

 - If you **have the product**, print "We have \{quantity\} of \{product\} left"
 - **Otherwise**, print "Sorry, we don't have \{product\}"

## Examples
| **Input** | **Output** |
| --- | --- |
| cheese 10 bread 5 ham 10 chocolate 3 | Sorry, we don't have jam |
| jam cheese ham tomatoes | We have 10 of cheese left |
|  | We have 10 of ham left |
|  | Sorry, we don't have tomatoes |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
cheese 10 bread 5 ham 10 chocolate 3
jam cheese ham tomatoes
[/input]
[output]
Sorry, we don't have jam
We have 10 of cheese left
We have 10 of ham left
Sorry, we don't have tomatoes
[/output]
[/test]
[test]
[input]
g 10
g
[/input]
[output]
We have 10 of g left
[/output]
[/test]
[test]
[input]
a 5 b 10
b a
[/input]
[output]
We have 10 of b left
We have 5 of a left
[/output]
[/test]
[test]
[input]
b 10 j 6
a
[/input]
[output]
Sorry, we don't have a
[/output]
[/test]
[test]
[input]
l 9 o 10 u 55
h n
[/input]
[output]
Sorry, we don't have h
Sorry, we don't have n
[/output]
[/test]
[test]
[input]
k 19 j 22 u 88 y 41
k g v u
[/input]
[output]
We have 19 of k left
Sorry, we don't have g
Sorry, we don't have v
We have 88 of u left
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Stock
[code-task title="Stock" taskId="49b02794-cff5-415f-8d2d-85bb75eaf32a" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
elements = input().split(" ")
bakery = {}
for i in range(0, len(elements), 2):
    key = elements[i]
    value = elements[i + 1]
    bakery[key] = int(value)

searched_products = input().split(" ")
for product in searched_products:
    if product in bakery:
        print(f"We have {bakery[product]} of {product} left")
    else:
        print(f"Sorry, we don't have {product}")
```
[/code-editor]
[task-description]
## Description
You will be given **key-value** pairs of **products** and **quantities** (on a single line **separated by space**).

On the next line you will be given products to **search** for.

Check for each product, you have **2 possibilities**:

 - If you **have the product**, print "We have \{quantity\} of \{product\} left"
 - **Otherwise**, print "Sorry, we don't have \{product\}"

## Examples
| **Input** | **Output** |
| --- | --- |
| cheese 10 bread 5 ham 10 chocolate 3 | Sorry, we don't have jam |
| jam cheese ham tomatoes | We have 10 of cheese left |
|  | We have 10 of ham left |
|  | Sorry, we don't have tomatoes |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
cheese 10 bread 5 ham 10 chocolate 3
jam cheese ham tomatoes
[/input]
[output]
Sorry, we don't have jam
We have 10 of cheese left
We have 10 of ham left
Sorry, we don't have tomatoes
[/output]
[/test]
[test]
[input]
g 10
g
[/input]
[output]
We have 10 of g left
[/output]
[/test]
[test]
[input]
a 5 b 10
b a
[/input]
[output]
We have 10 of b left
We have 5 of a left
[/output]
[/test]
[test]
[input]
b 10 j 6
a
[/input]
[output]
Sorry, we don't have a
[/output]
[/test]
[test]
[input]
l 9 o 10 u 55
h n
[/input]
[output]
Sorry, we don't have h
Sorry, we don't have n
[/output]
[/test]
[test]
[input]
k 19 j 22 u 88 y 41
k g v u
[/input]
[output]
We have 19 of k left
Sorry, we don't have g
Sorry, we don't have v
We have 88 of u left
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Statistics
[code-task title="Statistics" taskId="python-fundamentals-Associative-Arrays-03" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will be receiving **key-value** pairs on separate lines separated by "**:** " until you receive the command "**statistics**".

Sometimes you may receive a product **more than once**.

In that case you have to **add** the **new quantity** to the existing one.

When you receive the "**statistics**" command, print the following:

"Products in stock:

\- \{product1\}: \{quantity1\}

\- \{product2\}: \{quantity2\}

…

Total Products: \{count_all_products\}

Total Quantity: \{sum_all_quantities\}"


## Examples
| **Input** | **Output** |
| --- | --- |
| bread: 4 | Products in stock: |
| cheese: 2 | - bread: 5 |
| ham: 1 | - cheese: 2 |
| bread: 1 | - ham: 1 |
| statistics | Total Products: 3 |
|  | Total Quantity: 8 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
bread: 4
cheese: 2
ham: 1
bread: 1
statistics
[/input]
[output]
Products in stock:
\- bread: 5
\- cheese: 2
\- ham: 1
Total Products: 3
Total Quantity: 8
[/output]
[/test]
[test]
[input]
a: 10
b: 6
c: 8
d: 7
statistics
[/input]
[output]
Products in stock:
\- a: 10
\- b: 6
\- c: 8
\- d: 7
Total Products: 4
Total Quantity: 31
[/output]
[/test]
[test]
[input]
i: 1
statistics
[/input]
[output]
Products in stock:
\- i: 1
Total Products: 1
Total Quantity: 1
[/output]
[/test]
[test]
[input]
n: 10
k: 0
o: 5
statistics
[/input]
[output]
Products in stock:
\- n: 10
\- k: 0
\- o: 5
Total Products: 3
Total Quantity: 15
[/output]
[/test]
[test]
[input]
a: 1
a: 2
a: 3
statistics
[/input]
[output]
Products in stock:
\- a: 6
Total Products: 1
Total Quantity: 6
[/output]
[/test]
[test]
[input]
a: 5
b: 10
a: 9
b: 11
statistics
[/input]
[output]
Products in stock:
\- a: 14
\- b: 21
Total Products: 2
Total Quantity: 35
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Statistics
[code-task title="Statistics" taskId="d8aff116-e500-4d42-83b0-ec16f81edecd" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
products = {}

command = input()
while command != "statistics":
    tokens = command.split(": ")
    product = tokens[0]
    quantity = int(tokens[1])
    if product not in products:
        products[product] = 0
    products[product] += quantity
    command = input()

print("Products in stock:")
for (product, quantity) in products.items():
    print(f"- {product}: {quantity}")
print(f"Total Products: {len(products.keys())}")
print(f"Total Quantity: {sum(products.values())}")
```
[/code-editor]
[task-description]
## Description
You will be receiving **key-value** pairs on separate lines separated by "**:** " until you receive the command "**statistics**".

Sometimes you may receive a product **more than once**.

In that case you have to **add** the **new quantity** to the existing one.

When you receive the "**statistics**" command, print the following:

"Products in stock:

\- \{product1\}: \{quantity1\}

\- \{product2\}: \{quantity2\}

…

Total Products: \{count_all_products\}

Total Quantity: \{sum_all_quantities\}"

## Examples
| **Input** | **Output** |
| --- | --- |
| bread: 4 | Products in stock: |
| cheese: 2 | - bread: 5 |
| ham: 1 | - cheese: 2 |
| bread: 1 | - ham: 1 |
| statistics | Total Products: 3 |
|  | Total Quantity: 8 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
bread: 4
cheese: 2
ham: 1
bread: 1
statistics
[/input]
[output]
Products in stock:
\- bread: 5
\- cheese: 2
\- ham: 1
Total Products: 3
Total Quantity: 8
[/output]
[/test]
[test]
[input]
a: 10
b: 6
c: 8
d: 7
statistics
[/input]
[output]
Products in stock:
\- a: 10
\- b: 6
\- c: 8
\- d: 7
Total Products: 4
Total Quantity: 31
[/output]
[/test]
[test]
[input]
i: 1
statistics
[/input]
[output]
Products in stock:
\- i: 1
Total Products: 1
Total Quantity: 1
[/output]
[/test]
[test]
[input]
n: 10
k: 0
o: 5
statistics
[/input]
[output]
Products in stock:
\- n: 10
\- k: 0
\- o: 5
Total Products: 3
Total Quantity: 15
[/output]
[/test]
[test]
[input]
a: 1
a: 2
a: 3
statistics
[/input]
[output]
Products in stock:
\- a: 6
Total Products: 1
Total Quantity: 6
[/output]
[/test]
[test]
[input]
a: 5
b: 10
a: 9
b: 11
statistics
[/input]
[output]
Products in stock:
\- a: 14
\- b: 21
Total Products: 2
Total Quantity: 35
[/output]
[/test]
[/tests]
[/code-task]
[/slide]