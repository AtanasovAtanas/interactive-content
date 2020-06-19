# Stack - Last In First Out - LIFO

[slide]
# Stack Functionality

A Stack is a data structure where you add elements to the **top** of the stack, and also remove elements from the **top** again.
This is also referred to as the "Last In First Out" - **LIFO** principle. 

- Stacks provide the following functionality:
    - Pushing an element at the top of the stack
    - Popping element from the top fo the stack
    - Getting the topmost element without removing it

[image assetsSrc="stacksAndQueues-example(1).png" /]

[/slide]

[slide]
# Stack Implementation and Built-In Methods

- Stack Implementation using `ArrayDeque<E>`
```java
ArrayDeque<Integer> stack = new ArrayDeque<>();
```

- `push(element)` - adding elements at the top of the stack
```java live
ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(2);
stack.push(5);
stack.push(10);

stack.forEach(System.out::println);
```

- `pop()` - removing the topmost element
```java live
ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(2);
stack.push(5);
stack.push(10);

// remove 
stack.pop();

stack.forEach(System.out::println);
```

- `peek()` - getting the value of the topmost element
```java live
ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(2);
stack.push(5);
stack.push(10);

// get 
Integer element = stack.peek();

System.out.println(element);
```
# Utility Methods

- `size()` - returns the number of elements in deque

- `isEmpty()` - checks whether the deque is empty or not

- `contains()` - checks whether a deque contains the element or not

[/slide]

[slide]
# Problem: Browser History
[code-task title="Browser History" taskId="f1c2adae-8f12-4f70-94b4-2df7b1453714" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Write a program which takes 2 types of browser instructions:
- Normal navigation: a URL is set, given by a string
- The string "**back**" that sets the current URL to the last set URL

After each instruction the program should **print the current URL**. 
If the **back** instruction can’t be executed, print "**no previous URLs**".
The input **ends** with "**Home**" command, then simply you have to **stop the program**.


## Examples
| **Input** | **Output** |
| --- | --- |
| https//softuni.org/ | https//softuni.org/ |
| back | no previous URLs |
| https//softuni.org/trainings/courses | https//softuni.org/trainings/courses |
| back | https//softuni.org/ |
| https//softuni.org/trainings/2056 | https//softuni.org/trainings/2056 |
| back | https//softuni.org/ |
| https//softuni.org/trainings/live | https//softuni.org/trainings/live |
| https//softuni.org/trainings/live/details | https//softuni.org/trainings/live/details |
| Home |  |

## Hints
- Use ArrayDeque<>
- Use String to keep current page
- Use push(), when moving to next page
- Use pop(), when going back



[/task-description]
[code-io /]
[tests]
[test open]
[input]
https//softuni.org/
back
https//softuni.org/trainings/courses
back
https//softuni.org/trainings/2056
back
https//softuni.org/trainings/live
https//softuni.org/trainings/live/details
Home
[/input]
[output]
https//softuni.org/
no previous URLs
https//softuni.org/trainings/courses
https//softuni.org/
https//softuni.org/trainings/2056
https//softuni.org/
https//softuni.org/trainings/live
https//softuni.org/trainings/live/details
[/output]
[/test]
[test]
[input]
a
b
c
d
e
back
back
back
back
back
back
back
back
Home
[/input]
[output]
a
b
c
d
e
d
c
b
a
no previous URLs
no previous URLs
no previous URLs
no previous URLs
[/output]
[/test]
[test]
[input]
back
back
A
b
c
d
Home
[/input]
[output]
no previous URLs
no previous URLs
A
b
c
d
[/output]
[/test]
[test]
[input]
A
A
A
A
A
A
A
back
back
back
back
Home
[/input]
[output]
A
A
A
A
A
A
A
A
A
A
A
[/output]
[/test]
[test]
[input]
back
back
A
Go
To
Somewhere
Then
Get
back
back
back
And
Finally
Go
Home
[/input]
[output]
no previous URLs
no previous URLs
A
Go
To
Somewhere
Then
Get
Then
Somewhere
To
And
Finally
Go
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide]
# Solution: Browser History
[code-task title="Browser History"  executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayDeque<String> browser = new ArrayDeque<>();
        String line = scanner.nextLine();

        String current = "";
        while (!line.equals("Home")) {
            if (line.equals("back")) {
                if (!browser.isEmpty()) {
                    current = browser.pop();
                } else {
                    System.out.println("no previous URLs");
                    line = scanner.nextLine();
                    continue;
                }
            } else {
                if (!current.equals("")) {
                    browser.push(current);
                }
                current = line;
            }
            System.out.println(current);
            line = scanner.nextLine();
        }
    }
}
```
[/code-editor]
[task-description]
## Description
Write a program which takes 2 types of browser instructions:
- Normal navigation: a URL is set, given by a string
- The string "**back**" that sets the current URL to the last set URL

After each instruction the program should **print the current URL**. 
If the **back** instruction can’t be executed, print "**no previous URLs**".
The input **ends** with "**Home**" command, then simply you have to **stop the program**.


## Examples
| **Input** | **Output** |
| --- | --- |
| https//softuni.org/ | https//softuni.org/ |
| back | no previous URLs |
| https//softuni.org/trainings/courses | https//softuni.org/trainings/courses |
| back | https//softuni.org/ |
| https//softuni.org/trainings/2056 | https//softuni.org/trainings/2056 |
| back | https//softuni.org/ |
| https//softuni.org/trainings/live | https//softuni.org/trainings/live |
| https//softuni.org/trainings/live/details | https//softuni.org/trainings/live/details |
| Home |  |

## Hints
- Use ArrayDeque<>
- Use String to keep current page
- Use push(), when moving to next page
- Use pop(), when going back



[/task-description]
[code-io /]
[tests]
[test open]
[input]
https//softuni.org/
back
https//softuni.org/trainings/courses
back
https//softuni.org/trainings/2056
back
https//softuni.org/trainings/live
https//softuni.org/trainings/live/details
Home
[/input]
[output]
https//softuni.org/
no previous URLs
https//softuni.org/trainings/courses
https//softuni.org/
https//softuni.org/trainings/2056
https//softuni.org/
https//softuni.org/trainings/live
https//softuni.org/trainings/live/details
[/output]
[/test]
[test]
[input]
a
b
c
d
e
back
back
back
back
back
back
back
back
Home
[/input]
[output]
a
b
c
d
e
d
c
b
a
no previous URLs
no previous URLs
no previous URLs
no previous URLs
[/output]
[/test]
[test]
[input]
back
back
A
b
c
d
Home
[/input]
[output]
no previous URLs
no previous URLs
A
b
c
d
[/output]
[/test]
[test]
[input]
A
A
A
A
A
A
A
back
back
back
back
Home
[/input]
[output]
A
A
A
A
A
A
A
A
A
A
A
[/output]
[/test]
[test]
[input]
back
back
A
Go
To
Somewhere
Then
Get
back
back
back
And
Finally
Go
Home
[/input]
[output]
no previous URLs
no previous URLs
A
Go
To
Somewhere
Then
Get
Then
Somewhere
To
And
Finally
Go
[/output]
[/test]
[/tests]
[/code-task]
[/slide]