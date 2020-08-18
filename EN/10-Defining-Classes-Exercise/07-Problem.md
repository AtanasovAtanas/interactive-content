[slide hideTitle]
# Problem: Family Tree
[code-task title="Family Tree" taskId="102bcf46-b2bb-4218-b78d-86641c10eeec" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
*You want to build your family tree, so you went to ask your grandmother. Sadly your grandmother keeps remembering information about your predecessors in pieces, so it falls to you to group the information and build the family tree.*

On the first line of the input, you will receive either a name or a birthdate in the format:

`<FirstName> <LastName>` or `day/month/year`

Your task is to find information about the person in the family tree. 

On the next lines, until the command `End`, you will receive information about your predecessors that is needed for the family tree.

The information will be in one of the following formats:

- `firstName lastName - firstName lastName`
- `firstName lastName - day/month/year`
- `day/month/year - firstName lastName`
- `day/month/year - day/month/year`
- `firstName lastName day/month/year`

The first 4 formats reveal a family tie: 

The person **on the left** is the **parent** to the person **on the right**.

The format can be **without names**. 

For example, the 4th format means the person **born on the left date** is the **parent to the person born on the right** date. 

The last format ties **different** information together – i.e. **the person with that name was born on that date**. 

**Names** and **birthdates** are **unique** – there won't be two persons with the same name or birthdate. 

There will **always** be enough entries to construct the family tree (all people names and birthdates are known and they have **at least one** connection to another person in the tree).

After the command `End` is received you should print all information about the person whose name or birthdate you received on the first line – his **name, birthday, parents, and children** (check the examples for the format). 

The people in the parents and children lists should be **ordered** by their **first appearance** in the input.

Regardless if they appeared as a birthdate or a name. 

For example in the first input Stan is before Jenny because his birthdate appeared first in the second line, while she appeared in the third line.

## Examples
| **Input** | **Output** |
| --- | --- |
| John Baker | John Baker 23/05/1980 |
| 11/11/1951 - 23/05/1980 | Parents: |
| Jenny Baker - 23/05/1980 | Stan Baker 11/11/1951 |
| Jenny Baker 09/02/1953 | Jenny Baker 09/02/1953 |
| John Baker - Garrett Baker | Children: |
| Garrett Baker 01/01/2005 | Garrett Baker 01/01/2005 |
| Stan Baker 11/11/1951 |  |
| John Baker 23/05/1980 |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| 13/12/1993 | Christopher Williams 13/12/1993 |
| 25/03/1934 - 04/04/1961 | Parents: |
| Leonard Williams 25/03/1934 | Benjamin Williams 04/04/1961 |
| 04/04/1961 - Christopher Williams | Children: |
| Benjamin Williams - Edward Williams |  |
| Christopher Williams 13/12/1993 |  |
| Edward Williams 07/07/1995 |  |
| Benjamin Williams 04/04/1961 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John Baker
11/11/1951 - 23/05/1980
Jenny Baker - 23/05/1980
Jenny Baker 09/02/1953
John Baker - Garrett Baker
Garrett Baker 01/01/2005
Stan Baker 11/11/1951
John Baker 23/05/1980
End
[/input]
[output]
John Baker 23/05/1980
Parents:
Stan Baker 11/11/1951
Jenny Baker 09/02/1953
Children:
Garrett Baker 01/01/2005
[/output]
[/test]
[test open]
[input]
13/12/1993
25/03/1934 - 04/04/1961
Leonard Williams 25/03/1934
04/04/1961 - Christopher Williams
Benjamin Williams - Edward Williams
Christopher Williams 13/12/1993
Edward Williams 07/07/1995
Benjamin Williams 04/04/1961
End
[/input]
[output]
Christopher Williams 13/12/1993
Parents:
Benjamin Williams 04/04/1961
Children:
[/output]
[/test]
[test]
[input]
17/8/1950
P0 P - P8 P
P0 P 17/8/1950
P8 P - P1 P
P1 P 17/10/2001
26/5/1948 - P2 P
P2 P 13/5/1973
17/2/1952 - P P
P3 P 17/2/1952
P11 P - P4 P
P4 P 16/7/1998
26/5/1948 - P5 P
P5 P 21/1/1973
26/5/1948 - P5 P
P6 P 26/5/1948
21/1/1973 - P7 P
P7 P 18/10/2002
26/5/1948 - 28/1/1974
P8 P 28/1/1974
26/5/1948 - 23/4/1973
P9 P 23/4/1973
13/5/1973 - P10 P
P10 P 16/11/1998
P6 P - P11 P
P11 P 24/4/1977
24/7/1951 - 21/1/1973
P12 P 24/7/1951
End
[/input]
[output]
P0 P 17/8/1950
Parents:
Children:
P8 P 28/1/1974
[/output]
[/test]
[test]
[input]
6/9/1927
P7 P - 12/1/1974
P0 P 12/1/1974
17/2/1950 - 10/3/1975
P1 P 10/3/1975
P10 P - P2 P
P2 P 26/5/1924
17/2/1950 - P3 P
P3 P 28/12/1973
P1 P - 21/9/1998
P4 P 21/9/1998
P1 P - P5 P
P5 P 27/11/1998
P10 P - P6 P
P6 P 6/9/1927
P2 P - 17/2/1950
P7 P 17/2/1950
28/12/1973 - P8 P
P8 P 12/12/1999
P10 P - 10/7/1927
P9 P 10/7/1927
6/9/1900 - P9 P
P10 P 6/9/1900
End
[/input]
[output]
P6 P 6/9/1927
Parents:
P10 P 6/9/1900
Children:
[/output]
[/test]
[test]
[input]
Abc12 Abcde
3/10/1927 - 23/10/1951
Abc0 Abcde 3/10/1927
3/4/1923 - Abc1 Abcde
Abc1 Abcde 26/8/1951
3/10/1927 - Abc2 Abcde
Abc2 Abcde 24/6/1948
Abc4 Abcde - 5/2/1998
Abc3 Abcde 5/2/1998
Abc1 Abcde - 4/3/1977
Abc4 Abcde 4/3/1977
3/10/1927 - Abc5 Abcde
Abc5 Abcde 6/3/1951
Abc4 Abcde - 16/12/1998
Abc6 Abcde 16/12/1998
3/4/1923 - Abc7 Abcde
Abc7 Abcde 23/10/1951
Abc4 Abcde - 10/2/1999
Abc8 Abcde 10/2/1999
Abc4 Abcde - 23/11/2001
Abc9 Abcde 23/11/2001
Abc4 Abcde - 18/8/2000
Abc10 Abcde 18/8/2000
Abc4 Abcde - 21/6/2002
Abc11 Abcde 21/6/2002
Abc12 Abcde 3/4/1923
4/3/1977 - Abc13 Abcde
Abc13 Abcde 2/6/2001
End
[/input]
[output]
Abc12 Abcde 3/4/1923
Parents:
Children:
Abc1 Abcde 26/8/1951
Abc7 Abcde 23/10/1951
[/output]
[/test]
[test]
[input]
9/9/1975
Abc9 Abcde - 14/12/1948
Abc0 Abcde 14/12/1948
Abc9 Abcde - Abc1 Abcde
Abc1 Abcde 6/11/1952
Abc9 Abcde - Abc2 Abcde
Abc2 Abcde 10/6/1951
Abc6 Abcde - Abc3 Abcde
Abc3 Abcde 1/5/1999
Abc9 Abcde - Abc4 Abcde
Abc4 Abcde 20/8/1949
10/6/1951 - Abc5 Abcde
Abc5 Abcde 5/8/1973
14/12/1948 - Abc6 Abcde
Abc6 Abcde 9/9/1975
14/12/1948 - 14/1/1975
Abc7 Abcde 14/1/1975
Abc1 Abcde - Abc8 Abcde
Abc8 Abcde 7/10/1976
Abc9 Abcde - Abc1 Abcde
Abc9 Abcde 11/5/1925
Abc4 Abcde - 9/5/1976
Abc10 Abcde 9/5/1976
End
[/input]
[output]
Abc6 Abcde 9/9/1975
Parents:
Abc0 Abcde 14/12/1948
Children:
Abc3 Abcde 1/5/1999
[/output]
[/test]
[test]
[input]
14/6/1950
21/9/1899 - Abc9 Abcde
Abc0 Abcde 21/9/1899
22/2/1898 - 17/12/1924
Abc1 Abcde 17/12/1924
21/9/1899 - 11/2/1925
Abc2 Abcde 11/2/1925
22/2/1898 - Abc3 Abcde
Abc3 Abcde 20/7/1927
22/2/1898 - 11/2/1925
Abc4 Abcde 22/2/1898
19/6/1901 - 11/11/1926
Abc5 Abcde 11/11/1926
Abc5 Abcde - Abc6 Abcde
Abc6 Abcde 27/8/1952
14/6/1950 - 26/9/1974
Abc7 Abcde 26/9/1974
Abc2 Abcde - Abc8 Abcde
Abc8 Abcde 14/6/1950
Abc4 Abcde - Abc9 Abcde
Abc9 Abcde 17/3/1923
Abc10 Abcde - 17/12/1924
Abc10 Abcde 19/6/1901
End
[/input]
[output]
Abc8 Abcde 14/6/1950
Parents:
Abc2 Abcde 11/2/1925
Children:
Abc7 Abcde 26/9/1974
[/output]
[/test]
[/tests]
[/code-task]
[/slide]