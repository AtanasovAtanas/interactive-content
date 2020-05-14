# Box Sizing

[slide]

## Box-sizing

`box-sizing` sets how the total width and height of an element is calculated or with other words: if the padding and border are included.


* `content-box` is the **initial** and **default** value.
The width and height properties include the content, but they **don't include** the padding, border and margin;
* `border-box` The width and height properties **includes** content, padding and border.

**Example:**
```html
html {
  box-sizing: border-box;
}
```

## Universal Box-sizing

The box-sizing **Reset** takes care of the box-sizing of every element by setting it to **border-box** using universal CSS selector.

Save your **time** and don't write the same thing **again-and-again**.

Set the **"universal box-sizing"** with inheritance:

**Example:**
```html
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
```

[/slide]