[slide]
# Problem: Grades
[code-task title="Grades" taskId="FLE-p-06" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
# Description
Write a program to calculate statistics of the exam grades. 

In the beginning, the program receives the number of students attended the examination and its grade for each student. 

In the end, the program should print the percentage of students with grade between 2.00 and 2.99, between 3.00 and 3.99, 4.00 and 4.99, and between 5.00 or more. 

Also the average grade of the exam.

# Input
Read from the console a series of numbers, each on a separate line:
- The first line - number of students attended the exam - an integer in the range \[1 ... 1000\]
- For each student on a separate line - grade of the exam - real number in the range \[2.00 ... 6.00\]

# Output
Print on the console 5 rows that contain the following information:
- "Top students: \{percent student with grade 5.00 or more\}%"
- "Between 4.00 and 4.99: \{between 4.00 and 4.99 inclusive\}%"
- "Between 3.00 and 3.99: \{between 3.00 and 3.99 inclusive\}%"
- "Fail: \{less than 3.00\}%"
- "Average: \{average grade\}"

All numbers must be formatted to the second decimal place.

# Example

| Input | | Output |
| --- | --- | --- | 
| 10 | | Top students: 30.00% |
| 3.00 | | Between 4.00 and 4.99: 30.00% |
| 2.99| | Between 3.00 and 3.99: 20.00% |
| 5.68| | Fail: 20.00% |
| 3.01| | Average: 4.06 |
| 4| | | 
| 4| | | 
| 6.00| |
| 4.50| |
| 2.44| |
| 5| | | 

## Comments
- Students with grade 5 and more – three = 30% of 10
- Between 4 and 4.99 – three = 30% of 10
- Between 3 and 3.99 – two = 20% of 10
- Less than 3 – two = 20% of 10

Average grade: 3 + 2.99 + 5.68 + 3.01 + 4 + 4 + 6 + 4.50 + 2.44 + 5 = 40.62 / 10 = 4.062
[/task-description]
[tests]
[test]
[input]
10
3
2.99
5.68
3.01
4
4
6
4.5
2.44
5
[/input]
[output]
Top students: 30.00%
Between 4.00 and 4.99: 30.00%
Between 3.00 and 3.99: 20.00%
Fail: 20.00%
Average: 4.06
[/output]
[/test]
[test]
[input]
6
2
3
4
5
6
2.2
[/input]
[output]
Top students: 33.33%
Between 4.00 and 4.99: 16.67%
Between 3.00 and 3.99: 16.67%
Fail: 33.33%
Average: 3.70
[/output]
[/test]
[test]
[input]
100
6
6
5
5
4
4
3
3
2
2
2.1
2.2
2.3
2.4
2.5
2.6
2.7
2.8
2.9
3
3.1
3.2
3.3
3.4
3.5
3.6
3.7
3.8
3.9
4
4.1
4.2
4.3
4.4
4.5
4.6
4.7
4.8
4.9
5
5.1
5.2
5.3
5.4
5.5
5.6
5.7
5.8
5.9
2.02
2.12
2.22
2.32
2.42
2.52
2.62
2.72
2.82
2.92
2.02
3.09
3.19
3.29
3.39
3.49
3.59
3.69
3.79
3.89
3.99
4.09
4.19
4.29
4.39
4.49
4.59
4.69
4.79
4.89
4.99
5.09
5.19
5.29
5.39
5.49
5.59
5.69
5.79
5.89
5.99
3
4.1
5.2
6.0
5.4
4.5
3.6
2.7
2.8
5.9
[/input]
[output]
Top students: 28.00%
Between 4.00 and 4.99: 24.00%
Between 3.00 and 3.99: 24.00%
Fail: 24.00%
Average: 4.02
[/output]
[/test]
[test]
[input]
263
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
5.9
6
6
5.7
5.8
5.5
5.4
6
5.88
5.88
5.88
5.88
5.88
5.3
5.3
5.3
5.75
5.85
5.63
5.63
5.63
5.63
5.63
5.63
5.06
5.96
5.5
5.5
5.5
5.5
5.5
5.5
5.5
5
5
5
4.7
5.41
5
4.6
5.31
4.51
4.88
4.5
4.63
4.3
4.95
4.5
4.75
4.75
4.27
4.25
4.25
4.25
4.25
4.25
4.25
4.25
4.25
4.25
4
4
4
4
4
4
4
4
4
4.13
4.13
3.88
4.15
3.36
3.33
3.13
3.13
3.75
3.75
3.75
3.03
3.02
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
[/input]
[output]
Top students: 50.57%
Between 4.00 and 4.99: 12.55%
Between 3.00 and 3.99: 29.28%
Fail: 7.60%
Average: 4.56
[/output]
[/test]
[test]
[input]
20
3
6
6
6
5.7
5.4
5.63
3
2
2
3
5.3
4
4.7
3
2
2
6
3
6
[/input]
[output]
Top students: 45.00%
Between 4.00 and 4.99: 10.00%
Between 3.00 and 3.99: 25.00%
Fail: 20.00%
Average: 4.19
[/output]
[/test]
[test]
[input]
15
3
3
2
2
3
2
5.7
6
6
5.4
5.3
4
3
2
6
[/input]
[output]
Top students: 40.00%
Between 4.00 and 4.99: 6.67%
Between 3.00 and 3.99: 26.67%
Fail: 26.67%
Average: 3.89
[/output]
[/test]
[test]
[input]
10
6
6
6
6
6
6
6
6
6
6
[/input]
[output]
Top students: 100.00%
Between 4.00 and 4.99: 0.00%
Between 3.00 and 3.99: 0.00%
Fail: 0.00%
Average: 6.00
[/output]
[/test]
[test]
[input]
10
6
3
6
6
6
6
6
6
6
5.3
[/input]
[output]
Top students: 90.00%
Between 4.00 and 4.99: 0.00%
Between 3.00 and 3.99: 10.00%
Fail: 0.00%
Average: 5.63
[/output]
[/test]
[test]
[input]
38
3
6
5.3
2
6
3
6
6
6
3
3.9
4.75
6
5.05
6
3
5.3
3.75
6
4.5
3
3
6
5
3
6
5.75
6
5.5
3
4
6
6
5
3
4
2
6
[/input]
[output]
Top students: 55.26%
Between 4.00 and 4.99: 10.53%
Between 3.00 and 3.99: 28.95%
Fail: 5.26%
Average: 4.65
[/output]
[/test]
[test]
[input]
22
2
2.90
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
[/input]
[output]
Top students: 0.00%
Between 4.00 and 4.99: 0.00%
Between 3.00 and 3.99: 0.00%
Fail: 100.00%
Average: 2.04
[/output]
[/test]
[test]
[input]
188
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
5.84
5.73
5.7
5.62
5.6
5.51
5.51
5.29
5.29
5.29
5.29
5.17
5.15
5.07
5.07
4.98
4.95
4.95
4.91
4.87
4.85
4.76
4.7
4.68
4.66
4.58
4.58
4.56
4.56
4.56
4.55
4.51
4.48
4.44
4.44
4.43
4.39
4.31
4.27
4.24
4.24
4.24
4.22
4.18
4.13
4.09
4.04
4.04
4.04
3.98
3.98
3.98
3.98
3.98
3.94
3.9
3.87
3.83
3.76
3.74
3.71
3.71
3.67
3.59
3.56
3.55
3.52
3.49
3.45
3.44
3.44
3.44
3.44
3.4
3.37
3.34
3.22
3.11
3.07
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
[/input]
[output]
Top students: 25.00%
Between 4.00 and 4.99: 18.09%
Between 3.00 and 3.99: 28.19%
Fail: 28.72%
Average: 3.78
[/output]
[/test]
[test]
[input]
267
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
6
5.97
5.97
5.95
5.89
5.73
5.73
5.73
5.62
5.56
5.54
5.45
5.35
5.35
5.23
5.22
5.19
5.18
5.18
5.16
5.15
5.12
5.09
5.08
5.07
5.07
5.07
5.07
5.07
5.07
5.03
5
4.99
4.95
4.9
4.87
4.81
4.81
4.77
4.77
4.77
4.75
4.74
4.73
4.73
4.7
4.67
4.66
4.64
4.64
4.64
4.64
4.64
4.64
4.64
4.64
4.64
4.59
4.59
4.55
4.54
4.54
4.54
4.53
4.53
4.53
4.53
4.53
4.53
4.53
4.52
4.51
4.5
4.49
4.45
4.43
4.42
4.42
4.37
4.36
4.32
4.31
4.29
4.29
4.26
4.24
4.24
4.21
4.2
4.19
4.17
4.15
4.14
4.14
4.09
4.09
4.09
4.09
4.08
4.08
4.06
4.04
4.03
4.03
4.01
3.98
3.98
3.98
3.95
3.93
3.91
3.91
3.89
3.87
3.87
3.87
3.87
3.86
3.85
3.76
3.75
3.74
3.7
3.68
3.67
3.65
3.65
3.65
3.65
3.62
3.6
3.55
3.55
3.55
3.55
3.55
3.55
3.55
3.55
3.55
3.55
3.55
3.52
3.47
3.46
3.46
3.45
3.44
3.44
3.44
3.44
3.44
3.44
3.44
3.39
3.37
3.35
3.34
3.33
3.33
3.32
3.31
3.29
3.22
3.22
3.21
3.2
3.14
3.07
3.04
3.03
3.03
3.02
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
3
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
2
[/input]
[output]
Top students: 24.72%
Between 4.00 and 4.99: 27.34%
Between 3.00 and 3.99: 32.96%
Fail: 14.98%
Average: 4.05
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]