[slide]

# Problem: Simple Article Page

[code-task title="Problem: Simple Article Page" taskId="d5147f27-86be-44a1-82cf-a9b754251da0" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Simple Article Page**
* Use **article** tag to create an article
* **Divide** the article content into **header**, **section** and **footer** tags
* Use **background** with color - rgb(238, 238, 238)
* Use rgb(51, 51, 51) **color** for the text

You can find an example view [here](https://i.imgur.com/c3wG5rE.png) .

You can download the resources [here](https://mega.nz/file/icwz0BCb#y7UNCy8HPuB0qD_djk2EjzA9RZOOcZ-GtVmZnUrsy-g)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Simple Article Page","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let article = $("body \> article");
expect(article).to.have.lengthOf(1,"Incorrect amount of article tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $("body \> article \> header");
expect(header).to.have.lengthOf(1,"Incorrect amount of header tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body \> article \> section");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let footer = $("body \> article \> footer");
expect(footer).to.have.lengthOf(1,"Incorrect amount of footer tag.");
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
let ul = $("body \> article \> section \> ul");
expect(ul).to.have.lengthOf(1,"Incorrect amount of ul tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li = $("body \> article \> section \> ul li");
expect(li).to.have.lengthOf(5,"Incorrect amount of li tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('color')).to.equal('rgb(51, 51, 51)', "Incorrect text color.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
