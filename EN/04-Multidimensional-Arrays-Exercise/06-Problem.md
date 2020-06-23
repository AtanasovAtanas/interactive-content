[slide]
# Problem: String Matrix Rotation
[code-task title="Problem: String Matrix Rotation" taskId="b2188470-e920-4c37-a906-b36702dd7f89" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given a **sequence of text lines**.

Assume these text lines form a **matrix of characters** (pad the missing positions with spaces to build a rectangular matrix).

Write a program to **rotate the matrix** by 90, 180, 270, 360, … degrees.

Print the result at the console as a sequence of strings after receiving the **"END"** command.

## Example

[image assetsSrc="string-matrix-rotation.png"/]

## Input

The input is read from the console:

- The first line holds the command in format **"Rotate(X)"** where **X** are the degrees of the requested rotation.
- The next lines contain the **lines of the matrix** for rotation.
- The input ends with the command **"END"**.

The input data will always be valid and in the format described. There is no need to check it explicitly.

## Output

Print at the console the **rotated matrix** as a sequence of text lines.

## Constraints

- The rotation **degrees** is positive integer in the range [0…90000], where **degrees** is **multiple of 90**.
- The number of matrix lines is in the range [1 ... **1 000**].
- The matrix lines are **strings** of length 1 ... 1 000.
- Allowed working time: 0.2 seconds. Allowed memory: 16 MB.

## Examples
| **Input** | **Output** |
| --- | --- |
| Rotate(90) | esh |
| hello | xoe |
| softuni | afl |
| exam | mtl |
| END |  uo |
|  |  n  |
|  |  i  |

| **Input** | **Output** |
| --- | --- |
| Rotate(180) |    maxe |
| hello | inutfos |
| softuni |   olleh |
| exam |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| Rotate(270) |  i  |
| hello |  n  |
| softuni | ou  |
| exam | ltm |
| END | lfa |
|  | eox |
|  | hse |

| **Input** | **Output** |
| --- | --- |
| Rotate(720) | js |
| js | exam |
| exam |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| Rotate(810) | ej |
| js | xs |
| exam | a |
| END | m |
|  |  |

| **Input** | **Output** |
| --- | --- |
| Rotate(0) | js |
| js | exam |
| exam |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Rotate(90)
hello
softuni
exam
END
[/input]
[output]
esh
xoe
afl
mtl
 uo
 n 
 i
[/output]
[/test]
[test open]
[input]
Rotate(180)
hello
softuni
exam
END
[/input]
[output]
maxe
inutfos
  olleh
[/output]
[/test]
[test open]
[input]
Rotate(270)
hello
softuni
exam
END
[/input]
[output]
i 
 n 
ou 
ltm
lfa
eox
hse
[/output]
[/test]
[test open]
[input]
Rotate(720)
js
exam
END
[/input]
[output]
js  
exam
[/output]
[/test]
[test open]
[input]
Rotate(810)
js
exam
END
[/input]
[output]
ej
xs
a 
m
[/output]
[/test]
[test open]
[input]
Rotate(0)
js
exam
END
[/input]
[output]
js  
exam
[/output]
[/test]
[test]
[input]
Rotate(90)
a
abc
abcdef
fadjkjerjghjhfgfs
gfsjkgfjjgfjgfjgfsjhgjfhsjhkfsd
safsfsfgfffgd
f
afggfagfgfa
fgffgdfgdfsgfgdsgfssfd
END
[/input]
[output]
fafsgfaaa
gf afabb 
fg fsdcc 
fg sjjd  
gf fkke  
da sgjf  
fg ffe   
gf gjr   
dg fjj   
ff fgg   
sa ffh   
g  gjj   
f  dgh   
g   ff   
d   jg   
s   gf   
g   fs   
f   s    
s   j    
s   h    
f   g    
d   j    
    f    
    h    
    s    
    j    
    h    
    k    
    f    
    s    
    d
[/output]
[/test]
[test]
[input]
Rotate(180)
a
abc
abcdef
fadjkjerjghjhfgfs
gfsjkgfjjgfjgfjgfsjhgjfhsjhkfsd
safsfsfgfffgd
f
afggfagfgfa
fgffgdfgdfsgfgdsgfssfd
END
[/input]
[output]
dfssfgsdgfgsfdgfdgffgf
                    afgfgafggfa
                              f
                  dgfffgfsfsfas
dsfkhjshfjghjsfgjfgjfgjjfgkjsfg
              sfgfhjhgjrejkjdaf
                         fedcba
                            cba
                              a
[/output]
[/test]
[test]
[input]
Rotate(270)
a
abc
abcdef
fadjkjerjghjhfgfs
gfsjkgfjjgfjgfjgfsjhgjfhsjhkfsd
safsfsfgfffgd
f
afggfagfgfa
fgffgdfgdfsgfgdsgfssfd
END
[/input]
[output]
d    
    s    
    f    
    k    
    h    
    j    
    s    
    h    
    f    
    j   d
    g   f
    h   s
    j   s
    s   f
   sf   g
   fg   s
   gj   d
   ff   g
   hgd  f
   jjg  g
   hff as
   ggf ff
   jjf gd
   rjg fg
   eff gf
  fjgs ad
  ekkf fg
  djjs gf
 ccdsf gf
 bbafa fg
aaafgsfaf
[/output]
[/test]
[test]
[input]
Rotate(450)
JavaScript (JS) is a dynamic computer programming language.
It is most commonly used as part of web browsers,
whose implementations allow client-side scripts
to interact with the user, control the browser,
communicate asynchronously,
and alter the document content that is displayed.
It is also being used in server-side network
programming (with Node.js),
game development and the
creation of desktop and mobile applications.
END
[/input]
[output]
cgpIactwIJ
rartnoohta
emo dm o v
aegi misia
t rsaunesS
ida lnt  c
oematieimr
nvmlecrmoi
 eisraapsp
olno tcltt
fog tete  
 p bh  mc(
dm(eeaweoJ
eewi sinmS
snindyttm)
kttgonhao 
t h cc tni
oa uuhtils
pnNsmrhoy 
 doeeoen a
a ddnn su 
nte tou sd
dh.i usaey
 ejncseldn
m s olrl a
o )sny,oam
b ,et, wsi
i  re c  c
l  vn ocp 
e  et nlac
   r  tiro
a  -t retm
p  sh on p
p  ia ltou
l  dt  -ft
i  e  ts e
c   i hiwr
a  ns ede 
t  e   ebp
i  td b  r
o  wi rsbo
n  os ocrg
s  rp wror
.  kl siwa
    a epsm
    y rtem
    e ,sri
    d   sn
    .   ,g
          
         l
         a
         n
         g
         u
         a
         g
         e
         .
[/output]
[/test]
[test]
[input]
Rotate(540)
JavaScript (JS) is a dynamic computer programming language.
It is most commonly used as part of web browsers,
whose implementations allow client-side scripts
to interact with the user, control the browser,
communicate asynchronously,
and alter the document content that is displayed.
It is also being used in server-side network
programming (with Node.js),
game development and the
creation of desktop and mobile applications.
END
[/input]
[output]
.snoitacilppa elibom dna potksed fo noitaerc
                                   eht dna tnempoleved emag
                                ,)sj.edoN htiw( gnimmargorp
               krowten edis-revres ni desu gnieb osla si tI
          .deyalpsid si taht tnetnoc tnemucod eht retla dna
                                ,ylsuonorhcnysa etacinummoc
            ,resworb eht lortnoc ,resu eht htiw tcaretni ot
            stpircs edis-tneilc wolla snoitatnemelpmi esohw
          ,sresworb bew fo trap sa desu ylnommoc tsom si tI
.egaugnal gnimmargorp retupmoc cimanyd a si )SJ( tpircSavaJ
[/output]
[/test]
[test]
[input]
Rotate(720)
JavaScript (JS) is a dynamic computer programming language.
It is most commonly used as part of web browsers,
whose implementations allow client-side scripts
to interact with the user, control the browser,
communicate asynchronously,
and alter the document content that is displayed.
It is also being used in server-side network
programming (with Node.js),
game development and the
creation of desktop and mobile applications.
END
[/input]
[output]
JavaScript (JS) is a dynamic computer programming language.
It is most commonly used as part of web browsers,          
whose implementations allow client-side scripts            
to interact with the user, control the browser,            
communicate asynchronously,                                
and alter the document content that is displayed.          
It is also being used in server-side network               
programming (with Node.js),                                
game development and the                                   
creation of desktop and mobile applications.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]