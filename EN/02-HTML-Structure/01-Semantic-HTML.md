# HTML Structure

[slide]
# HTML Semantic Elements

HTML5 uses **semantic tags** for the document structure.

The semantic element clearly describes its meaning to both the **browser** and the **developer**.

Examples of **non-semantic elements** are \<div\>, \<span\> - they tell nothing about its content.

Examples of **semantic elements** are \<section\>, \<header\>, \<article\> they define its content.

In HTML there are some semantic elements, that can be used to define different parts of a web page:

* `<article>`
* `<aside>`
* `<details>`
* `<figcaption>`
* `<figure>`
* `<footer>`
* `<header>`
* `<main>`
* `<mark>`
* `<nav>`
* `<section>`
* `<summary>`
* `<time>`

[/slide]

[slide]
# HTML Semantic Tags

## HTML \<nav\> Tag

The `<nav>` tag defines a set of navigation links.

****Example****
```html
<nav id="topmenu">
  <ul>
    <li><a href="/Home">Home</a></li>
    <li><a href="/Menu">Menu</a></li>
    <li><a href="/Courses">Courses</a></li>
  </ul>
</nav>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="ExVROJj" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="ExVROJj">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/ExVROJj">
  ExVROJj</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<header\> Tag

The `<header>` tag specifies a header for a document or section.

This tag should be used as a **container for introductory content**.

You can have several `<header>` tags in one document.

****Example****
```html
<header>
  <h1>Welcome to SoftUni!</h1>
</header>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="vYNrQwZ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="vYNrQwZ">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/vYNrQwZ">
  vYNrQwZ</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<main\> Tag

The `<main>` tag specifies the main content of a document.

It's content should be unique to the document.

There must not be more than one `<main>` tag in a document.

`<main>` tag wraps the most important information in the body.

****Example****
```html
<main>
  <h1>HTML and CSS</h1>
  <p>HTML and CSS are two of the core technologies for building Web pages.</p>
  <article>
    <h2>HTML</h2>
    <p> Hypertext Markup Language (HTML) is the standard markup language for documents designed to be displayed in a web browser. </p>
    <p>... </p>
  </article>
  <article>
    <h2>CSS</h2>
    <p> Cascading Style Sheets (CSS) describes how HTML tags are to be displayed </p>
    <p>... </p>
  </article>
</main>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="MWaXzdd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="MWaXzdd">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/MWaXzdd">
  MWaXzdd</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<footer\> Tag

The `<footer>` tag represents a footer for a document or section.

Usually, a `<footer>` tag contains information about the author, copyright data or links to related documents.

You may have several `<footer>` tags in one document.

****Example****
```html
<footer>
  <p>Posted by: Hege Refsnes</p>
  <p><a href="someone@exam.uk">Contact...</a></p>
  <p>&copy;copyright</p>
</footer>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="PoPaxrR" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="PoPaxrR">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/PoPaxrR">
  PoPaxrR</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<section\> Tag

The HTML `<section>` tag represents a standalone section, which doesn't have a more specific semantic tag to represent it.

 Typically, but not mandatory, sections have a heading.

****Example****
```html
<section>
  <h2>First Section</h2>
  <p>First Section Example</p>
</section>
<section>
  <h2>Second Section</h2>
  <p>Second Section Example</p>
</section>
<section>
  <h2>Third Section</h2>
  <p>Third Section Example</p>
</section>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="OJyEaKZ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="OJyEaKZ">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/OJyEaKZ">
  OJyEaKZ</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<aside\> Tag

Тhe HTML `<aside>` tag defines some content aside from the content it is placed in.

Asides are frequently presented as sidebars or call-out boxes.

****Example****
```html
<aside>
  <h2>Blogroll</h2>
  <ul>
    <li><a href="#">My Friend</a></li>
    <li><a href="#">Other Friend</a></li>
    <li><a href="#">Best Friend</a></li>
  </ul>
</aside>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="wvKXRGY" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="wvKXRGY">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/wvKXRGY">
  wvKXRGY</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

Problem: Simple Web Page

## HTML \<figure\> and \<figcaption\> Tags

The `<figure>` tag is used to mark up a photo in a document.

The `<figcaption>` tag defines a caption for the photo:

**Example**
```html
<p>The Pulpit Rock …</p>
<figure>
  <img src="https://www.w3schools.com/w3css/img_lights.jpg" width="200" alt="The …">
  <figcaption>Fig.1 - A view</figcaption>
</figure>
```

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="rNOKoWO" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="rNOKoWO">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/rNOKoWO">
  rNOKoWO</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<details\> and \<summary\> Tags

The `<details>` tag specifies additional details, that the user can view or hide on demand. 

A summary or label can be provided using the `<summary>` element.

If the first child of the `<details>` element is a `<summary>`, the contents of the `<summary>` element are used as the label for the disclosure widget.

**Example**
```html
<details>
  <summary>Some details</summary> 
  <p>More info about the details.</p> 
</details>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="XWmYopd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="XWmYopd">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/XWmYopd">
  XWmYopd</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

## HTML \<time\> and \<address\> Tags

* The `<time>` tag defines a human-readable date/time. It may include the datetime attribute to translate dates into a machine-readable format.
* The HTML `<address>` element indicates that the enclosed HTML provides contact information like email address, URL, physical address, phone number, social media handle, etc.

**Example**
```html
<div>
  <p>We open at <time>10:00</time> every morning.</p>
  <address>
    <a href="mailto:jim@gmail.com">jim@gmail.com</a>
  </address>
</div>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="LYprMxL" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="LYprMxL">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/LYprMxL">
  LYprMxL</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

[/slide]