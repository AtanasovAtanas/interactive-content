[slide]

# Problem: Position Playground

[code-task title="Problem: Position Playground" taskId="2dcbfcb2-fb11-4c45-b241-a228b5f200cf" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Positioning Playground**
* Import **Font Awesome** into your CSS file
* Add two **container units** (divs) with **class viewport** inside the body
* Inside each one add **section** with **class card** (section.card)
* Change the **display** property of the section to **block**
* Try to center the **section** with **position** property **absolute**

You can find an example view [here](https://i.imgur.com/yt446ue.png)

You can download the resources [here](https://mega.nz/file/SF4CDIAa#wvDYpYWyE4X4rPOxMREeUKb73QtJgCEU2BTFiDJyCic)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Positioning Playground","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let cardSection = $("section.card");
expect(cardSection).to.have.lengthOf(2,"Incorrect amount of sections with class card.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let img = $("body img");
expect(img).to.have.lengthOf(2,"Incorrect amount of img tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section.card").css('display')).to.equal('block', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section.card").css('position')).to.equal('absolute', "Incorrect position property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
