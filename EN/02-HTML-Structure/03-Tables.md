# HTML Tables

[slide]
# HTML Table

HTML table allows web authors to arrange data into rows and columns.

## HTML `<table>` Tag

`<table>` tag defines an HTML table. Each table row is defined with a `<tr>` tag. A table cell is defined with a `<td>` tag (`td` means table data).

If the cell is in the header, it is defined with the `<th>` tag. By default, table headings are bold and centered. 

**Example**
```html
<table>
    <tr>
        <td>Cell 1.1</td>
    </tr>
    <tr>
        <td>Cell 2.1</td>
    </tr>
</table>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="JjYZwyN" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="JjYZwyN">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/JjYZwyN">
  JjYZwyN</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

[/slide]

[slide]

## Complete HTML Tables

There are three specific parts in every table: 
* `<thead>` - used to group header content in an HTML table;
* `<tbody>` - used to group the body content in an HTML table;
* `<tfoot>` - used to group footer content in an HTML table

These elements are used to specify each part of a table (header, body, footer). 

**Example**
```html
<table>
  <thead>
    <tr>
        <th>Name</th>
        <th>Grade</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td>Mark</td>
        <td>5,75</td>
    </tr>
  </tbody>
  <tfoot>…</tfoot>
</table>
```
[html]
<p class="codepen" data-height="265" data-theme-id="39135" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="ExVRGwN" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="ExVRGwN">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/ExVRGwN">
  ExVRGwN</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

[/slide]