[slide]
# Problem: Dragon Army
[code-task title="Problem: Dragon Army" taskId="edc53bdc-36c2-48f3-b89e-065386a43101" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Heroes III is the best game ever.

Everyone loves it and everyone plays it all the time.

John is no exclusion to this rule.

His favorite units in the game are all **types** of dragons – black, red, gold, azure etc... 

He likes them so much that he gives them **names** and keeps logs of their **stats** : **damage, health** and **armor**.

The process of aggregating all the data is quite tedious, so he would like to have a program doing it.

Since he is no programmer, it's your task to help him.

You need to categorize dragons by their **type**. 

For each dragon, identified by **name**, keep information about his **stats**. 

Type is **preserved** in the order of the input but dragons are **sorted** alphabetically by name. 

For each type, you should also print the average **damage**, **health** and **armor** of the dragons. 

For each dragon, print his own stats.

There **may** be **missing** stats in the input, though. 

If a stat is missing you should assign its default values. 

Default values are as follows: health **250** , damage **45** , and armor **10**. 

Missing stat will be marked by **null**.

The input is in the following format 

`{type} {name} {damage} {health} {armor}`

Any of the integers may be assigned **null** value. 

See the examples below for better understanding the task.

If the same dragon is added a second time, the new stats should **overwrite** the previous ones. 

Two dragons are considered **equal** if they match by **both** name and type.

## Input

- On the first line, you are given **number N** - the number of dragons
- On the **next N lines** you are given **input** in the **above described** format. There will be single space separating each element.

### Output

- Print the aggregated data on the console
- For each type, print average stats of its dragons in format 

`{Type}::({damage}/{health}/{armor})`

- Damage, health and armor should be rounded to two digits after the decimal separator
- For each dragon, print its stats in format **-{Name} -\> damage: {damage}, health: {health}, armor: {armor}**

### Constraints

- N is in the range [1 ... 100]
- The dragon type and name are one word only, starting with capital letter.
- Damage health and armor are integers in range [0 ... 100000] or **null**

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 | Red::(160.00/2350.00/30.00) |
| Red Bazgargal 100 2500 25 | -Bazgargal -> damage: 100, health: 2500, armor: 25 |
| Black Dargonax 200 3500 18 | -Obsidion -> damage: 220, health: 2200, armor: 35 |
| Red Obsidion 220 2200 35 | Black::(200.00/3500.00/18.00) |
| Blue Kerizsa 60 2100 20 | -Dargonax -> damage: 200, health: 3500, armor: 18 |
| Blue Algordox 65 1800 50 | Blue::(62.50/1950.00/35.00) |
|  | -Algordox -> damage: 65, health: 1800, armor: 50 |
|  | -Kerizsa -> damage: 60, health: 2100, armor: 20 |


| **Input** | **Output** |
| --- | --- |
| 4 | Gold::(223.75/826.25/17.50) |
| Gold Zzazx null 1000 10 | -Ardrax -> damage: 100, health: 1055, armor: 50 |
| Gold Traxx 500 null 0 | -Traxx -> damage: 500, health: 250, armor: 0 |
| Gold Xaarxx 250 1000 null | -Xaarxx -> damage: 250, health: 1000, armor: 10 |
| Gold Ardrax 100 1055 50 | -Zzazx -> damage: 45, health: 1000, armor: 10 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
Red Bazgargal 100 2500 25
Black Dargonax 200 3500 18
Red Obsidion 220 2200 35
Blue Kerizsa 60 2100 20
Blue Algordox 65 1800 50
[/input]
[output]
Red::(160.00/2350.00/30.00)
-Bazgargal -\> damage: 100, health: 2500, armor: 25
-Obsidion -\> damage: 220, health: 2200, armor: 35
Black::(200.00/3500.00/18.00)
-Dargonax -\> damage: 200, health: 3500, armor: 18
Blue::(62.50/1950.00/35.00)
-Algordox -\> damage: 65, health: 1800, armor: 50
-Kerizsa -\> damage: 60, health: 2100, armor: 20
[/output]
[/test]
[test open]
[input]
4
Gold Zzazx null 1000 10
Gold Traxx 500 null 0
Gold Xaarxx 250 1000 null
Gold Ardrax 100 1055 50
[/input]
[output]
Gold::(223.75/826.25/17.50)
-Ardrax -\> damage: 100, health: 1055, armor: 50
-Traxx -\> damage: 500, health: 250, armor: 0
-Xaarxx -\> damage: 250, health: 1000, armor: 10
-Zzazx -\> damage: 45, health: 1000, armor: 10
[/output]
[/test]
[test]
[input]
10
Black Gosho 50 100 50
Black Gosho 50 100 50
Black Gosho 50 100 50
Black Gosho 50 100 50
Black Gosho 100 150 100
Red Pesho 80 160 80
Red Pesho 80 160 80
Red Pesho 80 160 80
Red Pesho 80 160 80
Red Pesho 200 260 280
[/input]
[output]
Black::(100.00/150.00/100.00)
-Gosho -\> damage: 100, health: 150, armor: 100
Red::(200.00/260.00/280.00)
-Pesho -\> damage: 200, health: 260, armor: 280
[/output]
[/test]
[test]
[input]
5
Green Stamat 150 215 123
Yellow Stamat 51 124 124
Blue PernishkiGeroi 13 151 15
Gold Dancho 148 1787 11
Purple Azis 89 12 1515
[/input]
[output]
Green::(150.00/215.00/123.00)
-Stamat -\> damage: 150, health: 215, armor: 123
Yellow::(51.00/124.00/124.00)
-Stamat -\> damage: 51, health: 124, armor: 124
Blue::(13.00/151.00/15.00)
-PernishkiGeroi -\> damage: 13, health: 151, armor: 15
Gold::(148.00/1787.00/11.00)
-Dancho -\> damage: 148, health: 1787, armor: 11
Purple::(89.00/12.00/1515.00)
-Azis -\> damage: 89, health: 12, armor: 1515
[/output]
[/test]
[test]
[input]
15
Black Motichkata 150 12115 124
Purple Motichkata 105 124 1412
Black Asencho 121 12412 155
Black Mitaka 17 782 989
Green Parvan 115 1000 100
Purple Stoqn 151 12412 113
Purple Asencho 128 889 909
Green Bochko 124 56 1947
Purple Bochko 1948 909 1231
Black Motichkata 150 12115 124
Purple Motichka 105 1242 1412
Black Assencho 2121 12412 155
Black Shmitaka 17 782 989
Green Parvanka 1115 10020 100
Purple Stoqnka 151 12412 113
[/input]
[output]
Black::(485.20/7700.60/482.40)
-Asencho -\> damage: 121, health: 12412, armor: 155
-Assencho -\> damage: 2121, health: 12412, armor: 155
-Mitaka -\> damage: 17, health: 782, armor: 989
-Motichkata -\> damage: 150, health: 12115, armor: 124
-Shmitaka -\> damage: 17, health: 782, armor: 989
Purple::(431.33/4664.67/865.00)
-Asencho -\> damage: 128, health: 889, armor: 909
-Bochko -\> damage: 1948, health: 909, armor: 1231
-Motichka -\> damage: 105, health: 1242, armor: 1412
-Motichkata -\> damage: 105, health: 124, armor: 1412
-Stoqn -\> damage: 151, health: 12412, armor: 113
-Stoqnka -\> damage: 151, health: 12412, armor: 113
Green::(451.33/3692.00/715.67)
-Bochko -\> damage: 124, health: 56, armor: 1947
-Parvan -\> damage: 115, health: 1000, armor: 100
-Parvanka -\> damage: 1115, health: 10020, armor: 100
[/output]
[/test]
[test]
[input]
6
Green Goshko 120 123 0
Yellow Goshko 120 125 null
Blue Pesho 989 1050 null
Blue Pesho 1000 10000 100
Green Goshko null null null
Yellow Goshko 10000 1000 100
[/input]
[output]
Green::(45.00/250.00/10.00)
-Goshko -\> damage: 45, health: 250, armor: 10
Yellow::(10000.00/1000.00/100.00)
-Goshko -\> damage: 10000, health: 1000, armor: 100
Blue::(1000.00/10000.00/100.00)
-Pesho -\> damage: 1000, health: 10000, armor: 100
[/output]
[/test]
[test]
[input]
100
Gold Mitio null 100 null
Green Goshko 1112 123 123
Gold Toncho 150 null 123
Gold Asan 14 null null
Green Toshko 124 7878 null
Purple Biserchko 149 787 817
Purple Doncho 89 1982 180
Gold Stoil 888 109 1231
Green Boko null 1230 123
Purple Todor null null null
Gold Mitio null 100 null
Green Goshko 1112 123 123
Gold Toncho 150 null 123
Gold Asan 14 null null
Green Toshko 124 7878 null
Purple Bissgerchko 149 787 817
Purple Dosgncho 89 1982 180
Gold Stosgil 888 109 1231
Green Boksgo null 1230 123
Purple Todsgor null null null
Gold Mitigso null 100 null
Green Goshkajko 1112 123 123
Gold Tonchado 150 null 125
Gold Asanak 1412 null null
Green Toshkod 12134 7878 null
Purple Biseadrchko 149 787 817
Purple Donadcho 829 1982 180
Gold Stoiadl 8881 109 1231
Green Bokxo null 11230 123
Purple Todqeor null null null
Gold Mitiqeo null 1100 null
Green Goshqeko 1112 1123 123
Gold Toncqeho 1560 null 123
Gold Asaqen 14 null null
Green Toshkqo 124 7878 null
Purple Bisqeerchko 1849 787 817
Purple Doneqcho 89 19882 180
Gold Stoqeil 888 109 12831
Green Bokoq null 1230 1823
Purple Todqeor null null null
Gold Mitieqo null 1080 null
Green Gosqehko 1112 1283 123
Gold Toneqcho 150 null 8123
Gold Asqean 14 null null
Green Tosheqko 1248 7878 null
Purple Biseqerchko 1849 787 817
Purple Doqencho 898 1982 180
Gold Stoqeil 888 1089 1231
Green Bokeo null 1230 8123
Purple Toeqdor null null null
Gold Mitieo null 1080 null
Green Goseqhko 1112 1823 123
Gold Tonqecho 150 null 123
Gold Asean 114 null null
Green Tosheqko 124 7878 null
Purple Bqeiserchko 1492 7827 817
Purple Deoncho 891 1982 180
Gold Stoeil 888 1029 1231
Green Bokeqo null 1230 123
Purple Toeqdor null null null
Gold Mitqeio null 1010 null
Green Goqeshko 1112 1223 123
Gold Tonqcho 150 null 2123
Gold Asaqen 214 null null
Green Toshkeqo 124 7878 null
Purple Biseqerchko 149 787 817
Purple Donqwcho 829 1982 180
Gold Stoaeil 888 1209 1231
Green Bafoko null 1230 123
Purple Torydor null null null
Gold Mitiro null 1020 null
Green Goshkory 1112 1523 123
Gold Tonchako 150 null 5123
Gold Asankaaa 154 null null
Green Toshako 1254 7878 null
Purple Biseraschko 1549 7587 817
Purple Doncaasdho 859 1982 180
Gold Stoilzl 888 19 1231
Green Bokokko null 1230 123
Purple Todorrr null null null
Gold Mitkio null 10150 null
Green Gosghko 1112 1123 123
Gold Toncaho 150 null 1223
Gold Asaan 1134 null null
Green Toashko 124 72878 null
Purple Bisggerchko 1429 7287 817
Purple Donacho 89 1982 1280
Gold Stoail 888 109 13231
Green Boadko null 12330 123
Purple Toaddor null null null
Gold Mitaio null 1020 null
Green Godashko 1112 1223 123
Gold Toncdaho 150 null 123
Gold Asaana 124 null null
Green Toddshko 124 7878 null
Purple Biseggrchko 1429 7287 817
Purple Donancho 819 12982 180
Gold Stoilka 888 1029 1231
Green Bokoa null 12230 1123
Purple Todaor null null null
[/input]
[output]
Gold::(638.00/734.89/1155.94)
-Asaan -\> damage: 1134, health: 250, armor: 10
-Asaana -\> damage: 124, health: 250, armor: 10
-Asan -\> damage: 14, health: 250, armor: 10
-Asanak -\> damage: 1412, health: 250, armor: 10
-Asankaaa -\> damage: 154, health: 250, armor: 10
-Asaqen -\> damage: 214, health: 250, armor: 10
-Asean -\> damage: 114, health: 250, armor: 10
-Asqean -\> damage: 14, health: 250, armor: 10
-Mitaio -\> damage: 45, health: 1020, armor: 10
-Mitieo -\> damage: 45, health: 1080, armor: 10
-Mitieqo -\> damage: 45, health: 1080, armor: 10
-Mitigso -\> damage: 45, health: 100, armor: 10
-Mitio -\> damage: 45, health: 100, armor: 10
-Mitiqeo -\> damage: 45, health: 1100, armor: 10
-Mitiro -\> damage: 45, health: 1020, armor: 10
-Mitkio -\> damage: 45, health: 10150, armor: 10
-Mitqeio -\> damage: 45, health: 1010, armor: 10
-Stoaeil -\> damage: 888, health: 1209, armor: 1231
-Stoail -\> damage: 888, health: 109, armor: 13231
-Stoeil -\> damage: 888, health: 1029, armor: 1231
-Stoiadl -\> damage: 8881, health: 109, armor: 1231
-Stoil -\> damage: 888, health: 109, armor: 1231
-Stoilka -\> damage: 888, health: 1029, armor: 1231
-Stoilzl -\> damage: 888, health: 19, armor: 1231
-Stoqeil -\> damage: 888, health: 1089, armor: 1231
-Stosgil -\> damage: 888, health: 109, armor: 1231
-Toncaho -\> damage: 150, health: 250, armor: 1223
-Toncdaho -\> damage: 150, health: 250, armor: 123
-Tonchado -\> damage: 150, health: 250, armor: 125
-Tonchako -\> damage: 150, health: 250, armor: 5123
-Toncho -\> damage: 150, health: 250, armor: 123
-Toncqeho -\> damage: 1560, health: 250, armor: 123
-Toneqcho -\> damage: 150, health: 250, armor: 8123
-Tonqcho -\> damage: 150, health: 250, armor: 2123
-Tonqecho -\> damage: 150, health: 250, armor: 123
Green::(910.74/6740.41/485.81)
-Bafoko -\> damage: 45, health: 1230, armor: 123
-Boadko -\> damage: 45, health: 12330, armor: 123
-Bokeo -\> damage: 45, health: 1230, armor: 8123
-Bokeqo -\> damage: 45, health: 1230, armor: 123
-Boko -\> damage: 45, health: 1230, armor: 123
-Bokoa -\> damage: 45, health: 12230, armor: 1123
-Bokokko -\> damage: 45, health: 1230, armor: 123
-Bokoq -\> damage: 45, health: 1230, armor: 1823
-Boksgo -\> damage: 45, health: 1230, armor: 123
-Bokxo -\> damage: 45, health: 11230, armor: 123
-Godashko -\> damage: 1112, health: 1223, armor: 123
-Goqeshko -\> damage: 1112, health: 1223, armor: 123
-Goseqhko -\> damage: 1112, health: 1823, armor: 123
-Gosghko -\> damage: 1112, health: 1123, armor: 123
-Goshkajko -\> damage: 1112, health: 123, armor: 123
-Goshko -\> damage: 1112, health: 123, armor: 123
-Goshkory -\> damage: 1112, health: 1523, armor: 123
-Goshqeko -\> damage: 1112, health: 1123, armor: 123
-Gosqehko -\> damage: 1112, health: 1283, armor: 123
-Toashko -\> damage: 124, health: 72878, armor: 10
-Toddshko -\> damage: 124, health: 7878, armor: 10
-Toshako -\> damage: 1254, health: 7878, armor: 10
-Tosheqko -\> damage: 124, health: 7878, armor: 10
-Toshkeqo -\> damage: 124, health: 7878, armor: 10
-Toshko -\> damage: 124, health: 7878, armor: 10
-Toshkod -\> damage: 12134, health: 7878, armor: 10
-Toshkqo -\> damage: 124, health: 7878, armor: 10
Purple::(525.37/3134.93/382.70)
-Biseadrchko -\> damage: 149, health: 787, armor: 817
-Biseggrchko -\> damage: 1429, health: 7287, armor: 817
-Biseqerchko -\> damage: 149, health: 787, armor: 817
-Biseraschko -\> damage: 1549, health: 7587, armor: 817
-Biserchko -\> damage: 149, health: 787, armor: 817
-Bisggerchko -\> damage: 1429, health: 7287, armor: 817
-Bisqeerchko -\> damage: 1849, health: 787, armor: 817
-Bissgerchko -\> damage: 149, health: 787, armor: 817
-Bqeiserchko -\> damage: 1492, health: 7827, armor: 817
-Deoncho -\> damage: 891, health: 1982, armor: 180
-Donacho -\> damage: 89, health: 1982, armor: 1280
-Donadcho -\> damage: 829, health: 1982, armor: 180
-Donancho -\> damage: 819, health: 12982, armor: 180
-Doncaasdho -\> damage: 859, health: 1982, armor: 180
-Doncho -\> damage: 89, health: 1982, armor: 180
-Doneqcho -\> damage: 89, health: 19882, armor: 180
-Donqwcho -\> damage: 829, health: 1982, armor: 180
-Doqencho -\> damage: 898, health: 1982, armor: 180
-Dosgncho -\> damage: 89, health: 1982, armor: 180
-Toaddor -\> damage: 45, health: 250, armor: 10
-Todaor -\> damage: 45, health: 250, armor: 10
-Todor -\> damage: 45, health: 250, armor: 10
-Todorrr -\> damage: 45, health: 250, armor: 10
-Todqeor -\> damage: 45, health: 250, armor: 10
-Todsgor -\> damage: 45, health: 250, armor: 10
-Toeqdor -\> damage: 45, health: 250, armor: 10
-Torydor -\> damage: 45, health: 250, armor: 10
[/output]
[/test]
[test]
[input]
1
Green Stamat null null null
[/input]
[output]
Green::(45.00/250.00/10.00)
-Stamat -\> damage: 45, health: 250, armor: 10
[/output]
[/test]
[test]
[input]
6
Green Abc 124 14 1
Green Def 189 199 19
Green Ghi 78 899 91
Green Jkl 91 24 234
Green Mno 15 151 8
Green Pqr 898 109 133
[/input]
[output]
Green::(232.50/232.67/81.00)
-Abc -\> damage: 124, health: 14, armor: 1
-Def -\> damage: 189, health: 199, armor: 19
-Ghi -\> damage: 78, health: 899, armor: 91
-Jkl -\> damage: 91, health: 24, armor: 234
-Mno -\> damage: 15, health: 151, armor: 8
-Pqr -\> damage: 898, health: 109, armor: 133
[/output]
[/test]
[test]
[input]
10
Purple Toshko 12 123 1234
Purple Asen 11 2222 333
Purple Rosko 55 141 42
Green Bastuncho 150 1500 550
Green Bastuncho 150 100 150
Green Bastuncho 140 150 550
Green Bastuncho 120 150 550
Purple Stamat 128 1242 155
Green Azsymbastun null null null
Yellow Stoil null null 0
[/input]
[output]
Purple::(51.50/932.00/441.00)
-Asen -\> damage: 11, health: 2222, armor: 333
-Rosko -\> damage: 55, health: 141, armor: 42
-Stamat -\> damage: 128, health: 1242, armor: 155
-Toshko -\> damage: 12, health: 123, armor: 1234
Green::(82.50/200.00/280.00)
-Azsymbastun -\> damage: 45, health: 250, armor: 10
-Bastuncho -\> damage: 120, health: 150, armor: 550
Yellow::(45.00/250.00/0.00)
-Stoil -\> damage: 45, health: 250, armor: 0
[/output]
[/test]
[test]
[input]
3
Green Boklik 0 0 0
Yellow Bokluk 0 0 0
Green Boklek 0 0 0
[/input]
[output]
Green::(0.00/0.00/0.00)
-Boklek -\> damage: 0, health: 0, armor: 0
-Boklik -\> damage: 0, health: 0, armor: 0
Yellow::(0.00/0.00/0.00)
-Bokluk -\> damage: 0, health: 0, armor: 0
[/output]
[/test]
[test]
[input]
5
Black Xxx null 100 null
Black Motko 100 null 100
Yellow Pichagata 15 155 null
Black Azis null null null
Green Bochko 100 1000 10
[/input]
[output]
Black::(63.33/200.00/40.00)
-Azis -\> damage: 45, health: 250, armor: 10
-Motko -\> damage: 100, health: 250, armor: 100
-Xxx -\> damage: 45, health: 100, armor: 10
Yellow::(15.00/155.00/10.00)
-Pichagata -\> damage: 15, health: 155, armor: 10
Green::(100.00/1000.00/10.00)
-Bochko -\> damage: 100, health: 1000, armor: 10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]