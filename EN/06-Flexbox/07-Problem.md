[slide]

# Problem: Flexmodel Calendar

[code-task title="Problem: Flexmodel Calendar" taskId="d3f3ab01-07e0-428e-81e8-858163bea2b2" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Calendar**
* Create a **div** with class container and two sections inside
* First **section** has class **week**
* Second **section** has class **notes**
* Use **span** tags for all content
* Change the **div** and **sections** **display** property to **flex** and **align** the items in **center**
* Set on the **div** **max-width 65vw**
* The **span** must have
* Border **width** - 1px
* Border **color** - black
* Border **style** - solid
* For the **section** with class **notes** use the property **flex-direction column**
* Set on **all** HTML **elements** the property **box-sizing: border-box**

You can find an example view [here](https://i.imgur.com/jWRgdbx.png)

You can download the resources [here](https://mega.nz/file/KRAgVQha#3Fadc1SzzwDaG9IxoNjO-QKZdcB6YA7zWwc74Dh_09U)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Calendar","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let div = $("body div.container");
expect(div).to.have.lengthOf(1,"Incorrect amount of div tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body \> div \> section.week");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag or incorrect class attribute.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let span = $("body \> div \> section.week \> span");
expect(span).to.have.lengthOf(9,"Incorrect amount of span tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("div").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("div").css('max-width')).to.equal('65vw', "Incorrect div width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body \> div \> section.notes");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag or incorrect class attribute.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let span = $("body \> div \> section.notes\> span");
expect(span).to.have.lengthOf(2,"Incorrect amount of span tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body \> div span").css('border-width')).to.equal('1px', "Incorrect border width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section.notes").css('flex-direction')).to.equal('column', "Incorrect flex direction property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
