[slide]

# Problem: Center Position and Transform

[code-task title="Problem: Center Position and Transform" taskId="8becba9e-7472-41f6-b7d1-3931ab47f89e" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Center Position and Transform**
* Create **section** with two divs
* Look the **screenshot** for the inner items
* Use rgb(238, 238, 238) for **body background**
* Use rgb(255, 255, 255) for **card background**
* Use rgb(0, 153, 0) for **card button background**
* Use **font** Georgia, serif with **size** 1em/1.2 for the headings
* Set the **image position** property to **absolute**

You can find an example view [here](https://i.imgur.com/VTbCmOo.jpg)

You can download the resources [here](https://mega.nz/file/CRIkSKAC#kdCTCqYsIUKXov45YpwLQzxzMwzK4hI7eUEovxqgxag)

[/task-description]

[tests]
[test]
[input]
let section = $("body section.card");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let img = $("body img");
expect(img).to.have.lengthOf(1,"Incorrect amount of img tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body p");
expect(p).to.have.lengthOf(1,"Incorrect amount of p tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let div = $("section \> div");
expect(div).to.have.lengthOf(2,"Incorrect amount of div tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('background')).to.equal('rgb(238, 238, 238)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect(document.title).to.equal("Center Position and Transform","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("img").css('position')).to.equal('absolute', "Incorrect position property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
