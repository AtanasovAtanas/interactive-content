# Properties for the Children

[slide]

## Order

The `order` property defines the **order** of a flexbox item.

The first flex item in the code does not have to appear as the first item in the layout and you can manipulate it with `order` property.

* `order: 0;` - The order of the flexbox items is the one **defined in the HTML code**;

**Example** for `order: 0;`

[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="rNOPaQq" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="order:0">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/rNOPaQq">
  order:0</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

* `order: 1;` - The order is relative to the flexbox item's siblings. 

The final order is defined when all individual flexbox item order values are taken into account;

**Example** for `order: 1;`

[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="GRpzgzq" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="order:1">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/GRpzgzq">
  order:1</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

* `order: -1;` - Negative values are also possible. 

**Example** for `order: -1;`

[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="wvKNBOd" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="order:-1">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/wvKNBOd">
  order:-1</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

* `order: 9;` - Each item can have different order to appear on the needed place; 

**Example** for `order: 9;`

[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="pojGvBV" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="order:9">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/pojGvBV">
  order:9</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## Flex-grow

The `flex-grow` defines how much a flexbox item should **grow** if there's space available.

This property has two possible values:
* `flex-grow: 0;` - The element will **not** grow if there's space available. It will only use the space it needs. It's the **default** value;
* `flex-grow: 1;` - The element will **grow** by a factor of 1. It will fill up the remaining space if no other flexbox item has a flex-grow value;

**Example:**
[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="dyYaooY" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-grow">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/dyYaooY">
  flex-grow</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## Flex-shrink

The `flex-shrink` property defines how much a flexbox item should **shrink** if there's **not enough** space available.

This property has two possible values:
* `flex-shrink: 1;` - If there's **not enough** space available in the container's main axis, the element will **shrink** by a factor of **1**, and will wrap its content. It's the **default** value;
* `flex-shrink: 0;` - The element will **not shrink** it will retain the width it needs, and **not wrap** its content. Its siblings will shrink to give space to the target element.

If the target element will not wrap its content, there is a chance for the flexbox container's content to **overflow**;

**Example:**
[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="qBOgdZE" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-shrink">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/qBOgdZE">
  flex-shrink</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## Flex-basis

The `flex-basis` property defines the initial size of a flexbox item.

* `flex-basis: auto;` - The element will be automatically **sized based on its content**, or on any **height** or **width** value if they are defined;

* `flex-basis: 80px;` - You can define **pixel** or **(r)em** values. The element will wrap its content to avoid any overflow.

**Example:**
[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="QWjYbdx" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-basis">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/QWjYbdx">
  flex-basis</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## Flex - The Shorthand Property

The `flex` Flex is the shorthand for:
* `flex-grow`;
* `flex-shrink`;
* `flex-basis`.

The default value is `flex: 0 1 auto;`, wich is equivalent to:

`.item {
 flex-grow: 0;
 flex-shrink: 1;
 flex-basis: auto;
}`

[/slide]

[slide]

## Align-self

The `align-self` property works like `align-items`, but applies only to a single flexbox item, instead of all of them.

This property **overrides** the default alignment set by the container's align-items property.

**Example:**
[html]
<p class="codepen" data-height="300" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="LYpqVON" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-self">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/LYpqVON">
  align-self</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]