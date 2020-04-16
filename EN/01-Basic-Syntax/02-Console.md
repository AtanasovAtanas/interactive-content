# Console Input and Output

[slide]
# Video

[vimeo-video startTimeInSeconds="1778" endTimeInSeconds="2358 "]
[stream language="EN" videoId="341522009/063bddc415" default /]
[stream language="RO" videoId="386049133/766a425069"  /]
[/video-vimeo]

[/slide]

[slide]
# Reading from the Console
We can **read/write** to the console, using the **Scanner** class.

Import the **java.util.Scanner** class:

```java
import java.util.Scanner;
…
Scanner sc = new Scanner(System.in);
```

Reading input from the console:

```java
String name = sc.nextLine();
```

## Converting Input from the Console
As you know **scanner.nextLine()** returns a **String**, if we want **Integer** input we have to convert the string to number by **parsing**:

```java live
import java.util.Scanner;
…
Scanner sc = new Scanner(System.in);
String name = sc.nextLine();
int age = Integer.parseInt(sc.nextLine());
double salary = Double.parseDouble(sc.nextLine());
```

## Printing to the Console
We can print to the console, using the System class:
* System.out.print();
* System.out.println();

### Example
```java live
Scanner sc = new Scanner(System.in);
System.out.print("Name: ");
String name = sc.nextLine();
System.out.println("Hi, " + name);
```

The program will run in the **following** way: 
- **It starts** by asking to type in any name. 
- When we type in a name, the program concatenate and print on the console `Hi, George`. 

[/slide]

[slide]
# Using Print Format
We ca use **format** to print at the console:

```java live
String name = "George";
int age = 5;
System.out.printf("Name: %s, Age: %d", name, age);
```
* In that example we have a person with name `George` and age `5`.
* On the last line we print person's name and age, where `%s` stands for string and correspond to **name**. Here `%d` stands for integer number and corresponds to **age**.

# Formatting Numbers in Placeholders
We can format number to certain digits with leading zeros using **d**.

We can format floating point number with certain digits after the decimal point **f**.

```java live
int percentage = 55;
double grade = 5.5334;
System.out.printf("%03d", percentage);
System.out.printf("%.2f", grade);
```
* In that example we have two numbers **int** `55` and **double** `5.5334`.
* On the last two lines we use `%03d` to format first number to `055`, and we use `%.2f` to format second number to `5.53`.

# Using String.format
In the example below we use **String.format** to create a string by pattern.

```java live
String name = "George";
int age = 5;
String result = String.format("Name: %s,Age: %d", name, age);
System.out.println(result);
```
* In that example we have a person with name `George` and age `5`.
* On the next line we create a new **string** variable, named `result` where we use **String.format** to format our output message.
* On the last line we print `result`.

[/slide]


[slide]
# Student Information
[code-task title="Student Information" taskId="java-fundamentals-basic-syntax-lesson-1" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
You will be given 3 lines of input – student name, age and average grade.

Your task is to print all the info about the student in the following format:
* **"Name: \{student name\}, Age: \{student age\}, Grade: \{student grade\}"**. 

## Examples
|**Input**|**Output**|
|-----|------|
| John | Name: John, Age: 15, Grade: 5.40 |
| 15 ||
| 5.40 ||

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John
15
5.40
[/input]
[output]
Name: John, Age: 15, Grade: 5.40
[/output]
[/test]
[test]
[input]
Steve
16
2.50
[/input]
[output]
Name: Steve, Age: 16, Grade: 2.50
[/output]
[/test]
[test]
[input]
Marry
12
6.00
[/input]
[output]
Name: Marry, Age: 12, Grade: 6.00
[/output]
[/test]
[test]
[input]
Mary
12
6.00
[/input]
[output]
Name: Mary, Age: 12, Grade: 6.00
[/output]
[/test]
[test]
[input]
Marrys
12
6.00
[/input]
[output]
Name: Marrys, Age: 12, Grade: 6.00
[/output]
[/test]
[test]
[input]
Steves
16
2.50
[/input]
[output]
Name: Steves, Age: 16, Grade: 2.50
[/output]
[/test]
[test]
[input]
John
18
5.40
[/input]
[output]
Name: John, Age: 18, Grade: 5.40
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide]
# Solution: Student Information
[code-task title="Student Information" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
 public static void main(String[] args) {
  Scanner scanner = new Scanner(System.in);
  String name = scanner.nextLine();
  int age = Integer.valueOf(scanner.nextLine());
  double grade = Double.valueOf(scanner.nextLine());

  System.out.printf("Name: %s, Age: %d, Grade: %.2f", name, age, grade);
 }
}
```
[/code-editor]
[task-description]
## Description
You will be given 3 lines of input – student name, age and average grade.

Your task is to print all the info about the student in the following format:
* **"Name: \{student name\}, Age: \{student age\}, Grade: \{student grade\}"**. 

## Examples
|**Input**|**Output**|
|-----|------|
| John | Name: John, Age: 15, Grade: 5.40 |
| 15 ||
| 5.40 ||

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John
15
5.40
[/input]
[output]
Name: John, Age: 15, Grade: 5.40
[/output]
[/test]
[test]
[input]
Steve
16
2.50
[/input]
[output]
Name: Steve, Age: 16, Grade: 2.50
[/output]
[/test]
[test]
[input]
Marry
12
6.00
[/input]
[output]
Name: Marry, Age: 12, Grade: 6.00
[/output]
[/test]
[test]
[input]
Mary
12
6.00
[/input]
[output]
Name: Mary, Age: 12, Grade: 6.00
[/output]
[/test]
[test]
[input]
Marrys
12
6.00
[/input]
[output]
Name: Marrys, Age: 12, Grade: 6.00
[/output]
[/test]
[test]
[input]
Steves
16
2.50
[/input]
[output]
Name: Steves, Age: 16, Grade: 2.50
[/output]
[/test]
[test]
[input]
John
18
5.40
[/input]
[output]
Name: John, Age: 18, Grade: 5.40
[/output]
[/test]
[/tests]
[/code-task]
[/slide]