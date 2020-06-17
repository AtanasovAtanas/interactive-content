[slide]

# Problem: Box Model Container

[code-task title="Problem: Box Model Container" taskId="ad6dd487-24e4-452f-8515-0769efa121c1" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Box Model Container**
* Use **p** tag to create a paragraph
* Set the paragraph **width**: 200px;
* Set **padding** and **margin**
* Set **5px solid border** with **border-radius**
* Use **rgb(64, 224, 208)** color for the **background**
* Try to center the container with **margin: auto**

You can find an example view [here](https://i.imgur.com/YPecbHc.png)

You can download the resources [here](https://mega.nz/file/6U4j0K5D#bE77e7n5MZyQ_fuAKBPOHa6UOb9N27_3nLtSwQahIbw)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Box Model Container","Incorrect title name");
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
expect($("p").css('background')).to.equal('rgb(64, 224, 208)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("p").css('border-width')).to.equal('5px', "Incorrect border width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("p").css('border-style')).to.equal('solid', "Incorrect border-style");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
