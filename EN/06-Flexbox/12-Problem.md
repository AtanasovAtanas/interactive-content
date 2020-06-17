[slide]

# Problem: Center Flexbox

[code-task title="Problem: Center Flexbox" taskId="cfc9d115-46e2-45e3-9e42-7be5a4fe0472" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Center Flexbox**
* The **document background color** must be rgb(238, 238, 238)
* The** body display** property must be **flex**
* The **content** must be placed into **div** with **class card** (div.card)
* The **div background color** must be **rgb(255, 255, 255)**

You can find an example view [here](https://i.imgur.com/fsG9LGK.jpg)

You can download the resources [here](https://mega.nz/file/GZg3iIbJ#7AiGUgdLABqux4xmAOLzCLbrLXlhvTeznYwmUHrhFVg)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Center Flexbox","Incorrect document title.");
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
let divCard = $('.card')
expect(divCard).to.have.lengthOf(1,"Card class is missing.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let divCard = $('div.card')
expect((divCard).css('background')).to.equal('rgb(255, 255, 255)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
