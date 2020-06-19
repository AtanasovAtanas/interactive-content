[slide]

# Problem: Landing Page

[code-task title="Problem: Landing Page" taskId="e0655724-dfc8-4ec7-8747-ca15c242a59f" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create an **index.html** file with title - **Landing Page**
* Get the latest reset.css
* Get the latest typography.css
* Get the latest buttons.css
* Get the latest forms.css
* Create a section with a title **Need a website?**
* Create a section with a title **Our Team**
* Create a section with a title **Sign-up to our Newsletter**
* Create a section with a title **Testimonials**
* Create a **footer**
* Make the page **responsive** per the screenshots attached

You can find an example for **desktop** view [here](https://i.imgur.com/bsqUT02.png)

You can find an example for **laptop** view [here](https://i.imgur.com/XzkCC97.png)

You can find an example for **phone** view [here](https://i.imgur.com/OUUNl9x.png)

You can find an example for **tablet** view [here](https://i.imgur.com/S2Owx61.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Landing Page","Incorrect document title");
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
let buttonsCSS = $('\<link rel="stylesheet" href="buttons.css" type="text/css"/\>');
expect(buttonsCSS).to.have.lengthOf(1,"Missing buttons.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let elementsCSS = $('\<link rel="stylesheet" href="elements.css" type="text/css"/\>');
expect(elementsCSS).to.have.lengthOf(1,"Missing elements.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let formsCSS = $('\<link rel="stylesheet" href="forms.css" type="text/css"/\>');
expect(formsCSS).to.have.lengthOf(1,"Missing forms.css.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
