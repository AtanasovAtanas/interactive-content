[slide]

# Problem: Responsive Menu

[code-task title="Problem: Responsive Menu" taskId="36ef16e6-936f-4b46-bdc4-0e9a02547662" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Responsive Menu**
* Add media queries to **hide** the toggle checkbox and label for **desktops**
* Add media queries to **show** the toggle checkbox and label for **mobile devices**


You can find an example for **desktop** view [here](https://i.imgur.com/GbDC0cV.png)

You can find an example for **laptop** view [here](https://i.imgur.com/DG767qz.png)

You can find an example for **phone** view [here](https://i.imgur.com/0CWrGEB.png)

You can find an example for **tablet** view [here](https://i.imgur.com/s4B8bxo.png)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Responsive Menu","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let navigation = $("body header nav");
expect(navigation).to.have.lengthOf(1,"Incorrect amount of nav tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ul = $("body header nav \> ul");
expect(ul).to.have.lengthOf(1,"Incorrect amount of ul in the navigation.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let label = $("body header label");
expect(label).to.have.lengthOf(1,"Incorrect amount of label tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let input = $("body \> input");
expect(input).to.have.lengthOf(1,"Incorrect amount of input tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
