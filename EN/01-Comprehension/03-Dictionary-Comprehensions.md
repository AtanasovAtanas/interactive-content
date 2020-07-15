# Dictionary Comprehensions

[slide]
# Video

[vimeo-video startTimeInSeconds="4102" endTimeInSeconds="7696"]
[stream language="EN" videoId="421712112" default /]
[stream language="RO" videoId="434994638"  /]
[/video-vimeo]

[/slide]

[slide]
# Structure

Extending the idea of list comprehensions, we can also create dictionaries using dictionary comprehensions.

A dictionary comprehension consists of a few parts:

 - An **input sequence** (iterable).
   - It can be a **list** or **dictionary**.
 - A **variable** that represents **each of the elements** of the **input sequence**.
   - It can also be a **key-value pair**, as we can have a **dictionary input sequence**.
 - A **predicate expression** (think of **lambda expressions**) which is **optional**.
 - An **output expression** that **produces the new dictionary's pairs** from **elements of the input sequence**.

The basic structure of a dictionary comprehension looks like below:

```python
{key: value for (key, value) in [iterable] [optional_predicate_expression]}
```

[/slide]

[slide]
# Examples

In the first example, the **input sequence** will be a **list of numbers**:

```python live
values = list(range(65, 70))
ascii_dictionary = {x: chr(x) for x in values}
print(ascii_dictionary) # {65: 'A', 66: 'B', 67: 'C', 68: 'D', 69: 'E'}
```

The purpose of this dictionary comprehension is to create a **dictionary** that consists of **characters and their ASCII code**.

The **keys** will be the **ASCII codes**, because we don't manipulate it in any way.

But the **values** of **each pair** will be the **corresponding character**, we **convert** the **ASCII code** to a **character** (`chr(x)`).

The result is a **dictionary** with **integer keys** and **character values**.

In the second example, we'll show you how to use a **dictionary as input sequence**:

```python live
grades = {
    "Amy": 5.59,
    "Mark": 4.23,
    "George": 5.21
}

rounded_grades = {name: round(grade) for (name, grade) in grades.items()}
print(rounded_grades) # {'Amy': 6, 'Mark': 4, 'George': 5}
```

Notice that you need to use the `items()` function over the **input dictionary** to get the **pairs**.

The comprehension **creates a new dictionary** that keeps the **keys** of the **input dictionary** but **rounds the values**.

Just like in the list comprehensions, there can be **predicate expressions** too:

```python live
grades = {
    "Amy": 5.59,
    "Mark": 4.23,
    "George": 5.21
}

rounded_grades = {name: round(grade) for (name, grade) in grades.items() if grade > 5}
print(rounded_grades) # {'Amy': 6, 'George': 5}
```

This is the **same as the previous example** with the only **addition** of the **predicate expression**.

It tells the comprehension to add **only the pairs where the grade (value) is higher than 5.00**.

[/slide]

[slide]
# Problem: ASCII Values
[code-task title="ASCII Values" taskId="python-fundamentals-comprehensions-2" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write program that receives a **list of characters** and creates a dictionary with each **character** as a **key** and its **ASCII** value as a **value**.

Try solving that problem using **comprehensions**.

## Examples
| **Input** | **Output** |
| --- | --- |
| a, b, c, a | {'a': 97, 'b': 98, 'c': 99} |
|  |  |

| **Input** | **Output** |
| --- | --- |
| d, c, m, h | {'d': 100, 'c': 99, 'm': 109, 'h': 104} |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
a, b, c, a
[/input]
[output]
\{'a'\: 97, 'b'\: 98, 'c'\: 99\}
[/output]
[/test]
[test open]
[input]
d, c, m, h
[/input]
[output]
\{'d'\: 100, 'c'\: 99, 'm'\: 109, 'h'\: 104\}
[/output]
[/test]
[test]
[input]
f, w, y, n, x
[/input]
[output]
\{'f'\: 102, 'w'\: 119, 'y'\: 121, 'n'\: 110, 'x'\: 120\}
[/output]
[/test]
[test]
[input]
a
[/input]
[output]
\{'a'\: 97\}
[/output]
[/test]
[test]
[input]
g, b, v, c
[/input]
[output]
\{'g'\: 103, 'b'\: 98, 'v'\: 118, 'c'\: 99\}
[/output]
[/test]
[test]
[input]
b, c, x
[/input]
[output]
\{'b'\: 98, 'c'\: 99, 'x'\: 120\}
[/output]
[/test]
[test]
[input]
n, v, d
[/input]
[output]
\{'n'\: 110, 'v'\: 118, 'd'\: 100\}
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: ASCII Values
[code-task title="ASCII Values" taskId="1e56cffe-864d-4130-84aa-cdd2b50ec1da" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
input = input().split(", ")
ascii_dictionary = {ascii: ord(ascii) for ascii in input}
print(ascii_dictionary)
```
[/code-editor]
[task-description]
## Description
Write program that receives a **list of characters** and creates a dictionary with each **character** as a **key** and its **ASCII** value as a **value**.

Try solving that problem using **comprehensions**.

## Examples
| **Input** | **Output** |
| --- | --- |
| a, b, c, a | {'a': 97, 'b': 98, 'c': 99} |
|  |  |

| **Input** | **Output** |
| --- | --- |
| d, c, m, h | {'d': 100, 'c': 99, 'm': 109, 'h': 104} |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
a, b, c, a
[/input]
[output]
\{'a'\: 97, 'b'\: 98, 'c'\: 99\}
[/output]
[/test]
[test open]
[input]
d, c, m, h
[/input]
[output]
\{'d'\: 100, 'c'\: 99, 'm'\: 109, 'h'\: 104\}
[/output]
[/test]
[test]
[input]
f, w, y, n, x
[/input]
[output]
\{'f'\: 102, 'w'\: 119, 'y'\: 121, 'n'\: 110, 'x'\: 120\}
[/output]
[/test]
[test]
[input]
a
[/input]
[output]
\{'a'\: 97\}
[/output]
[/test]
[test]
[input]
g, b, v, c
[/input]
[output]
\{'g'\: 103, 'b'\: 98, 'v'\: 118, 'c'\: 99\}
[/output]
[/test]
[test]
[input]
b, c, x
[/input]
[output]
\{'b'\: 98, 'c'\: 99, 'x'\: 120\}
[/output]
[/test]
[test]
[input]
n, v, d
[/input]
[output]
\{'n'\: 110, 'v'\: 118, 'd'\: 100\}
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# The zip() Function

The `zip()` function returns a **zip object**, that contains a **collection of elements** from **different iterators paired together**.

```python live
countries = ["China", "Belgium", "Australia"]
capitals = ["Beijing", "Brussels", "Canberra"]
countries_capitals = zip(countries, capitals)
print(countries_capitals) # <zip object>
countries_capitals = list(countries_capitals)
print(countries_capitals) # [('China', 'Beijing'), ('Belgium', 'Brussels'), ('Australia', 'Canberra')]
```

Because it returns a `zip object`, you have to **convert** it to a **list** to have a **readable version** of the result.

Basically, it **packs** the **elements** on the **same position** of all **iterators passed**.

If the **passed iterators** have **different lengths**, the iterator with **the least items** decides the **length of the new iterator**.

```python live
countries = ["China", "Belgium", "Australia"]
capitals = ["Beijing", "Brussels"]
countries_capitals = list(zip(countries, capitals))
print(countries_capitals) # [('China', 'Beijing'), ('Belgium', 'Brussels')]
```

You can see that the **last element** of the `countries` list (`"Australia"`) is **ignored** as it **doesn't have with what to be paired**.

The `zip()` function is **often used with dictionary comprehensions** to **generate a dictionary from two lists** (one with the keys and the other with the values).

An example comprehension with the `zip()` function:

```python live
countries = ["China", "Belgium", "Australia"]
capitals = ["Beijing", "Brussels"]

countries_capitals = {country: capital for (country, capital) in zip(countries, capitals)}
print(countries_capitals) # {'China': 'Beijing', 'Belgium': 'Brussels'}
```

As we can see, the result is a **dictionary** with **keys** holding the **name of the country** and **values** with the **name of the capital**.

[/slide]

[slide]
# Problem: Capitals
[code-task title="Capitals" taskId="python-fundamentals-comprehensions-3" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Using **dictionary comprehension** write a program that receives:

 - **countries** on the first line separated by **comma and space** ", "
 - and their corresponding **capital cities** on the second line (again separated by **comma and space** ", ").
 
It should **print each country** with their **capital** on a **separate line** in the format: "\{country\} -> \{capital\}".

## Examples
| **Input** | **Output** |
| --- | --- |
| Bulgaria, Romania, Germany, England | Bulgaria -> Sofia |
| Sofia, Bucharest, Berlin, London | Romania -> Bucharest |
|  | Germany -> Berlin |
|  | England -> London |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Bulgaria, Romania, Germany, England
Sofia, Bucharest, Berlin, London
[/input]
[output]
Bulgaria -\> Sofia
Romania -\> Bucharest
Germany -\> Berlin
England -\> London
[/output]
[/test]
[test]
[input]
a, t, w, r
y, e, b, x
[/input]
[output]
a -\> y
t -\> e
w -\> b
r -\> x
[/output]
[/test]
[test]
[input]
g, e, y, w, k
f, b, x, s, a
[/input]
[output]
g -\> f
e -\> b
y -\> x
w -\> s
k -\> a
[/output]
[/test]
[test]
[input]
x, g, s, y, w, q, o
s, c, v, a, g, h, e
[/input]
[output]
x -\> s
g -\> c
s -\> v
y -\> a
w -\> g
q -\> h
o -\> e
[/output]
[/test]
[test]
[input]
a
b
[/input]
[output]
a -\> b
[/output]
[/test]
[test]
[input]
a, g, e, q, w, y
f, s, a, h, d, c
[/input]
[output]
a -\> f
g -\> s
e -\> a
q -\> h
w -\> d
y -\> c
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Capitals
[code-task title="Capitals" taskId="dd93d6f5-5cab-4dc1-b1ba-dd619b3a442e" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
countries = input().split(', ')
capitals = input().split(', ')

[print(f'{country} -> {capital}') for (country, capital) in zip(countries, capitals)]
```
[/code-editor]
[task-description]
## Description
Using **dictionary comprehension** write a program that receives:

 - **countries** on the first line separated by **comma and space** ", "
 - and their corresponding **capital cities** on the second line (again separated by **comma and space** ", ").
 
It should **print each country** with their **capital** on a **separate line** in the format: "\{country\} -> \{capital\}".

## Examples
| **Input** | **Output** |
| --- | --- |
| Bulgaria, Romania, Germany, England | Bulgaria -> Sofia |
| Sofia, Bucharest, Berlin, London | Romania -> Bucharest |
|  | Germany -> Berlin |
|  | England -> London |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Bulgaria, Romania, Germany, England
Sofia, Bucharest, Berlin, London
[/input]
[output]
Bulgaria -\> Sofia
Romania -\> Bucharest
Germany -\> Berlin
England -\> London
[/output]
[/test]
[test]
[input]
a, t, w, r
y, e, b, x
[/input]
[output]
a -\> y
t -\> e
w -\> b
r -\> x
[/output]
[/test]
[test]
[input]
g, e, y, w, k
f, b, x, s, a
[/input]
[output]
g -\> f
e -\> b
y -\> x
w -\> s
k -\> a
[/output]
[/test]
[test]
[input]
x, g, s, y, w, q, o
s, c, v, a, g, h, e
[/input]
[output]
x -\> s
g -\> c
s -\> v
y -\> a
w -\> g
q -\> h
o -\> e
[/output]
[/test]
[test]
[input]
a
b
[/input]
[output]
a -\> b
[/output]
[/test]
[test]
[input]
a, g, e, q, w, y
f, s, a, h, d, c
[/input]
[output]
a -\> f
g -\> s
e -\> a
q -\> h
w -\> d
y -\> c
[/output]
[/test]
[/tests]
[/code-task]
[/slide]