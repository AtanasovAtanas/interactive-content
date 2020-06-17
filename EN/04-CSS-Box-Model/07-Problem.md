[slide]

# Problem: Box Sizing

[code-task title="Problem: Box Sizing" taskId="3e91f1aa-9e58-43a6-948b-fa3701dbe74f" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Box Sizing**
* Use **section** tag to create a section
* Use **h1** heading with content **Front End** in the section
* Use **paragraph** with content **I like HTML and CSS!** in the section
* The section has **width** 250px, **height** 250px and **border**
* The paragraph has **width 100%**, **border** and **padding 20px** on all sides

You can find an example view [here](https://i.imgur.com/Orafv63.png)

You can download the resources [here](https://mega.nz/file/TAAUTAKD#iXs0ItpkU43ToiWyF73hjc3kocY4y02_SDtZqIRo5Mc)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Box Sizing","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body section");
expect(section ).to.have.lengthOf(1,"Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body section \> p");
expect(p).to.have.lengthOf(1,"Incorrect amount of p tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1 = $("body section \> h1");
expect(h1).to.have.lengthOf(1,"Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section").css('height')).to.equal('250px', "Incorrect section height.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("p").css('width')).to.equal('100%', "Incorrect paragraph width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('box-sizing')).to.equal('inherit', "Incorrect box-sizing property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
