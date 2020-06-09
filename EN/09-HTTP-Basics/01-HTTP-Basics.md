# HTTP Protocol

[slide]
# HTTP Basics

**HTTP** is the main Internet protocol used to communicate between:

- **Web servers:** which host Web sites and server-side software components

- **Web clients:** such as Web browsers and mobile apps, which display the information to the users and interact with them.

HTTP comes from **Hyper Text Transfer Protocol** and It is a protocol originally created for transferring `HTML`, `CSS`, images and other Web resources within the global distributed information system called **World Wide Web** (or just Web).

**The Web** consists of all Web sites in **Internet**, which are accessed via the **HTTP protocol**.

Later, HTTP was extended to a **general-purpose client-server protocol for the Internet** and was widely used for transferring almost anything over Internet: text, images, documents, audio streaming, video streaming, chat messages and many others.

There are different kinds of **protocols**:

- a **communication protocol** is a set of rules, which define how two or more parties are talking to each other.

It defines the format of the messages exchanged and their semantics

- programming Protocols are `languages`, used to communicate between machines.

Like in the human languages, protocols have syntax, which specifies the structure of commands and semantics, which specifies their meaning.

[/slide]


[slide]
# HTTP Explained

[image assetsSrc="http-example(1).png" /]

HTTP is **text-based client-server protocol** for the Internet.

- **Text-based** means that the messages, which are exchanged, are human-readable text, not binary data, such as JPEG images.

- **Client-server** means that the communication takes place between a server.

- **Server** is a software which stores the data and provides it upon request and a client, a software which reads and visualizes the data from the server.

**HTTP** is mostly used to transfer Web resources such as HTML files, images, styles, media and documents.

## Example

When you open a **Web site**, the **Web browser** connects to the **Web server**, hosting the requested site, and requests the **URL** that you have entered in the browser's location bar via the **HTTP protocol**.

In most cases the Web server returns an HTML document that contains references to other resources, such as CSS styles, images and scripts, which are downloaded by the Web browser in subsequent HTTP requests.

**HTTP** follows the `request-response model`, which means that the **HTTP client software**, in most cases is a Web browsers, requests resources from the **HTTP servers** (the Web servers) and gets these resources as a response.

Clients **request** and servers **respond** to the requests: this is how it works!

HTTP **does not directly allow** a Web sites to send data to the clients, unless this data is explicitly requested.

And this is perfectly normal: users don't want a Web site to open when it is not requested.

The H**TTP protocol** lies on the `request-response` paradigm and cannot open a website unless someone has asked to open it.

The **HTTP protocol** relies on unique resource locators (URLs), like `https, column, slash, slash, softuni dot org`.

When a resource is downloaded from the Web server, it comes with metadata (such as content-type and encoding), which helps in visualizing the resource correctly.

The **HTTP protocol** is stateless by design, which means that it does not preserve state.

Each HTTP request is **independent** of the others.

Stateful HTTP conversations can be implemented by extra effort, using cookies, custom header fields, Web storage or other techniques.

[/slide]