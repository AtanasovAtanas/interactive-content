# Margin, Padding and Border

[slide]

## Margin, Padding and Border

### Margin

`margin` defines the space outside the element.

It is a **short hand** property for the following properties:
* `margin-top`
* `margin-left`
* `margin-bottom`
* `margin-right`


The values of the margin property are:
* \<length> - Specifies a margin in **px, pt, cm,** etc. Default value is 0. **Negative** values are allowed.
* `%` - Specifies a margin in **percent of the width** of the containing element

The following two examles make the same thing:

**Example:**
```html
div {
  margin-top: 50px;
  margin-right: 0;
  margin-bottom: 40px;
  margin-left: 10px;
}
```

**Example:**
```html
div {
	margin: 50px 0 40px 10px;
}
```

[/slide]

[slide]

### Padding

`padding` defines the space between the content and the border.

It is a **short hand** property for the following properties:
* `padding-top`
* `padding-left`
* `padding-bottom`
* `padding-right`

The values of the padding property are:
* **\<length>** - Specifies the padding in **px, pt, cm,** etc. Default value is 0.
* `%` - Specifies the padding in **percent of the width** of the containing element

The following two examles make the same thing:

**Example:**
```html
div {
  padding-top: 50px;
  padding-right: 0;
  padding-bottom: 50px;
  padding-left: 0px;
}
```

**Example:**
```html
div {
	padding: 50px 0;
}
```

[/slide]

[slide]

### Border

`border` is a **short hand** property for the following properties:
* `border-width`
* `border-style`
* `border-color`

`border-style` has the following values:
* `none` - Default value. Defines no border;
* `hidden` - The same as "none", except in border conflict resolution for table elements;	
* `dotted` - Dotted border;
* `dashed` - Dashed border;
* `solid` - Solid border;
* `double` - Double border;
* `groove` - 3D grooved border. The effect depends on the border-color value;
* `ridge` - 3D ridged border. The effect depends on the border-color value;
* `inset` - 3D inset border. The effect depends on the border-color value;
* `outset` - 3D outset border. The effect depends on the border-color value.

**Example:**
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="result" data-user="softuni-inter" data-slug-hash="dyYqyBM" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="border-color">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/dyYqyBM">
  border-color</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

**Example:**
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="result" data-user="softuni-inter" data-slug-hash="jObvENv" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="border-properties">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/jObvENv">
  border-properties</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

### Cursor

`cursor` - Sets the mouse cursor when hovering the element.

**Example:**
```html
p {
  cursor: pointer;
}
div {
  cursor: move;
}
```

[/slide]
