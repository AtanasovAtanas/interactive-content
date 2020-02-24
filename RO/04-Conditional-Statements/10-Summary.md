# Summary

[slide]
# Video

[vimeo-video startTimeInSeconds="9994" endTimeInSeconds="10210"]
[stream language="EN" videoId="341539841/456a08950e" /]
[stream language="RO" videoId="387657941/b7f1ede8f0" default /]
[/vimeo-video]

[/slide]

[slide]
# Summary

Numbers can be compared by the `==,` `<`, `>`, `<=`, `>=` and `!=` operators:
```java live
System.out.println(5 <= 10); 
```

Simple **if-conditions** check a condition and execute a code block if it is `true`:
```java live
Scanner scanner = new Scanner(System.in);
int a = Integer.parseInt(scanner.nextLine());

if (a > 5) {
    System.out.println("The number a is bigger than 5");
}
```

The **if-else** construction executes one of two blocks depending on whether a condition is `true` or `false`:
```java live
Scanner scanner = new Scanner(System.in);
int a = Integer.parseInt(scanner.nextLine());

if (a > 5) {
    System.out.println("The number `a` is bigger than 5");
} else {
    System.out.println("The number `a` is smaller or equal than 5");
}
```

If-else constructions can be chained as **if-else-if-else sequences**:
```java live
Scanner scanner = new Scanner(System.in);
int a = Integer.parseInt(scanner.nextLine());

if (a > 100) {
    System.out.println("The number `a` is bigger than 100");
} else if (a > 20) {
    System.out.println("The number `a` is bigger than 20");
} else {
    System.out.println("The number `a` is smaller or equal than 20");
}
```
[/slide]