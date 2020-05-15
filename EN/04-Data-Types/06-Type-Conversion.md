[slide]
# Type Conversion

When you assign value of one data type to another, the two types might not be compatible with each other.

If the data types are compatible, then Java will perform the conversion automatically known as Automatic Type Conversion and if not then they need to be casted or converted explicitly.

For example, assigning an int value to a long variable.

In Java, there are two types of casting:

- Widening Casting \(automatically\) - converting a smaller type to a larger type size.

```java live
int myInt = 9;
double myDouble = myInt; // Automatic casting: int to double

System.out.println(myInt);
System.out.println(myDouble);
```

Here the lower data type \(having smaller size\) is converted into the higher data type \(having larger size\). Hence there is no loss in data. This is why this type of conversion happens automatically.

- Narrowing Casting \(manually\) - converting a larger type to a smaller size type.

```java live
double myDouble = 9.78;
int myInt = (int)myDouble; // Manual casting: double to int

System.out.println(myDouble);
System.out.println(myInt);
```

Here the higher data types \(having larger size\) are converted into lower data types \(having smaller size\). Hence there is the loss of data. This is why this type of conversion does not happen automatically.

[/slide]

[slide]

# Problem: Centuries to Minutes

[code-task title="Problem: Centuries to Minutes" taskId="9e72df63-7fba-48e8-b7c3-fa121db7f79e" executionType="tests-execution" executionStrategy="java-code" requiresInput][code-editor language=java]

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```

[/code-editor][task-description]

## Description

Write program to enter an integer number of **centuries** and convert it to **years**, **days**, **hours** and **minutes**.

## Examples

| **Input** | **Output**                                                                |
| --------- | ------------------------------------------------------------------------- |
| 1         | 1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes    |
| 5         | 5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes |

[/task-description][code-io /]
[tests][test open]
[input]
1
[/input][output]
1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes
[/output][/test]
[test open][input]
5
[/input][output]
5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes
[/output][/test]
[test][input]
14
[/input][output]
14 centuries = 1400 years = 511339 days = 12272136 hours = 736328160 minutes
[/output][/test]
[test][input]
2
[/input][output]
2 centuries = 200 years = 73048 days = 1753152 hours = 105189120 minutes
[/output][/test]
[test][input]
4
[/input][output]
4 centuries = 400 years = 146096 days = 3506304 hours = 210378240 minutes
[/output][/test]
[test][input]
3
[/input][output]
3 centuries = 300 years = 109572 days = 2629728 hours = 157783680 minutes
[/output][/test]
[test][input]
6
[/input][output]
6 centuries = 600 years = 219145 days = 5259480 hours = 315568800 minutes
[/output][/test]
[/tests][/code-task]
[/slide]

[slide]

# Problem: Centuries to Minutes

[code-task title="Problem: Centuries to Minutes" taskId="9e763-7fba-48e8-b7c3-fabf79" executionType="tests-execution" executionStrategy="java-code" requiresInput][code-editor language=java]

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int centuries = Integer.parseInt(scanner.nextLine());
        int years = centuries * 100;
        int days = (int)(years * 365.2422);
        int hours = days * 24;
        int minutes = hours * 60;

        System.out.printf("%d centuries = %d years = %d days = %d hours = %d minutes", centuries, years, days, hours, minutes);
    }
}
```

[/code-editor][task-description]

## Description

Write program to enter an integer number of **centuries** and convert it to **years**, **days**, **hours** and **minutes**.

## Examples

| **Input** | **Output**                                                                |
| --------- | ------------------------------------------------------------------------- |
| 1         | 1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes    |
| 5         | 5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes |

[/task-description][code-io /]
[tests][test open]
[input]
1
[/input][output]
1 centuries = 100 years = 36524 days = 876576 hours = 52594560 minutes
[/output][/test]
[test open][input]
5
[/input][output]
5 centuries = 500 years = 182621 days = 4382904 hours = 262974240 minutes
[/output][/test]
[test][input]
14
[/input][output]
14 centuries = 1400 years = 511339 days = 12272136 hours = 736328160 minutes
[/output][/test]
[test][input]
2
[/input][output]
2 centuries = 200 years = 73048 days = 1753152 hours = 105189120 minutes
[/output][/test]
[test][input]
4
[/input][output]
4 centuries = 400 years = 146096 days = 3506304 hours = 210378240 minutes
[/output][/test]
[test][input]
3
[/input][output]
3 centuries = 300 years = 109572 days = 2629728 hours = 157783680 minutes
[/output][/test]
[test][input]
6
[/input][output]
6 centuries = 600 years = 219145 days = 5259480 hours = 315568800 minutes
[/output][/test]
[/tests][/code-task]
[/slide]

[slide]

# Problem: Chars to String

[code-task title="Problem: Chars to String" taskId="6bb07-4b0-412b-90cf-cbaa8c9d5c" executionType="tests-execution" executionStrategy="java-code" requiresInput][code-editor language=java]

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```

[/code-editor][task-description]

## Description

Write a program that reads 3 lines of input.

On each line you get a single character.

Combine all the characters into one string and print it on the console.

## Example

| **Input** | **Output** |
| --------- | ---------- |
| a         | abc        |
| b         |            |
| c         |            |

| **Input** | **Output** |
| --------- | ---------- |
| %         | %2o        |
| 2         |            |
| o         |            |

[/task-description][code-io /]
[tests][test open]
[input]
a
b
c
[/input][output]
abc
[/output][/test]
[test open][input]
%
2
0
[/input][output]
%20
[/output][/test]
[test][input]
1
5
p
[/input][output]
15p
[/output][/test]
[test][input]
d
e
f
[/input][output]
def
[/output][/test]
[test][input]
x
y
z
[/input][output]
xyz
[/output][/test]
[test][input]
1
2
3
[/input][output]
123
[/output][/test]
[test][input]
0
0
0
[/input][output]
000
[/output][/test]
[test][input]
1
b

#

[/input][output]
1b#
[/output][/test]
[/tests][/code-task]
[/slide]

[slide]

# Problem: Lower or Upper

[code-task title="Problem: Lower or Upper" taskId="65519ad1-b13a-4eb0-a7dc-24805b4bb257" executionType="tests-execution" executionStrategy="java-code" requiresInput][code-editor language=java]

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```

[/code-editor][task-description]

## Description

Write a program that prints whether a given character is upper-case or lower-case.

## Example

| **Input** | **Output** |
| --------- | ---------- |
| L         | upper-case |

| **Input** | **Output** |
| --------- | ---------- |
| f         | lower-case |

[/task-description][code-io /]
[tests][test open]
[input]
L
[/input][output]
upper-case
[/output][/test]
[test][input]
f
[/input][output]
lower-case
[/output][/test]
[test][input]
A
[/input][output]
upper-case
[/output][/test]
[test][input]
a
[/input][output]
lower-case
[/output][/test]
[/tests][/code-task]
[/slide]
