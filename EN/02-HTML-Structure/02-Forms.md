# HTML Forms

[slide]
# HTML Form

An HTML form is used to collect user input, which is generally sent to a web server for processing and storage. It can also be used on the client-side to immediately update the interface in some way (for example by adding another item to a list, or show or hide a UI feature).

## HTML `<form>` Tag

The HTML `<form>` tag defines a form. It's a container element like `<main>` and `<section>`. The form contains interactive controls for submitting information. It takes input from the site visitor and posts it.

Example
```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <input type="submit" value="Submit">
</form>
```
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="ZEbRVeG" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="ZEbRVeG">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/ZEbRVeG">
  ZEbRVeG</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

[/slide]

[slide]

## Form Attributes

The form attributes are optional, but it's standard practice to always set at least the **action** and **method** attributes.
* The action attribute defines the URL, where the form's collected data should be send, when it is submitted.
* The method attribute defines which HTTP method to send the data with (GET/POST).

Example
```html
<form action="/action_my-page.php" method="get">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Smith"><br>
  <input type="submit" value="Submit">
</form>
```
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="wvKXRJR" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="wvKXRJR">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/wvKXRJR">
  wvKXRJR</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

[/slide]

[slide]

## Form Elements

### The `<input>` Element

The `<input>` element is one of the most important form elements. This element can be displayed in several ways, depending on the type attribute:

* `<input type="text">` - defines a single-line text input field;
* `<input type="number">` - defines a numeric input field;
* `<input type="password">` - defines a password field;
* `<input type="email">` - defines an e-mail address. Depending on the browser support, the e-mail address can be automatically validated by submit;
* `<input type="submit">` - defines a button for submitting form data to a form-handler;
* `<input type="radio">` - defines a radio button, which means the user can select **ONLY ONE** of a limited number of choices;
* `<input type="checkbox">` - defines a checkbox, which means the user can select **ZERO** or **MORE** options of a limited number of choices;
* `<input type="file">` - defines a file-select field and a "Browse" button for file uploads.

**Note**: If the type attribute is omitted, the input field gets the default type: "text".

Problem: Write a form.

### Input Validation

* HTML input validation is done automatically by the browser based on special attributes.
* The validation only occurs when attempting to submit the form.
* Inputs which are disabled or read-only will not trigger validation.

### Input Attributes

* `id` – specifies a unique id for an HTML element 
* `type` – specifies the type of `<input>` element to display
* `value` – specifies the initial value for an input field
* `name` – specifies the name of the input element
* `placeholder` – specifies a hint that describes the expected value of the input field
* `required` – the field must be filled out before submitting the form
* `autofocus` – the input should automatically get focus when the page load
* `disabled` – specifies that the input field is disabled
* `min` and `max` – specify the minimum and maximum values

Example
```html
<input type="email" required="true" />
<input type="url" required="true" />
<input type="tel" required="true" />
```

### The `<label>` Element

`<label>` - defines a label for the others forms elements. The for attribute should be equal to the id attribute of the related element to bind them together

Example
```html
<form>
    <label for="male">Male</label>
    <input type="radio" name="gender" id="male" value="male">
    <label for="female">Female</label>
    <input type="radio" name="gender" id="female" value="female">
    <label for="other">Other</label>
    <input type="radio" name="gender" id="other" value="other">
</form>
```
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="vYNrvmd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="vYNrvmd">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/vYNrvmd">
  vYNrvmd</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

### The `<fieldset>` and  `<legend>` Elements

`<fieldset>` is used to group related data in a form and draws a box around the related elements.

Example
```html
<form>
  <fieldset>
    <legend>Customer Details</legend>
    <input type="text" name="fName" />
    <input type="text" name="lName" />
  </fieldset>
  <fieldset>
    <legend>Order Details</legend>
    <input type="text" name="quantity" />
    <textarea name="remarks"></textarea>
  </fieldset>
</form>
```
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="bGVKOWz" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="bGVKOWz">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/bGVKOWz">
  bGVKOWz</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

### The `<select>` and  `<option>` Elements

`<select>` creates a drop-down list. This element is a form control and can be used in a form to collect user input.
`<option>` tags inside the `<select>` element define the available options in the list.

Example
```html
<form>
  <label for="colors">Choose a color:</label>
  <select id="colors" name="colors">
    <option value="volvo">Red</option>
    <option value="saab">Black</option>
    <option value="fiat">White</option>
  </select>
</form>
```
[html]
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="softuni-inter" data-slug-hash="VwvdqWy" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="VwvdqWy">
  <span>See the Pen <a href="https://codepen.io/softuni-inter/pen/VwvdqWy">
  VwvdqWy</a> by Bozhidar (<a href="https://codepen.io/softuni-inter">@softuni-inter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
[/html]

### The `<textarea>` Element

`<textarea>` – defines a multi-line input field. A text area can hold an unlimited number of characters. 
The size of a text area can be specified by the cols and rows attributes or through CSS height and width properties.

`rows` – specifies the visible number of lines in a text area

`cols` – specifies the visible width of a text area.

Example
```html
<textarea rows="10" cols="30">The cat was playing in the garden.</textarea>
```

### Buttons
Submit button – sends the form data to the server
Example
```html
<input type="submit" value="Apply Now" />
```
Reset button – resets all form fields
Example
```html
<input type="reset"/>
```
The `<button>` tag defines a clickable button
Example
```html
<button type="button">Click Me!</button>
```
[/slide]