# Import

[slide]
# Import

The **@import CSS at-rule** is used to import style rules from other style sheets.

You can specify media-dependent @import rules.

These conditional imports specify comma-separated media queries after the URL.

**Example:**
```html
@import url;
@import url list-of-media-queries;
@import url("fineprint.css") print;
@import url(“landscape.css") screen and (orientation: landscape);
```

[/slide]