# String Definition

[slide]
# Video

[vimeo-video startTimeInSeconds="1028" endTimeInSeconds="1655"]
[stream language="EN" videoId="421758207" default /]
[stream language="RO" videoId="434995028"  /]
[/video-vimeo]

[/slide]

[slide]
# What is a String?

A string is a **sequence of characters**.

Each character is simply a **symbol**.

Computers don't deal with characters, but with **numbers** instead.

A character is stored and manipulated as a **combination** of **0's** and **1's**.

In Python a string is a sequence of **Unicode** characters.

**Unicode** is a **standard** for **consistent** encoding, representation and handling of text.

Learn more [here](https://home.unicode.org/).

[image assetsSrc="indices-strings.png" /]

[/slide]

[slide]
# String Literals

String literals are **surrounded** by either **single** or **double quotation marks**.

`'hello'` is the same as `"hello"`.

However if you want to use `'` in the string, you need to use `"` to declare the string.

```python live
print("hello, my name's Jordan")
```

While the above example had no trouble, the one below will raise a `SyntaxError`:

```python live
print('hello, my name's Jordan')
```

Another way to prevent this `SyntaxError` is to **escape** problematic characters:

```python live
print('hello, my name\'s Jordan')
```

As you see in the example above, escaping is done by typing `\` **before the character**.

[/slide]

[slide]
# Assign String to a Variable

As you should already know, assigning a string to a variable is done with the `=` operator.

**First** you declare the **variable name**, then **put** the `=` **operator**, **followed** by a **string**.

```python live
a = "Hello!"
print(a)
```

There is a way to assign a **multiline string** to a variable by using **three double quotation marks**.

Upon printing, it will be printed **along with the new lines**.

```python live
forecast_advice = """Hello, Emily!
It's raining outside.
You should grab an umbrella."""

print(forecast_advice)
```

[/slide]

[slide]
# str() and split() Functions

## str()

The `str()` function converts the specified in the braces value into a string.

The example below will raise a `TypeError` because an integer cannot be concatenated to strings:

```python live
print('Outside is ' + 32 + ' degrees.')
```

Let's make use of the `str()` function and prevent this error:

```python live
print('Outside is ' + str(32) + ' degrees.')
```

## split()

Use the `split()` function over a string and it will create a list.

The `split()` function accepts a **parameter**, that defines by what it will split the string, a **separator**.

```python live
some_text = "a!b!c!d"
my_list = some_text.split("!")
print(my_list) # ['a', 'b', 'c', 'd']
```

In case you don't specify the separator, the function will try to split the string by spaces. See the example below:

```python live
some_text = "hello, my name is Stephen."
my_list = some_text.split()
print(my_list) # ['hello,', 'my', 'name', 'is', 'Stephen.']
```

The separator can be a whole string, not only a single character.

```python live
some_text = "How separate are separate you"
my_list = some_text.split("separate")
print(my_list) # ['How ', ' are ', ' you']
```

[/slide]

[slide]
# Problem: Reverse Strings
[code-task title="Reverse Strings" taskId="python-fundamentals-Text-Processing-01" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
You will be given series of strings until you receive an "**end**" command.

Write a program that reverses strings and prints each pair on separate line in format:

"\{word\} = \{reversed word\}".

## Examples
| **Input** | **Output** |
| --- | --- |
| helLo | helLo = oLleh |
| Softuni | Softuni = inutfoS |
| bottle | bottle = elttob |
| end |  |

| **Input** | **Output** |
| --- | --- |
| Dog | Dog = goD |
| caT | caT = Tac |
| chAir | chAir = riAhc |
| end |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
helLo
Softuni
bottle
end
[/input]
[output]
helLo = oLleh
Softuni = inutfoS
bottle = elttob
[/output]
[/test]
[test open]
[input]
Dog
caT
chAir
end
[/input]
[output]
Dog = goD
caT = Tac
chAir = riAhc
[/output]
[/test]
[test]
[input]
Fork
Pork
Zork
end
[/input]
[output]
Fork = kroF
Pork = kroP
Zork = kroZ
[/output]
[/test]
[test]
[input]
test
Fail
Pass
Happy
end
[/input]
[output]
test = tset
Fail = liaF
Pass = ssaP
Happy = yppaH
[/output]
[/test]
[test]
[input]
123
0101
java
python
end
[/input]
[output]
123 = 321
0101 = 1010
java = avaj
python = nohtyp
[/output]
[/test]
[test]
[input]
DEN
pesho
gosho
12731y2h3
end
[/input]
[output]
DEN = NED
pesho = ohsep
gosho = ohsog
12731y2h3 = 3h2y13721
[/output]
[/test]
[test]
[input]
edn
10x
lab
!\*\#&@\#&@!JDSOsk
cobra
fury
end
[/input]
[output]
edn = nde
10x = x01
lab = bal
!\*\#&@\#&@!JDSOsk = ksOSDJ!@&\#@&\#\*!
cobra = arboc
fury = yruf
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Reverse Strings
[code-task title="Reverse Strings" taskId="6fdea5b3-1b72-4ff3-8f48-d8eafcd74d07" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
text = input()
while text != "end":
    text_reversed = ""
    for ch in reversed(text):
        text_reversed += ch
    print(text + " = " + text_reversed)
    text = input()
```
[/code-editor]
[task-description]
## Description
You will be given series of strings until you receive an "**end**" command.

Write a program that reverses strings and prints each pair on separate line in format:

"\{word\} = \{reversed word\}".

## Examples
| **Input** | **Output** |
| --- | --- |
| helLo | helLo = oLleh |
| Softuni | Softuni = inutfoS |
| bottle | bottle = elttob |
| end |  |

| **Input** | **Output** |
| --- | --- |
| Dog | Dog = goD |
| caT | caT = Tac |
| chAir | chAir = riAhc |
| end |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
helLo
Softuni
bottle
end
[/input]
[output]
helLo = oLleh
Softuni = inutfoS
bottle = elttob
[/output]
[/test]
[test open]
[input]
Dog
caT
chAir
end
[/input]
[output]
Dog = goD
caT = Tac
chAir = riAhc
[/output]
[/test]
[test]
[input]
Fork
Pork
Zork
end
[/input]
[output]
Fork = kroF
Pork = kroP
Zork = kroZ
[/output]
[/test]
[test]
[input]
test
Fail
Pass
Happy
end
[/input]
[output]
test = tset
Fail = liaF
Pass = ssaP
Happy = yppaH
[/output]
[/test]
[test]
[input]
123
0101
java
python
end
[/input]
[output]
123 = 321
0101 = 1010
java = avaj
python = nohtyp
[/output]
[/test]
[test]
[input]
DEN
pesho
gosho
12731y2h3
end
[/input]
[output]
DEN = NED
pesho = ohsep
gosho = ohsog
12731y2h3 = 3h2y13721
[/output]
[/test]
[test]
[input]
edn
10x
lab
!\*\#&@\#&@!JDSOsk
cobra
fury
end
[/input]
[output]
edn = nde
10x = x01
lab = bal
!\*\#&@\#&@!JDSOsk = ksOSDJ!@&\#@&\#\*!
cobra = arboc
fury = yruf
[/output]
[/test]
[/tests]
[/code-task]
[/slide]