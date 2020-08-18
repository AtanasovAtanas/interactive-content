[slide]

# Defining Simple Classes

A class is the **basic building block of an object-oriented language** such as Java.

Everything in Java is associated with **classes** and **objects**, along with its attributes and **methods**. 

For example: in real life, a **car is an object**. 

The car has **attributes**, such as **weight** and **color**, and **methods**, such as **drive** and **brake**.

A **class is a template** that describes the **data** and **behaviour** associated with instances of that class.

When you instantiate a class you create an object that looks and feels like other instances of the same class. 

The data (**attributes**) associated with a class or object is stored in **variables**. 

The **behavior** associated with a class or object is implemented with **methods**. 

When defining class, it contains only those components of a class declaration that are required.

The obligatory components are:

- Keyword - `class`
- Class name
- Class body - between `{}`

Not obligatory, but credential, components are:

- Class fields
- Constructor
- Getters and Setters
- Class methods

Here is an example of a class Car which have two fields (**brand, model**) and one void method - `start()`.

```java
class Car {

    String brand;
    String model;

    void start(){ ... }
}
```
Below are the class naming rules of java programming language. 

They must be followed while developing software in java for good maintenance and readability of code. 

Class names should be nouns, in mixed case with the first letter of each internal word capitalized. 

Try to keep your class names simple and descriptive. 

Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML).




[/slide]