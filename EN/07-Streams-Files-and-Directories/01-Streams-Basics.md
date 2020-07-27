# Streams Basics

[slide]

# What is Stream in Java?

All of us have watched online videos on youtube or some other such website. 

When you start watching a video, a small portion of the file is first loaded into your computer and start playing. 

There is no need to download the complete video before you start playing it and this is called **streaming**.

The Java Stream API was first introduced in Java 8.

A Java Stream can be explained as a pipeline through which data will flow. 

The pipeline's functions will operate on the data by e.g. filtering, mapping, and sorting the items. 
Lastly, a terminal operation can be performed to collect the items in a preferred data structure such as a List, an Array, or a Map. 

An important thing to notice is that a Stream can only be consumed once.

## Picture  

As it shown on the picture above, a Stream Pipeline contains three main parts:

- **Stream source**

- **Intermediate** operations(zero or more)

- **Terminal** operation

**Stream source** it might be an **Array**, a **Collection**, a **generator function**, an **I/O channel** etc.

Stream operations are either **intermediate** or **terminal**.

**Terminal operations** can return a result of a certain type or creating side effect (**void**).

The Stream API provides the following common **terminal operations**:
- `toArray()` 
- `collect()` 
- `count()`
- `reduce()`
- `forEach()`

**Intermediate operations** return a new Stream which allows to call multiple operartions in the form of a query.
As intermediate operations return another Stream as a result, they can be chained together to form a pipeline of operations.
Pipeline of operations may contain any number of intermediate operations, but there is only one terminal operation, that too at the end of the pipeline.

The Stream API provides the following common **intermediate operations**:
- `map()`
- `filter()`
- `sorted()`
- `limit()`
- `distinct()`



[/slide]

[slide]

# Streams Basics

A stream can be defined as a sequence of data.

There are two kinds of Streams:

- InputStream − used to read data from a source

## Picture

- OutputStream − used for writing data to a destination

## Picture


## InputStream
[/slide]



