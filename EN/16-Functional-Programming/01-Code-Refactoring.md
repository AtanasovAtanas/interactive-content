[slide]

# Objects and Classes

# Using Objects and Classes Defining Simple Classes

<img src="img\ppt0.png" width=500px />

SoftUniTeam

Technical Trainers

Software University

[https://softuni\.bg](https://softuni.bg/)

# Table of Contents

* Objects
* Classes
* Built in Classes
* Defining Simple Classes
  * Fields
  * Constructors
  * Methods

# Have a Question?

_sli\.do_

__\#fund__  __\-__  __java__

<img src="img\ppt1.png" width=256px />

# Objects and Classes

# Objects

* An __object__ holds a set of named values
  * E\.g\. __birthday__ object holds day\, month and year
  * Creating a birthdayobject:

__LocalDate__  __birthday =__

__LocalDate\.of\(2018\, 5\, 5\)__  __;__

__System\.out\.println\(birthday\);__

<span style="color:#FFFFFF"> __Create a new object of type__ </span>  <span style="color:#FFFFFF"> __LocalDate__ </span>

# Classes

* In programming __classes__ provide the structure for __objects__
  * Act as a __blueprint__ for __objects__ of the same type
* Classes define:
  * __Fields__ \( __private variables__ \)\, e\.g\. day\,month\,year
  * __Getters/Setters__ \, e\.g\.getDay\,setMonth\,getYear
  * Actions \( __behavior__ \)\, e\.g\.plusDays\(count\)\,subtract\(date\)
* Typically a class has multiple __instances__ \(objects\)
  * Sample class: __LocalDate__
  * Sample objects: __birthdayPeter__ \, __birthdayMaria__

# Objects – Instances of Classes

Creating the object of a defined class iscalled __instantiation__

The __instance__ is the object itself\, which iscreatedruntime

All instances have common __behaviour__

__LocalDate__  __date1 =__  __LocalDate\.of__  __\(2018\, 5\, 5\);__

__LocalDate__  __date2 =__  __LocalDate\.of__  __\(2016\, 3\, 5\);__

__LocalDate__  __date3 =__  __LocalDate\.of__  __\(2013\, 3\, 2\);__

# Classes vs. Objects

Classes provide structure for creatingobjects

An object is a singleinstance of a class

__object__  __birthdayPeter__

__day = 27__

__month = 11__

__year = 1996__

__day: int__

__month: int__

__year: int__

__plusDays\(…\)__

__minusDays\(…\)__

<span style="color:#FFFFFF"> __Class__ </span>  __actions__  <span style="color:#FFFFFF"> __\(methods\)__ </span>

# Math, Random, BigInteger ...

# Using the Built-In API Classes

# Built-In API Classes in Java

* Java provides __ready\-to\-use__ classes:
  * Organized inside Packages like: __java\.util\.Scanner__ \, __java\.utils\.List__ \,etc\.
* Using static class members:
* Using non\-static Java classes:

LocalDateTimetoday=LocalDateTime\.now\(\);

doublecosine=Math\.cos\(Math\.PI\);

Randomrnd = newRandom\(\);

int randomNumber =rnd\.nextInt\(99\);

# Problem: Randomize Words

* You are given a list of words
  * Randomize their order and print each word on a separate line

<span style="color:#FFFFFF"> __Note: the output is a sample\. It should always be different\!__ </span>

Check your solution here:[https://judge\.softuni\.bg/Contests/1319/](https://judge.softuni.bg/Contests/1319/)

# Solution: Randomize Words

Scannersc= new Scanner\(System\.in\);

String\[\] words =sc\.nextLine\(\)\.split\(" "\);

Randomrnd =newRandom\(\);

for \(int pos1 = 0; pos1 < words\.length; pos1\+\+\) \{

int pos2 = rnd\.nextInt\(words\.length\);

_//_  _TODO:_  _Swap words\[pos1\] with words\[pos2\]_

\}

System\.out\.println\(String\.join\(

System\.lineSeparator\(\)\, words\)\);

Check your solution here:[https://judge\.softuni\.bg/Contests/1319/](https://judge.softuni.bg/Contests/1319/)

# Problem: Big Factorial

Calculaten\! \(nfactorial\) for very bign\(e\.g\. 1000\)

__30414093201713378043612608166064768844377641568960512000000000000__

__185482642257398439114796845645546284380220968949399346684421580986889562184028199319100141244804501828416633516851200000000000000000000__

Check your solution here:[https://judge\.softuni\.bg/Contests/1319/](https://judge.softuni.bg/Contests/1319/)

# Solution: Big Factorial

importjava\.math\.BigInteger;

\.\.\.

int n = Integer\.parseInt\(sc\.nextLine\(\)\);

BigIntegerf = newBigInteger\(String\.valueOf\(1\)\);

for \(int i = 1; i <= n; i\+\+\) \{

f = f\.multiply\(BigInteger\.valueOf\(Integer\.parseInt\(String\.valueOf\(i\)\)\)\);

\}

System\.out\.println\(f\);

<span style="color:#FFFFFF"> __Use the__ </span>  __java\.math\.BigInteger__

Check your solution here:[https://judge\.softuni\.bg/Contests/1319/](https://judge.softuni.bg/Contests/1319/)

<img src="img\ppt2.png" width=500px />

# Creating Custom Classes

# Defining Classes

# Defining Simple Classes

Specification of a given type of objectsfrom the real\-world

__Classes__ provide structure for describingand creating objects

classDice\{

…

\}

# Naming Classes

Use __PascalCase__ naming

Use __descriptive__ nouns

Avoid abbreviations \(except widely known\, e\.g\. URL\,HTTP\, etc\.\)

class Dice \{ … \}

classBankAccount\{ … \}

classIntegerCalculator\{ … \}

<img src="img\ppt3.png" width=128px />

class TPMF \{ … \}

classbankaccount\{ … \}

classintcalc\{ … \}

<img src="img\ppt4.png" width=256px />

# Class Members

Class is made up of __state__ and __behavior__

Fields __store values__

Methods __describe behaviour__

<img src="img\ppt5.png" width=482px />

class Dice \{

private intsides;

public void roll\(\) \{ … \}

\}

# Methods

Store executable code \(algorithm\)

class Dice \{

public int sides;

public int roll\(\) \{

Random rnd = new Random\(\);

int sides = rnd\.nextInt\(this\.sides \+ 1\);

returnsides;

\}

\}

<img src="img\ppt6.png" width=482px />

# Getters and Setters

class Dice \{

\. \. \.

publicintgetSides\(\)\{returnthis\.sides;\}

publicvoidsetSides\(int sides\)\{

this\.sides =sides;

\}

publicStringgetType\(\) \{return this\.type;\}

publicvoidsetType\(String type\) \{

this\.type = type;

\}

\}

<img src="img\ppt7.png" width=482px />

<span style="color:#FFFFFF"> __Getters & Setters__ </span>

# Creating an Object

A class can havemany __instances__ \(objects\)

<img src="img\ppt8.png" width=500px />

class Program \{

public static void main\(String\[\] args\) \{

DicediceD6 =new Dice\(\);

DicediceD8 =new Dice\(\);

\}

\}

<span style="color:#FFFFFF"> __Use the__ </span>  __new__  <span style="color:#FFFFFF"> __keyword__ </span>

<span style="color:#FFFFFF"> __Variable stores a__ </span>  __reference__

# Constructors

Special methods\, executed during object creation

<img src="img\ppt9.png" width=500px />

class Dice \{

public int sides;

public Dice\(\) \{

this\.sides = 6;

\}

\}

__Constructor__  __name__  <span style="color:#FFFFFF"> __is the same as the name of the class__ </span>

__Overloading__  <span style="color:#FFFFFF"> __default constructor__ </span>

# Constructors (2)

You can have multiple constructors in the same class

class Dice \{

public int sides;

publicDice\(\)\{ \}

publicDice\(intsides\)\{

this\.sides=sides;

\}

\}

class StartUp \{

public static void main\(String\[\] args\) \{

Dicedice1=new Dice\(\);

Dicedice2=new Dice\(7\);

\}

\}

# Problem: Students

* Read students until you receive " __end__ " in the following format:
  * " __\{__  __firstName__  __\} \{__  __lastName__  __\} \{age\} \{hometown\}__ "
  * Define a class __Student__ \, which holds the needed information
  * If you receive a student which already exists \(matching __firstName__ and __lastName__ \)\, overwrite the information
* After the end command\, you will receive a city name
* Print students which are from the given city in the format:" __\{__  __firstName__  __\} \{__  __lastName__  __\} is \{age\} years old\.__ "

# Solution: Students (1)

public Student\(String firstName\, String lastName\,int age\, String city\)\{

this\.firstName= firstName;

this\.lastName= lastName;

this\.age= age;

this\.city= city;

_//_  _TODO:_  _Implement Getters and Setters_

\}

List\<Student> students = new ArrayList<>\(\);

String line;

while \(\!line\.equals\("end"\)\) \{

_// TODO: Extract firstName\, lastName\, age\, city from the input_

StudentexistingStudent=getStudent\(students\,firstName\,lastName\);

if\(existingStudent\!= null\) \{

existingStudent\.setAge\(age\);

existingStudent\.setCity\(city\);

\} else \{

Student student = new Student\(firstName\, lastName\, age\, city\);

students\.add\(student\);

\}

line =sc\.nextLine\(\);

\}

static Student getStudent\(List\<Student> students\, String firstName\,

StringlastName\) \{

for \(Student student : students\)\{

if\(student\.getFirstName\(\)\.equals\(firstName\)

&&student\.getLastName\(\)\.equals\(lastName\)\)

return student;

\}

return null;

\}

<img src="img\ppt10.png" width=500px />

# Live Exercises

# Summary

* Classes define templates for object
  * __Fields__
  * __Constructors__
  * __Methods__
* Objects
  * Hold a set of __named values__
  * __Instance__ of a class

…

…

…

<img src="img\ppt11.png" width=500px />

# Questions?

# Trainings @ Software University (SoftUni)

* Software University – High\-Quality Education\, Profession and Job for Software Developers
  * [softuni\.bg](https://softuni.bg/)\,[about\.softuni\.bg](https://about.softuni.bg/)
* Software University Foundation
  * [softuni\.foundation](https://softuni.foundation/)
* Software University @ Facebook
  * [facebook\.com/SoftwareUniversity](https://www.facebook.com/SoftwareUniversity)
* Software University Forums
  * [forum\.softuni\.bg](https://forum.softuni.bg/)

# License

This course \(slides\, examples\, demos\, exercises\, homework\, documents\, videos and other assets\) is __copyrighted content__

Unauthorized copy\, reproduction or use is illegal

© SoftUni –[https://about\.softuni\.bg/](https://about.softuni.bg/)

© Software University –[https://softuni\.bg](https://softuni.bg/)

<img src="img\ppt12.png" width=223px />





[/slide]