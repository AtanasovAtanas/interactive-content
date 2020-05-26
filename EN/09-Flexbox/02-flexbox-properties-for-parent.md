# Properties for the Parent

[slide]

## `display: flex;`

For start using the Flexbox model, we need to turn the parent element into a **flexbox container**.

The child elements will be turned into flexbox **items**.

**Example:**

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="XWmoWqz" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-container">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/XWmoWqz">
  flex-container</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## `flex-direction` Property

By working with flexbox we have two axes: 
* the main axis;
* the cross axis.

With `flex-direction` property we can define the main axis, and the cross axis is the perpendicular one.

The `flex-direction` property has the following values:
* `row`- The flexbox  items are ordered the **same way** as the text direction, along the main axis;

**Example** for `flex-direction: row;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="LYpMExo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-direction:row">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/LYpMExo">
  flex-direction:row</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

* `row-reverse` - The flexbox items are ordered the **opposite** way as the **text direction**, along the main axis;

**Example** for `flex-direction: row-reverse;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="QWjzwgq" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-direction:rowr">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/QWjzwgq">
  flex-direction:rowr</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

* `column` - The flexbox items are ordered the **same way** as the text direction, along the cross axis;

**Example** for `flex-direction: column;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="LYpMEjw" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-direction:column">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/LYpMEjw">
  flex-direction:column</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

* `column-reverse` - The flexbox items are ordered the **opposite** way as the **text direction**, along the cross axis.


**Example** for `flex-direction: column-reverse;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="abvPzLM" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-direction:columnr">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/abvPzLM">
  flex-direction:columnr</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## `flex-wrap` Property

`flex-wrap` defines if flexbox items appear on a **single line** or on **multiple lines** within a flexbox container.

`flex-wrap: wrap;`- The flexbox items will be distributed **among multiple lines** if needed.

**Example** for `flex-wrap: wrap;`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="WNQLEME" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-wrap:wrap">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/WNQLEME">
  flex-wrap:wrap</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`flex-wrap: wrap-reverse;`- The flexbox items will be distributed **among multiple lines** if needed.

**Example** for `flex-wrap: wrap-reverse;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="wvKRqjd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-wrap:wrapr">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/wvKRqjd">
  flex-wrap:wrapr</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`flex-wrap: nowrap;`- The flexbox items will remain on a **single line**, no matter what, and will eventually overflow if needed.

**Example** for `flex-wrap: nowrap;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="YzydxvX" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-wrap:nowrap">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/YzydxvX">
  flex-wrap:nowrap</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## `flex-flow` Shorthand Property

`flex-flow` is a shorthand for the `flex-direction` and `flex-wrap` properties.

The default value is `row nowrap`.

**Example** for `flex-flow: row wrap;`

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="OJyrjop" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="flex-flow">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/OJyrjop">
  flex-flow</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## `justify-content` Property

`justify-content` defines how flexbox/grid items are aligned according to the **main axis**, within a flexbox container.

`justify-content: flex-start` - with this value the flexbox items are pushed towards the **start of the container's main axis**, which is the **default** value.


**Example** for `justify-content: flex-start`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="QWjzMzQ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justify-content:start">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/QWjzMzQ">
  justify-content:start</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`justify-content: flex-end` - with this value the flexbox items are pushed towards the **end of the container's main axis**.


**Example** for `justify-content: flex-end`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="dyYwzrY" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justify-content:end">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/dyYwzrY">
  justify-content:end</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`justify-content: center` - with this value the flexbox items are **centered** along the container's **main axis**.

**Example** for `justify-content: center`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="WNQLEWM" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justify-content:center">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/WNQLEWM">
  justify-content:center</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`justify-content: space-between` - with this value the remaining space is distributed **between** the flexbox items.

**Example** for `justify-content: space-between`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="NWGevVX" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justify-content:spaceb">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/NWGevVX">
  justify-content:spaceb</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`justify-content: space-around` - with this value the remaining space is distributed **around** the flexbox items: this adds space **before** the first item and **after** the last one.


**Example** for `justify-content: space-around`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="qBOLXeE" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justify-content:spacea">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/qBOLXeE">
  justify-content:spacea</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## `align-items` Property

`align-items` defines how flexbox items are aligned **according to the cross axis**, within a line of a flexbox container.

`align-items: flex-start` - with this value the flexbox items are aligned at the **start of the cross axis**.

**Example** for `align-items: flex-start`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="xxwmXEG" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-items:start">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/xxwmXEG">
  align-items:start</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`align-items: flex-end` - with this value the flexbox items are aligned at the **end of the cross axis**.

**Example** for `align-items: flex-end`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="jObXGMe" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-items:end">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/jObXGMe">
  align-items:end</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`align-items: center` - with this value the flexbox items are aligned at the **center of the cross axis**.

**Example** for `align-items: center`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="YzydrpN" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-items:center">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/YzydrpN">
  align-items:center</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`align-items: baseline` - with this value the flexbox items are aligned at the **baseline of the cross axis**.

**Example** for `align-items: baseline`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="LYpMzxZ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-items:baseline">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/LYpMzxZ">
  align-items:baseline</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

`align-items: stretch` - The flexbox items will stretch **across the whole cross axis**. 
This is the **default** value.

**Example** for `align-items: stretch`:

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="ExVGwWa" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-items:stretch">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/ExVGwWa">
  align-items:stretch</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]

[slide]

## `align-content` Property

`align-content` defines how each line is aligned within a flexbox container.

This property is similar to `align-items`, but instead of aligning flex items, **it aligns flex lines**.

It only applies if `flex-wrap: wrap;` **is present**, and if there are **multiple lines** of flexbox items.

* `stretch` - **Default** value. Lines stretch to take up the **remaining** space;
* `center` - Lines are packed toward the **center** of the flex container;
* `flex-start` - Lines are packed toward the **start** of the flex container;
* `flex-end` - Lines are packed toward the **end** of the flex container;
* `space-between` - Lines are **evenly** distributed in the flex container between the elements;
* `space-around` - Lines are **evenly** distributed in the flex container, with **half-size** spaces on either end.

**Example:**

[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="result" data-user="softuni-inter" data-slug-hash="KKdbZKW" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="align-content">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/KKdbZKW">
  align-content</a> by SoftUni (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[/html]

[/slide]