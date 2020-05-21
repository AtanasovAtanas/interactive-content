# Box Sizing

[slide]

# Box-sizing

`box-sizing` sets how the total width and height of an element is calculated or with other words: if the padding and border are included.

* `content-box` is the **initial** and **default** value. The width and height properties include the content, but they **don't include** the padding, border and margin;
* `border-box` The width and height properties **includes** content, padding and border.

**Example:**
```html
html {
  box-sizing: border-box;
}
```

# Universal Box-sizing

The box-sizing **Reset** takes care of the box-sizing of every element by setting it to **border-box** using a universal CSS selector.

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

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="pojQGMJ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="box-sizing">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/pojQGMJ">
  box-sizing</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]