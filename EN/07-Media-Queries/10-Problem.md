[slide]

# Problem: Update Blog Layout

[code-task title="Problem: Update Blog Layout" taskId="0f6c2aa3-b6e8-4507-b481-30cd625681ae" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Responsive Forms**
* Create a simple **login form** using semantic html
* Add **icons** to the input fields using **FontAwesome**
* Add **focus state** that changes the **input** and the **icon**

You can find an example for **desktop** view [here](https://i.imgur.com/luhotsh.png)

You can find an example for **laptop** view [here](https://i.imgur.com/kw5AE7j.png)

You can find an example for **phone** view [here](https://i.imgur.com/weuW9z5.png)

You can find an example for **tablet** view [here](https://i.imgur.com/d5KX5HF.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Update Blog Layout","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let resetCSS = $('\<link rel="stylesheet" href="reset.css" type="text/css"/\>');
expect(resetCSS).to.have.lengthOf(1,"Missing reset.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let typographyCSS = $('\<link rel="stylesheet" href="typography.css" type="text/css"/\>');
expect(typographyCSS).to.have.lengthOf(1,"Missing typography.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let layoutCSS = $('\<link rel="stylesheet" href="layout.css" type="text/css"/\>');
expect(layoutCSS).to.have.lengthOf(1,"Missing layout.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let navigationCSS = $('\<link rel="stylesheet" href="navigation.css" type="text/css"/\>');
expect(navigationCSS).to.have.lengthOf(1,"Missing navigation.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let nav = $("header nav");
expect(nav).to.have.lengthOf(1,"Incorrect amount of nav tag in the header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let label = $("header label");
expect(label).to.have.lengthOf(1,"Incorrect amount of label tag in the header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let aside = $("body aside");
expect(aside).to.have.lengthOf(1,"Incorrect amount of aside tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
