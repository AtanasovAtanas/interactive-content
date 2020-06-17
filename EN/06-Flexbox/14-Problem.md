[slide]

# Problem: Cards with CSS Columns and Flexbox

[code-task title="Problem: Cards with CSS Columns and Flexbox" taskId="47d00a0a-76ef-47c4-8e96-07691f3f80e5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Cards with CSS Columns and Flexbox**
* **Body background color** must be rgb(238, 238, 238)
* The content should be divided in **two parts**:
* **First part** is container unit (div) with **classes cards-layout and masonry**
* **Second part** is container unit (div) with **classes cards-layout and flex**
* Use **h2** for the **heading**

You can find an example view [here](https://i.imgur.com/1KtihJh.jpg)

You can download the resources [here](https://mega.nz/file/nVQmEYjY#iRgatsPgYLXwvU2JxGUBR_uCZGLIgz6fkZyIl79eiNQ)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Cards with CSS Columns and Flexbox","Incorrect document title.");
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
let container = $('.container')
expect(container).to.have.lengthOf(1,"There is no section with class container.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let headings = $('h2')
expect(headings).to.have.lengthOf(2,"Incorrect amount of h2 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let images = $('img')
expect(images).to.have.lengthOf(16,"Incorrect amount of img tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
