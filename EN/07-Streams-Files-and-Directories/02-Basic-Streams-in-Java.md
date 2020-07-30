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
[/slide]

[slide]

# Buffered Streams 

[/slide]


[slide]

# Command I/O Streams 

[/slide]

