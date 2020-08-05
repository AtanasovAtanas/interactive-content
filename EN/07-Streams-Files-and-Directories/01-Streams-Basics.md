# Streams Basics

[slide]

# Streams Basics

All of us have watched online videos on youtube or some other such website. 

When you start watching a video, a small portion of the file is first loaded into your computer and start playing. 

There is no need to download the complete video before you start playing it and this is called **streaming**.

A stream can be defined as a **sequence of data**. 

In Java, a stream is **composed of bytes**. 

It's called a stream because it is like a stream of water that continues to flow.

There are **two fundamental types** of Streams:

- **InputStream** − used to read data from a **source**

[image assetsSrc="streams-files-directories-example(1).png" /]

- **OutputStream** − used for writing data to a **destination**

[image assetsSrc="streams-files-directories-example(2).png" /]

Let's have a look at the following examples:

 - **Opening a File Stream**:

```java
// source
String path = "C:\\input.txt";

// opening an input stream by instantiating a FileInputStream class
FileInputStream fileStream = new FileInputStream(path);

// storing the first byte into an int variable
int oneByte = fileStream.read();

while (oneByte >= 0) {
  // printing the current byte
  System.out.print(oneByte);
  
  // reading the next byte from the file
  // the read() method returns -1 if there is no more content
  oneByte = fileStream.read();
}
```

- **Closing a File Stream** using `try-catch-finally`:


```java
// source 
String path = "C:\\input.txt";

// declaring the inputStream variable
InputStream inputStream = null;

// opening the try block
try {
    // opening a stream might cause an exception if the file is missing or corrupted
    // or some other circumstances might trip us in our efforts of reading it
    inputStream = new FileInputStream(path);
    int oneByte = in.read();
    while (oneByte >= 0) {
        System.out.print(oneByte);
        oneByte = in.read();
    }
} // specifying the exact type of exception
  catch (IOException ex) {
    // handling the exception
    System.out.println("File not found!");

} // it will always be executed with or without of exception of the try block 
  finally {
    if (inputStream != null) {
      // closing the stream
        inputStream.close();
    }
}

```
- **Closing a File Stream** using `try-with-resources`

There is a **shorter way** of implementing the same behavior in the previous example - `try-with-resources`.

We can create a Stream inside of the braces of the try block and this operatin will make a Stream available inside the try block.

The **main benefit** is that the Stream will be **automatically closed** after we finish our job in the try block.

```java
// source 
String path = "C:\\input.txt";

// opening a stream inside of the braces of the try block
try (InputStream in = new FileInputStream(path)) {
    int oneByte = in.read();
    while (oneByte >= 0) {
        System.out.print(oneByte);
        oneByte = in.read();
      }
  } catch (IOException e) {
        System.out.println("File not found!");
}

```

[/slide]

[slide]
# Problem: Read File
[code-task title="Read File" taskId="193a469d-4176-465b-bc37-7729ac760388" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```

```
[/code-editor]
[task-description]
## Description
You are given a file named "**input.txt**" (from the Resources - Folder).

**Read** and **print** all of its contents as a sequence of bytes (the binary representation of the ASCII code for each character) separated by a single comma.

## Guidelines

There is one zipped folder with resources for all exercises, that you need to use. 

Download the **resources folder** [here](https://mega.nz/file/qV4WgapZ#twhDs3mE_2NNg1P6R-WKoH7cnAJPIpPZ14AaBcScilw).

For each exercise submit only the **output** of your program, **not the code**.


## Examples
| **Input** | **Output** |
| --- | --- |
| On January 1 , 1533 , Michael Angelo, then fifty-seven years old, writes… | 11101111 10111011 10111111 1001111 1101110 100000 1001010 1100001 1101110 1110101… |
|  |  |

| **Input** | **Output** |
| --- | --- |
| Two households, both alike in dignity, | 1010100 1110111 1101111 100000 1101000 1101111 1110101 1110011 1100101 1101000… |
| In fair Verona, where we lay our scene… |  |


## Hints
- Create a string variable holding the path to the file. If, for example, the file is located in "D:\\"
```java
String path = "D:\\input.txt";
```
- Use try-with-resources to open the file and to be sure that it will be closed after you are done with it
```java
try(FileInputStream fileStream = new FileInputStream(path)){
      
}catch (IOException ex){
      ex.printStackTrace();
}
```

- Use the read() method to read each byte of the file until it returns -1

```java
try (FileInputStream fileStream = new FileInputStream(path)) {
    int oneByte = fileStream.read();
    while (oneByte >= 0) {
        System.out.printf("%s ", Integer.toBinaryString(oneByte));
        oneByte = fileStream.read();
    }
} catch (IOException ex) {
    ex.printStackTrace();
}
```
- Select the output of the program and copy it [Ctrl + C]
- Paste the output in the Platform



[/task-description]
[code-io /]
[tests]
[test]
[input]
1001111 
[/input]
[output]
1001111 
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]

# Solution: Read File

```java
// After downloading the resource folder 
// Create a string variable holding the path to the input.txt file. 
// If, for example, the file is located in "D:\"
String path = "D:\\input.txt";

// Use try-with-resources to open the file and to be sure that it will be closed after you are done with it
try (FileInputStream fileStream = new FileInputStream(path)) {

  // Use the read() method to read each byte of the file until it returns -1
    int oneByte = fileStream.read();
    while (oneByte >= 0) {
        System.out.printf("%s ", Integer.toBinaryString(oneByte));
        oneByte = fileStream.read();
    }
} catch (IOException ex) {
    ex.printStackTrace();
}    
```

[/slide]



