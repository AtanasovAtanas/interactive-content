[slide]

# Problem: Responsive Forms

[code-task title="Problem: Responsive Forms" taskId="cdc4c755-5c26-40a5-8161-c4cc659b99f3" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Responsive Forms**
* **Create** a simple **login form** using semantic html
* Add **icons** to the input fields using **FontAwesome**
* Add **focus** state that changes the **input** and the **icon**

You can find an example for **desktop** view [here](https://i.imgur.com/vSjYsLV.png)

You can find an example for **laptop** view [here](https://i.imgur.com/sECy1Re.png)

You can find an example for **phone** view [here](https://i.imgur.com/442PnP7.png)

You can find an example for **tablet** view [here](https://i.imgur.com/oobTYY9.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Responsive Forms","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let form = $("body form");
expect(form).to.have.lengthOf(1,"Incorrect amount of form tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let fieldset = $("body fieldset");
expect(fieldset).to.have.lengthOf(1,"Incorrect amount of fieldset tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let legend = $("body legend");
expect(legend).to.have.lengthOf(1,"Incorrect amount of legend tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body form p");
expect(p).to.have.lengthOf(2,"Incorrect amount of p tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
