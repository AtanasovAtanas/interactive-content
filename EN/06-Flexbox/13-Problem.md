[slide]

# Problem: Expanding Flex Cards

[code-task title="Problem: Expanding Flex Cards" taskId="c455515f-ee34-4239-80b9-828a053a4aec" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Expanding Flex Cards**
* **Body background color** must be **rgb(238, 238, 238)**
* The **body** **display** property must be **flex**
* **Align** the items in **center**
* The entire **page content** must be inside **section** with class named **container** (section.container)
* The **container** **display** property must be **flex**

You can find an example view [here](https://i.imgur.com/Xtv0cTW.jpg)

You can download the resources [here](https://mega.nz/file/PEI2QAYS#ikqnbEzo5lkBMcvw-HszUOPaV8e3lpGplvm2wmkLo-g)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Expanding Flex Cards","Incorrect document title.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('background')).to.equal('rgb(238, 238, 238)', "Incorrect body background.");
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
expect($("body").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let container = $('.container')
expect(container).to.have.lengthOf(1,"There is no section with class container.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let container = $('.container')
expect((container).css('display')).to.be.equal('flex', "Incorrect container display property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
