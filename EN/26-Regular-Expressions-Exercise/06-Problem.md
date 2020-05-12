[slide hideTitle]
# Problem: Extract Emails
[code-task title="Extract Emails" taskId="db42c96a-8e71-437c-8795-39f2f2e0763e" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program to extract all email addresses from a given text.

The text comes at the **only input line**.

**Print the emails on the console**, each at a separate line.

Emails are considered to be in **format** \{user\}\@\{host\}, where: 

- \{user\} is a sequence of **letters and digits**, where '.', '-' and '_' can appear between them.
    - Examples of **valid users**: "stephan", "mike03", "s.johnson", "st_steward", "12345".
    - Examples of **invalid users**: ''--123", ".....", "_steve", ".info". 
- \{host\} is a **sequence of at least two words, separated by dots** '.'. Each word is **sequence of letters and can have hyphens** '-' between the letters.
    - Examples of **hosts**: "softuni.org", "software-university.com", "intoprogramming.info", "mail.softuni.org". 
    - Examples of **invalid hosts**: "helloworld", ".unknown.soft.", "invalid-host-", "invalid-". 
- Examples of **valid emails**: info\@softuni.org, kiki\@hotmail.co.uk, no-reply\@github.com, s.peterson\@mail.uu.net, info-bg\@software-university.software.academy. 
- Examples of **invalid emails**: --123\@gmail.com, …\@mail.bg, .info\@info.info, _steve\@yahoo.cn, mike\@helloworld, mike\@.unknown.soft., s.johnson\@invalid-.

### Example
| **Input** | **Output** |
| --- | --- |
| Just send email to s.miller@mit.edu and j.hopking@york.ac.uk for more information. | s.miller@mit.edu  |
| | j.hopking@york.ac.uk |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Please contact us at: support@github.com.
end
[/input]
[output]
support@github.com
[/output]
[/test]
[test]
[input]
Just send email to s.miller@mit.edu and j.hopking@york.ac.uk for more information.
end
[/input]
[output]
s.miller@mit.edu
j.hopking@york.ac.uk
[/output]
[/test]
[test]
[input]
Many users @ SoftUni confuse email addresses. We @ Softuni.BG provide high-quality training @ home or @ class. ?- steve.parker@softuni.de.
end
[/input]
[output]
steve.parker@softuni.de
[/output]
[/test]
[test]
[input]
Examples of valid emails: info@softuni-bulgaria.org, kiki@hotmail.co.uk, no-reply@github.com, s.peterson@mail.uu.net, info-bg@software-university.software.academy
end
[/input]
[output]

info@softuni-bulgaria.org
kiki@hotmail.co.uk
no-reply@github.com
s.peterson@mail.uu.net
info-bg@software-university.software.academy
[/output]
[/test]
[/tests]
[/code-task]
[/slide]