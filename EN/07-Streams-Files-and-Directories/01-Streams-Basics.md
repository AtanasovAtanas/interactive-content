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

## Picture

- **OutputStream** − used for writing data to a **destination**

## Picture

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



