# Basic Streams in Java


[slide]

# Byte Streams

Java byte streams are used to perform input and output of 8-bit bytes.

Byte streams are the lowest level streams there are.

Their main characteristic is that they can read or write only one byte at a time. 

All of the byte streams descend from the InputStream and the OutputStream classes.

Though there are many classes related to byte streams but the most frequently used classes are, **FileInputStream** and **FileOutputStream**.

- Тhe **InputStream is a sequence of bytes finishing with -1**, which is a special character **marking the end of the file**.

## Picture

- The **OutputStream is consisted only of bytes**, which will be written.

## Picture


[/slide]

[slide]
# Problem: Copy Bytes

[/slide]

[slide]

# Character Streams

**Java Character streams** are used to perform input and output for **16-bit unicode**.

Though there are many classes related to character streams but the most frequently used classes are, **FileReader** and **FileWriter**. 

Though internally **FileReader uses FileInputStream** and **FileWriter uses FileOutputStream** but here the major difference is that FileReader **reads two bytes at a time** and FileWriter **writes two bytes at a time**.

In short the character streams can read and write from an input **character by character**.

- Let's see the following example:

Input and output streams are created by using FileReader and FileWriter classes in a **try-with-resources** block.

After declaring and assigning the character variable, by using the `inputStream.read()` method, the while loop has been started until the last character has been read from the input file.

In the scope of the loop, the characters, from the input files, are written to the output file by using the `outputStream.write()` method.


```java
String input = "C:\\input.txt";
String output = "C:\\output.txt";

try (FileReader inputStream = new FileReader(input);
             FileWriter outputStream = new FileWriter(output)) {

     int character;
     while ((character = inputStream.read()) != -1) {
         outputStream.write(character);
     }
} catch (FileNotFoundException ex) {
    System.out.println("Input file not found!");
} catch (IOException e) {
    e.printStackTrace();
}

```

## Combining Streams

- Character streams are often "**wrappers**" for byte streams:
    - FileReader uses FileInputStream
    - FileWriter uses FileOutputStream

```java
String path = "D:\\input.txt";

Scanner reader = new Scanner(new FileInputStream(path));
```

An example above is given with the `Scanner` class, which you have used for quite some time now.

Here is used to wrap a `FileInputStream` and, by now, you have done that by wrapping `System.in`, wich is nothing more but a constant holding an `InputStream`.

[/slide]

[slide]

# Buffered Streams 

The next layer of abstraction over the byte stream are Buffered Streams. 

The Streams we have seen so far use unbuffered I/O. 

This means each or write request is handled directly by the underlying Operating System.

This can make a program much less efficient, since each such request often triggers disk space, network activity, or some other operation that is relatively expensive.

To overcome this kind of overhead, the Java platform implements Buffered I/O Streams.

Buffered input streams read data from a memory area known as a buffer.

When the Buffered Stream is created, an internal buffer array is created.

Buffered stream can wrap a character stream and give us access to very powerful methods. 

There are four buffered stream classes used to wrap unbuffered streams:
 - **BufferedInputStream** and **BufferedOutputStream** create buffered **byte streams**
 - **BufferedReader** and **BufferedWriter** create buffered **character streams**.

Let's see the following example:

## Picture

Instead of reading the content "**Files and**", byte by byte or a character by character, we can use a buffer to get bigger chunks of that text at a time. 

In this case, the buffer will hold two characters at the same time. 

This significantly will **boost the performance** of our applications. 

[/slide]


[slide]

# Command I/O Streams 

[/slide]

