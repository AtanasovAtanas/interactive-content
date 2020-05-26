# Media Queries

[slide]
# Media Queries

## What is Media Query?

Media Queries are a feature of CSS that enable webpage content to **adapt** to different screen sizes and resolutions.

They are a fundamental part of **responsive web design** and are used to customize the appearance of websites for multiple devices.

The example bellow means, that if the browser window is 550px or smaller, the background color will be changed to blue, and the text-color will be red.

**Example:**
```html
@media only screen and (max-width: 550px) {
  body {
    background-color: blue;
    color: red;
  }
}
```

[/slide]

[slide]

## How Can be Used Media Queries?

Media queries in CSS3 look at the **capability** of the device.

Media queries can be used to check many things, such as:
* **width** and **height** of the **viewport**;
* **width** and **height** of the **device**;
* orientation (is the tablet/phone in **landscape** or **portrait** mode?);
* **resolution**.

[/slide]

[slide]

## Media Query Syntax

A media query consists of a **media type** and can contain one or more **expressions**, which resolve to either true or false.

**Example:**
```html
@media not|only mediatype and (media-feature-rule) {
  CSS rules goes here
}
```

The result of the query is **true** if the specified media type matches the type of device the document is being displayed on.

Unless you use the **not** or **only** operators, the media type is **optional** and the all type will be implied.

A **media type**, which tells the browser what kind of media this code is for (e.g. print, or screen).

A **media feature rule** is test that must be passed for the contained CSS to be applied.

A set of **CSS rules** that will be applied if the test passes and the media type is correct.

[/slide]
