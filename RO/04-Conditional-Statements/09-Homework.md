# Homework

[slide]
# Video

[vimeo-video startTimeInSeconds="7708" endTimeInSeconds="9990"]
[stream language="EN" videoId="341539841/456a08950e"  /]
[stream language="RO" videoId="387657941/b7f1ede8f0" default /]
[/vimeo-video]

[/slide]

[slide]
# Homework
Welcome to the homework. 

Now we are going to write a couple of console applications, by which we are going to make a few more steps into programming. 

We have prepared some problems for you to solve.

Let's solve a few problems to confirm what we have learned.

[image src="https://github.com/AtanasovAtanas/pb-interactive-csharp/blob/master/assets/homeowrk.png"/]
[/slide]

[slide]
# Problem: Guess the Password
[code-task title="Guess the Password" taskId="C-p-01" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program to check a password:

  * Read a string: the password **guess**
  * Print **"Welcome"** if the password guess is **"s3cr3t!"**
  * Print **"Wrong password!"** in all other cases 
# Example
## Input
- s3cr3t!
## Output
- Welcome
## Input
- qwerty
## Output
- Wrong password!
[/task-description]
[tests]
[test]
[input]
s3cr3t!
[/input]
[output]
Welcome
[/output]
[/test]
[test]
[input]
wrong
[/input]
[output]
Wrong password!
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide]
# Problem: Boiling Water
[code-task title="Boiling Water" taskId="C-p-02" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]

```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program, which checks for hot water: 

  * Read a floating-point number: the water **temperature** (in °C)
  * Print **"The water is boiling"** if the number **> 100**
  * Prints **"The water is not hot enough"** in all other cases 
# Example
## Input
- 104.8
## Output
- The water is boiling
## Input
- 29
## Output
- The water is not hot enough
[/task-description]
[tests]
[test]
[input]
105
[/input]
[output]
The water is boiling
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
The water is not hot enough
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide]
# Problem: Speed Info
[code-task title="Speed Info" taskId="C-p-03" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]

```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program to check for fast / slow speed: 

  * Read the **speed** (a floating-point number)
  * Print **"Slow"** if the speed **<= 30**
  * Print **"Fast"** if the speed **> 30**
# Example
## Input
- 30
## Output
- Slow
## Input
- 60
## Output
- Fast
[/task-description]
[tests]
[test]
[input]
30
[/input]
[output]
Slow
[/output]
[/test]
[test]
[input]
43
[/input]
[output]
Fast
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide]
# Problem: Area of Figures
[code-task title="Area of Figures" taskId="C-p-04" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]

```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program to calculate the area of different figures:
  * Reads a string: the figure **type**
  * Checks if the entered figure is **square**, **rectangle** or **circle**
  * Reads a number for square and circle or two numbers for rectangle
    * Numbers will be floating-point
  * Prints the calculated area **formatted** to the second digit after the decimal point
  * For unknown figure print **"Unknown figure"**

## Examples

| **Input** | **Output** |
| --- | --- |
| square | 25.00 |
| 5 |  |

| **Input** | **Output** |
| --- | --- |
| rectangle | 30.00 |
| 3 |  |
| 10 |  |

| **Input** | **Output** |
| --- | --- |
| trapezoid | Unknown figure |

| **Input** | **Output** |
| --- | --- |
| circle | 28.27 |
| 28.27 | |

[/task-description]
[tests]
[test]
[input]
square
5
[/input]
[output]
25.00
[/output]
[/test]
[test]
[input]
rectangle
5
10
[/input]
[output]
50.00
[/output]
[/test]
[test]
[input]
circle
2.5
[/input]
[output]
19.63
[/output]
[/test]
[test]
[input]
figure
[/input]
[output]
Unknown figure
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide]
# Problem: Tickets
[code-task title="Tickets" taskId="C-p-05" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program to calculate a ticket price:

  * Read a ticket type: either **student** or **regular**
  * Print the **price** in the following format "$\{price\}":
    * The price should be **formatted** to 2nd digit after the decimal point
  * Student ticket price: **1.00**
  * Regular ticket price: **1.60**
  * For invalid type print **"Invalid ticket type!"**
# Example
## Input
- student
## Output
- $1.00
[/task-description]
[tests]
[test]
[input]
student
[/input]
[output]
$1.00
[/output]
[/test]
[test]
[input]
regular
[/input]
[output]
$1.60
[/output]
[/test]
[test]
[input]
ticket
[/input]
[output]
Invalid ticket type!
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide]
# Problem: Coffee Shop
[code-task title="Coffee Shop" taskId="C-p-06" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]

```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program to calculate the drink price in a coffee shop:

  * Read a drink: either **"coffee"** or **"tea"**
  * Read an extra: either **"sugar"** or **"no"**
  * Print the price in format `"Final price: ${price}"`
    * The price should be **formatted** to 2nd digit after the decimal point
  
Prices:
  * Coffee price: **1.00**
  * Tea price: **0.60**
  * Sugar price: **0.40**
# Example
## Input
- coffee
- sugar
## Output
- Final price: $1.40
## Input
- tea
- no
## Output
- Final price: $0.60
[/task-description]
[tests]
[test]
[input]
coffee
sugar
[/input]
[output]
Final price: $1.40
[/output]
[/test]
[test]
[input]
coffee
no
[/input]
[output]
Final price: $1.00
[/output]
[/test]
[test]
[input]
tea
sugar
[/input]
[output]
Final price: $1.00
[/output]
[/test]
[test]
[input]
tea
no
[/input]
[output]
Final price: $0.60
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide]
# Problem: Valid Triangle
[code-task title="Valid Triangle" taskId="C-p-07" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]

```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program to check if a triangle is valid by its sizes:

  * Read 3 integers: the **sides of a triangle**
  * Checks if each side is less than the sum of the others 2
    * Prints **"Valid Triangle"** if the above condition is met
    * Prints **"Invalid Triangle"** otherwise 
# Example
## Input
- 3
- 4
- 5
## Output
- Valid Triangle

[/task-description]
[tests]
[test]
[input]
3
4
5
[/input]
[output]
Valid Triangle
[/output]
[/test]
[test]
[input]
5
8
3
[/input]
[output]
Invalid Triangle
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]
[/slide]

[slide]
# Homework Results

[tasks-results /]

[/slide]