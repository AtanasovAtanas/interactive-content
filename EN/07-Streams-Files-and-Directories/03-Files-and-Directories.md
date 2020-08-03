# Files and Directories

[slide]

# Files and Paths
A Java **Path** instance represents **a path in the file system**.

A path can point to either a **file** or a **directory**.

**Path** is used to **examine**, **locate**, and **manipulate** files.

An example of that is input.txt file wich we have used for the previous problems.

```java
String input = "D:\\input.txt";

Path path = Paths.get(input);
```
The static method `get()` takes as argument the **String representation of the file location**.

By calling a `Paths.get()` - method the **instance of Path** is created.

The Path instance gives us an easy way to create a Buffered Stream by using a BufferedReader and **Files** classes.

Let's see the following example:

```java
Path path = Paths.get("D:\\input.txt");

try (BufferedReader inputStream = Files.newBufferedReader(path)) {

    String line = inputStream.readLine();
    while (line != null) {
        System.out.println(line);
        line = inputStream.readLine();
    }
} catch (IOException e) {
    e.printStackTrace();
}
```
By calling a `newBufferedReader()` - method of the Files class and pass the path as a argument, the BufferedReader instance is created (**Buffered Stream**).

The following example illustrates copying the content of one file to another:

```java
Path inputPath = Paths.get("D:\\input.txt");
Path outputPath = Paths.get("D:\\output.txt");

try  {
    List<String> lines = Files.readAllLines(inputPath);
    Files.write(outputPath, lines);
} catch (IOException e) {
    e.printStackTrace();
}
```
First we create two Path variables for input and output files.

Next we call `readallLines()` - method of the Files class and pass the **inputPath** variable.

The `readAllLines()` - method, returns a List with all lines in a file.

Then we pass this **List** to the Files `write()` - method along with the **outputPath** variable.




[/slide]

[slide]

# File Class in Java

[/slide]

    