# Z\-index

[slide]

# Z\-index

`z-index` defines the order of the elements on the **z-axis**.

It only works on **positioned** elements (anything apart from static).

If the element has **greater** stack order then it is always **in front** of an element with a lower stack order.

The following values of `z-index` are possible:
* `auto` - Sets the stack order **equal to its parents**. This is **default**;
* `number` - Sets the **stack order** of the element. Negative numbers are **allowed**.

The order is defined by the **order in the HTML** code:
* First in the code goes behind;
* Last in the code goes in front.

**Example:**

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="eYpQvdL" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="position-static">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/eYpQvdL">
  position-static</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

# `z-index: 1;`

The `z-index` value is relative to the other ones.

The target element is moved in **front** of its siblings.

**Example:**
```html
.second {
  position: relative;
  top: -20px;
  left: 45px;
  z-index: 1;
  background-color: #ff3d64;
  width: 70%;
}
```

**Example:**

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="bGVQLpx" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="z-index:1">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/bGVQLpx">
  z-index:1</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

# `z-index: -1;`

For `z-index` you can use **negative** values.

The target element is moved **behind** its siblings.


**Example:**
```html
.second {
  position: relative;
  top: -20px;
  left: 45px;
  z-index: -1;
  background-color: #ff3d64;
  width: 70%;
}
```

**Example:**

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="jObQZMd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="z-index:-1">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/jObQZMd">
  z-index:-1</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]