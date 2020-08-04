# Serialization

[slide]

# Serializing and Deserializing Objects

In Java, we create several objects that live and die accordingly, and every object will certainly die when the program execution finish.

But sometimes, we might want to **reuse** an object between several programs or we might want to **transfer** an object to another machine over the network.

**Serialization** allows us to **convert the state of an object into a byte stream**, which then can be saved into a file on the local disk or sent over the network to any other machine. 

**Deserialization** allows us to reverse the process, which means **reconverting the serialized byte stream to an object** again.

In simple words, object **serialization** is the process of **saving an object's state** to a **sequence of bytes** and **deserialization** is the process of **reconstructing an object from those bytes**.

Generally, the complete process is called **Serialization**.

The **Serialization** process is **platform independent**, an object serialized on one platform can be deserialized on a different platform.

- **Serialization**:

```java
String output = "D:\\names.ser";

List<String> names = new ArrayList<>();
Collections.addAll(names, "Maria", "George", "Peter","Sophia");

FileOutputStream fileOutputStream = new FileOutputStream(output);
ObjectOutputStream objectOutputStream =  new ObjectOutputStream(fileOutputStream);

objectOutputStream.writeObject(names);
```
In the example above first, we create a **FileOutputStream** and placing the file location in the constructor.

It's good practice to store the serialized object in files with extension `.ser`.

Next, we wrap the FileOutputStream with an **ObjectOutputStream**.

By `writeObject()` - method, the names data structure is written to the output file.

- **Deserialization**:

```java
String input = "D:\\names.ser";

FileInputStream fileInputStream = new FileInputStream(input);
ObjectInputStream objectInputStream = new ObjectInputStream(fileInputStream);
List<String> names = (List<String>) objectInputStream.readObject();
```
Deserialization on other hand does the absolute opposite. 

It reads files, the content of which are serialized objects and loads them back into the memory of our Java program.

In the example above, we create a FileInputStream wrapped by an ObjectInputStream.

The `readObject()` -  method returns back the names data structure that we previously stored into the file.

- Serialization of **Custom Objects**:

To serialize Custom objects, they have to implement the Serializable interface.

```java
class Cube implements Serializable {
  String color;
  double width;
  double height;
  double depth;
}
```

[/slide]


