[slide]

# Problem: Flexmodel ABC Game

[code-task title="Problem: Flexmodel ABC Game" taskId="3f27a4a2-94c4-44b1-ae33-ef8d1e61d90d" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **ABC Game**
* Create a **section** with three **articles** inside
* Create a **div** with class **container** and 12 **span** tags inside
* Type the **letters** in the spans **EXACTLY** as they are in the file text.txt
* Use **font-family**: Helvetica, sans-serif, with **font-size**: 20px
* Change the div **display** property to **flex** and **align** the items in center
* Set on the div **max-width**: 15vw and **height** 35rem
* The **span** must have
* Border **width** - 1px
* Border **color** - black
* Border **style** - solid
* To arrange the letters, use the **flex** property **order**

You can find an example view [here](https://i.imgur.com/P3ngOYk.png)

You can download the resources [here](https://mega.nz/file/2dJBwKBL#LEt0D2DXogY2Sgw4YT6aMA7-xeQunE306uvVHAGz8RA)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("ABC Game","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let div = $("body div.container");
expect(div).to.have.lengthOf(1,"Incorrect amount of div tag or incorrect class attribute.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let span = $("body \> div \> span");
expect(span).to.have.lengthOf(12,"Incorrect amount of span tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let spanSecond = $("div \> span:nth-child(2)");
expect(spanSecond.text()).to.include('e',"Incorrect text in span tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-family')).to.equal('Helvetica, sans-serif', "Incorrect document font family.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let spanTen = $("div \> span:nth-child(10)");
expect(spanTen.text()).to.include('L',"Incorrect text in span tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("div").css('display')).to.equal('flex', "Incorrect div display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("div").css('max-width')).to.equal('15vw', "Incorrect width to the div element.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body span").css('border-width')).to.equal('1px', "Incorrect border-width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body span").css('border-style')).to.equal('solid', "Incorrect border-style.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
