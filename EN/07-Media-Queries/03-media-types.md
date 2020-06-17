# Media Types

[slide]
# Media Types

Media Types describe the general category of a given device:
* `all` – used for all media type devices;
* `print` – used for printers;
* `screen`– used for computer screens, tablets, smart-phones etc.
* `speech` – used for screenreaders that "reads" the page out loud.

The following media query will only set the body to 14px if the page is **printed**. It will not apply when the page is loaded in a browser:

**Example:**
```html
@media print {
    body {
        font-size: 14px;
  }
}
```

[/slide]