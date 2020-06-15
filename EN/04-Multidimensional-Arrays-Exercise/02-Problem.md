[slide]
# Problem: Matrix of Palindromes
[code-task title="Problem: Matrix of Palindromes" taskId="74a5c710-6bb2-4a63-928a-c97f4022a2b7" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program to generate the following **matrix of palindromes** of **3** letters with **r** rows and **c** columns like the one in the examples below.

- **Rows** define the first and the last letter: row 0 -> 'a', row 1 ->'b', row 2 ->'c', ...
- **Columns + rows** define the middle letter:
  - column 0, row 0 -> 'a', column 1, row 0 -> 'b', column 2, row 0 -> 'c', ...
  - column 0, row 1 -> 'b', column 1, row 1 -> 'c', column 2, row 1 -> 'd', ...

## Input

- The numbers **r** and **c** stay at the first line at the input.
- **r** and **c** are integers in the range \[1 ... 26\].
- **r** + **c** <= 27

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 6 | aaa aba aca ada aea afa |
|  | bbb bcb bdb beb bfb bgb |
|  | ccc cdc cec cfc cgc chc |
|  | ddd ded dfd dgd dhd did |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 3 2 | aaa aba |
|  | bbb bcb |
|  | ccc cdc |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4 6
[/input]
[output]
aaa aba aca ada aea afa 
bbb bcb bdb beb bfb bgb 
ccc cdc cec cfc cgc chc 
ddd ded dfd dgd dhd did
[/output]
[/test]
[test open]
[input]
3 2
[/input]
[output]
aaa aba 
bbb bcb 
ccc cdc
[/output]
[/test]
[test]
[input]
3 8
[/input]
[output]
aaa aba aca ada aea afa aga aha 
bbb bcb bdb beb bfb bgb bhb bib 
ccc cdc cec cfc cgc chc cic cjc
[/output]
[/test]
[test]
[input]
1 26
[/input]
[output]
aaa aba aca ada aea afa aga aha aia aja aka ala ama ana aoa apa aqa ara asa ata aua ava awa axa aya aza
[/output]
[/test]
[test]
[input]
26 1
[/input]
[output]
aaa 
bbb 
ccc 
ddd 
eee 
fff 
ggg 
hhh 
iii 
jjj 
kkk 
lll 
mmm 
nnn 
ooo 
ppp 
qqq 
rrr 
sss 
ttt 
uuu 
vvv 
www 
xxx 
yyy 
zzz
[/output]
[/test]
[test]
[input]
13 14
[/input]
[output]
aaa aba aca ada aea afa aga aha aia aja aka ala ama ana 
bbb bcb bdb beb bfb bgb bhb bib bjb bkb blb bmb bnb bob 
ccc cdc cec cfc cgc chc cic cjc ckc clc cmc cnc coc cpc 
ddd ded dfd dgd dhd did djd dkd dld dmd dnd dod dpd dqd 
eee efe ege ehe eie eje eke ele eme ene eoe epe eqe ere 
fff fgf fhf fif fjf fkf flf fmf fnf fof fpf fqf frf fsf 
ggg ghg gig gjg gkg glg gmg gng gog gpg gqg grg gsg gtg 
hhh hih hjh hkh hlh hmh hnh hoh hph hqh hrh hsh hth huh 
iii iji iki ili imi ini ioi ipi iqi iri isi iti iui ivi 
jjj jkj jlj jmj jnj joj jpj jqj jrj jsj jtj juj jvj jwj 
kkk klk kmk knk kok kpk kqk krk ksk ktk kuk kvk kwk kxk 
lll lml lnl lol lpl lql lrl lsl ltl lul lvl lwl lxl lyl 
mmm mnm mom mpm mqm mrm msm mtm mum mvm mwm mxm mym mzm
[/output]
[/test]
[test]
[input]
14 13
[/input]
[output]
aaa aba aca ada aea afa aga aha aia aja aka ala ama 
bbb bcb bdb beb bfb bgb bhb bib bjb bkb blb bmb bnb 
ccc cdc cec cfc cgc chc cic cjc ckc clc cmc cnc coc 
ddd ded dfd dgd dhd did djd dkd dld dmd dnd dod dpd 
eee efe ege ehe eie eje eke ele eme ene eoe epe eqe 
fff fgf fhf fif fjf fkf flf fmf fnf fof fpf fqf frf 
ggg ghg gig gjg gkg glg gmg gng gog gpg gqg grg gsg 
hhh hih hjh hkh hlh hmh hnh hoh hph hqh hrh hsh hth 
iii iji iki ili imi ini ioi ipi iqi iri isi iti iui 
jjj jkj jlj jmj jnj joj jpj jqj jrj jsj jtj juj jvj 
kkk klk kmk knk kok kpk kqk krk ksk ktk kuk kvk kwk 
lll lml lnl lol lpl lql lrl lsl ltl lul lvl lwl lxl 
mmm mnm mom mpm mqm mrm msm mtm mum mvm mwm mxm mym 
nnn non npn nqn nrn nsn ntn nun nvn nwn nxn nyn nzn
[/output]
[/test]
[/tests]
[/code-task]
[/slide]