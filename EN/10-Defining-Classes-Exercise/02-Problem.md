[slide]
# Problem: Company Roster
[code-task title="Problem: Company Roster" taskId="76597424-6663-4f2d-b5d1-cb23dff0383e" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Define a class **Employee** that holds the following information: **name, salary, position, department, email** and **age**.

The **name, salary, position** and **department** are **mandatory** while the rest are **optional**.

Your task is to write a program which takes **N** lines of information about employees from the console and calculates the department with the highest average salary and prints for each employee in that department his **name, salary, email and age** - **sorted by salary in descending order**. 

If an employee **does not have** an **email** – in place of that field you should print **"n/a"** instead, if he does not have an **age** – print **"-1"** instead. 

The **salary** should be printed to **two decimal places** after the separator.

**Hint**: you can define a **Department** class that holds a list of employees.

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 | Highest Average Salary: Development |
| Peter 2200.00 Dev Development peter@softuni.org 28 | John 4400.20 john@john.com -1 |
| Tom 3300.00 Manager Marketing 33 | Peter 2200.00 peter@softuni.org 28 |
| John 4400.20 ProjectLeader Development john@john.com |  |
| Philip 0.20 Freelancer Nowhere 18 |  |

| **Input** | **Output** |
| --- | --- |
| 6 | Highest Average Salary: Sales |
| Stan 4960.37 Temp Coding stan@yahoo.com | Jimmy 6100.13 n/a -1 |
| Jimmy 6100.13 Manager Sales | Alex 6090.99 alex@softuni.org 44 |
| Alex 6090.99 Manager Sales alex@softuni.org 44 |  |
| Victoria 0.02 Director BeerDrinking victoria@gmail.com 23 |  |
| Andrew 7000.00 Director Coding |  |
| Peyton 130.3333 Sailor SpinachGroup peyton@softuni.org |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4
Peter 2200.00 Dev Development peter@softuni.org 28
Tom 3300.00 Manager Marketing 33
John 4400.20 ProjectLeader Development john@john.com
Philip 0.20 Freelancer Nowhere 18
[/input]
[output]
Highest Average Salary: Development
John 4400.20 john@john.com -1
Peter 2200.00 peter@softuni.org 28
[/output]
[/test]
[test open]
[input]
6
Stan 4960.37 Temp Coding stan@yahoo.com
Jimmy 6100.13 Manager Sales
Alex 6090.99 Manager Sales alex@softuni.org 44
Victoria 0.02 Director BeerDrinking victoria@gmail.com 23
Andrew 7000.00 Director Coding
Peyton 130.3333 Sailor SpinachGroup peyton@softuni.org
[/input]
[output]
Highest Average Salary: Sales
Jimmy 6100.13 n/a -1
Alex 6090.99 alex@softuni.org 44
[/output]
[/test]
[test]
[input]
6
Michael 1300.01 Dev Development michael@softuni.org 28
Jeremy 1200.01 QA Testing jeremy@softuni.org 21
Trevor 1300.01 QA Testing trevor@gmail.com 23
Bethany 1300.02 QA Testing bethany@bethany.net 19
Stiven 1200.43 Dev Development stiven@yahoo.com 28
Sofia 1200.23 Dev Development sofia@softuni.org 28
[/input]
[output]
Highest Average Salary: Testing
Bethany 1300.02 bethany@bethany.net 19
Trevor 1300.01 trevor@gmail.com 23
Jeremy 1200.01 jeremy@softuni.org 21
[/output]
[/test]
[test]
[input]
6
Jacob 8400.20 ProjectLeader Development jacob@jacob.com
Bishop 1230.31 Manager Marketing bishop@gmail.com
Derek 3210.23 QA Testing derek@yahoo.com
Bobby 310.1 ProjectLeader Testing bobby@bobby.net
Phil 0.23 NoWhere StreetWork kodko@street.bg
Ed 11000.33 Dev Development ed@softuni.org
[/input]
[output]
Highest Average Salary: Development
Ed 11000.33 ed@softuni.org -1
Jacob 8400.20 jacob@jacob.com -1
[/output]
[/test]
[test]
[input]
7
Ben 8400.20 ProjectLeader Development 123
Clark 1230.31 Manager Marketing  123
Wendy 3210.23 QA Testing 22
Andy 3100.1 ProjectLeader Testing 14
Sarah 0.23 NoWhere StreetWork 13
Abbigail 1100.33 Dev Development 12
Robert 9999.98 QADev Testing 13
[/input]
[output]
Highest Average Salary: Testing
Robert 9999.98 n/a 13
Wendy 3210.23 n/a 22
Andy 3100.10 n/a 14
[/output]
[/test]
[test]
[input]
3
Ed 1223.32 Dev Development email@email.em
Edward 1993.32 Dev Development 22
Edison 1223931.32 Dev Development email@email.em 44
[/input]
[output]
Highest Average Salary: Development
Edison 1223931.32 email@email.em 44
Edward 1993.32 n/a 22
Ed 1223.32 email@email.em -1
[/output]
[/test]
[test]
[input]
18
Stan 49665.37 Temp Coding stan@yahoo.com
Yasmin 610.1653 Manager Sales
Teodor 60659.99 Manager Sales teodor@tdr.com 44
Benjamin 0.0652 Trainer Training benjamin@ben.org 23
Penny 700.0650 Director Coding
Popeye 13.335433 Sailor Shipping popeye@pop.eu
Murphy 496.3734 Temp Coding murphy@yahoo.com
Kurt 610.13 Manager Sales kurt@gmail.com
Teodor 609.993 Manager Sales teodor@gmail.com 44
Victor 0.032 Director Sales sales@uni.eu 23
Andrew 700.03305 Director Coding
Popeye2 13.333333 Sailor Shipping popeye@pop.eu
Simon 496.3437 Temp Coding simon@yahoo.com
Donald 620.133333 Manager Sales 12
Duck 609.99 Manager Sales duck@gmail.com 44
Daffy 0.02 Director Training daffy@uni.eu 23
Duckk 702.00 Director Coding
Christopher 13.3333 Sailor SpinachGroup robin@pop.eu
[/input]
[output]
Highest Average Salary: Sales
Teodor 60659.99 teodor@tdr.com 44
Donald 620.13 n/a 12
Yasmin 610.17 n/a -1
Kurt 610.13 kurt@gmail.com -1
Teodor 609.99 teodor@gmail.com 44
Duck 609.99 duck@gmail.com 44
Victor 0.03 sales@uni.eu 23
[/output]
[/test]
[/tests]
[/code-task]
[/slide]