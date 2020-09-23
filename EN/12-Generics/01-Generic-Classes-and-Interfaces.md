# Generic Classes and Interfaces

[slide]

# Generic Classes

We can define our own classes with generics type.

A generic type is a class or interface that is parameterized over types.

In the generic class declarations, the name of the class is followed by the type parameter section. 

The type parameter, also known as the type variable, is an identifier used to specify a generic type name. 

The type parameter section of the generic class can include one or more type parameters that are separated by commas. 

These classes are also known as parameterized classes.

In the following example, we have a generic class Container which accepts one type parameter:

```java
public class Container<T> {

    private List<T> items;

    public void addItem(T item) {
        this.items.add(item);
    }

    public boolean removeItem(T item) {
        return this.items.remove(item);
    }
}
```

Multiple Type Parameters Example:

```java
public class Container<K,V> {

    private HashMap<K,V> items;

    public void addItem(K key, V value) {
        this.items.put(key,value);
    }

    public boolean removeByKey(K key, V value) {
        return this.items.remove(key, value);
    }
}
```
[/slide]

[slide]
# Problem: Jar of T
[code-task title="Problem: Jar of T" taskId="11709b5a-e400-4da9-8b47-1cb8af706312" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Java - Unit Testing Strategy needed
    }
}
```
[/code-editor]
[task-description]
## Description
Create a class Jar<> that can store anything.
It should have two public methods:
- void add(element)
- element remove()
Adding should add on top of its contents. Remove should get the topmost element.

## Examples
[image assetsSrc="generics-example(1).png" /]

## Submit
To submit your solution, **zip** your whole package with the **Jar** and **Main classes**:

[image assetsSrc="generics-example(2).png" /]

If you didn't create **package** just choose your classes and **zip** them.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
import org.junit.Assert;
import org.junit.Test;

public class P01_ZeroTest \{

    @Test
    public void test() throws NoSuchMethodException \{
        Assert.assertTrue("Class 'Jar' not found", Classes.allClasses.containsKey("Jar"));
        Class cl = Classes.allClasses.get("Jar");
	Assert.assertTrue("Jar class has no type parameters", cl.getTypeParameters().length \> 0);
        cl.getDeclaredMethod("add", Object.class);
        cl.getDeclaredMethod("remove");
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

public class P01_TestAddInt \{

    @Test
    public void test() throws NoSuchMethodException, IllegalAccessException, InstantiationException, InvocationTargetException \{
        Class\<?\> cl = Classes.allClasses.get("Jar");
	Assert.assertTrue(cl.getTypeParameters().length \> 0);
        Method add = cl.getMethod("add", Object.class);
        Method remove = cl.getMethod("remove");
        Object jar = cl.newInstance();
        add.invoke(jar, 123);
        Integer result = (Integer) remove.invoke(jar);
        Assert.assertTrue(result.equals(123));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

public class P01_TestAddString \{

    @Test
    public void test() throws NoSuchMethodException, IllegalAccessException, InstantiationException, InvocationTargetException \{
        Class\<?\> cl = Classes.allClasses.get("Jar");
	Assert.assertTrue(cl.getTypeParameters().length \> 0);
        Method add = cl.getMethod("add", Object.class);
        Method remove = cl.getMethod("remove");
        Object jar = cl.newInstance();
        add.invoke(jar, "123");
        String result = (String) remove.invoke(jar);
        Assert.assertTrue(result.equals("123"));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

public class P01_TestAddFloat \{

    @Test
    public void test() throws NoSuchMethodException, IllegalAccessException, InstantiationException, InvocationTargetException \{
        Class\<?\> cl = Classes.allClasses.get("Jar");
        Assert.assertTrue(cl.getTypeParameters().length \> 0);
        Method add = cl.getMethod("add", Object.class);
        Method remove = cl.getMethod("remove");
        Object jar = cl.newInstance();
        add.invoke(jar, 123.2f);
        Float result = (Float) remove.invoke(jar);
        Assert.assertTrue(result.equals(123.2f));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

public class P01_TestAddDouble \{

    @Test
    public void test() throws NoSuchMethodException, IllegalAccessException, InstantiationException, InvocationTargetException \{
        Class\<?\> cl = Classes.allClasses.get("Jar");
        Assert.assertTrue(cl.getTypeParameters().length \> 0);
        Method add = cl.getMethod("add", Object.class);
        Method remove = cl.getMethod("remove");
        Object jar = cl.newInstance();
        add.invoke(jar, 123.2);
        Double result = (Double) remove.invoke(jar);
        Assert.assertTrue(result.equals(123.2));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

public class P01_TestAddBoolean \{

    @Test
    public void test() throws NoSuchMethodException, IllegalAccessException, InstantiationException, InvocationTargetException \{
        Class\<?\> cl = Classes.allClasses.get("Jar");
        Assert.assertTrue(cl.getTypeParameters().length \> 0);
        Method add = cl.getMethod("add", Object.class);
        Method remove = cl.getMethod("remove");
        Object jar = cl.newInstance();
        add.invoke(jar, false);
        add.invoke(jar, true);
        add.invoke(jar, false);
        boolean result = (boolean) remove.invoke(jar);
        Assert.assertTrue(!result);
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

# Generic Interfaces

A generic Java interface is an interface which can be typed - meaning it can be specialized to work with a specific type (e.g. interface or class) when used.

Generic interfaces are specified just like generic classes. 

For example:

```java
public interface Mathematics<T extends Number> {

    int powerOf(T number);
}
```
In the example above, we declare the Mathematics interface which declares the method `powerOf()`.

The type parameter `T` extends Number to restrict the type of objects that can be used in the parameterized type.

The `Number` is a superclass of all numeric classes, such as `Integer`, `Float` and `Double`.

So, if we try to use another class which is **not a subclass of Number**, the compiler will throw `compile-time-error`.




[/slide]

