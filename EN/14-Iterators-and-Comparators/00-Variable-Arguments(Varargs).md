# Variable Arguments(Varargs)

[slide]

# Variable Arguments(Varargs)

Let’s suppose you are creating a Java method. 

However, you are not sure how many arguments your method is going to accept. 

To overcome this problem, Java 5 introduced varargs.

Varargs stands for variable arguments.

The varrags allows the method to accept zero or multiple arguments.

Let's see the following example:

```java

static void display(String... values) {  
  System.out.println("display method invoked");  
} 

static void main() {
  display();
  display("first");
  display("multiple", "Strings"); 
}

```

In the example above, the method named `display()` accepts varargs (of type String) and from the main method, we are invoking this method multiple times by passing a different number of arguments each time we invoke it.






[/slide]



[slide]

# Variable Arguments Rules


[/slide]