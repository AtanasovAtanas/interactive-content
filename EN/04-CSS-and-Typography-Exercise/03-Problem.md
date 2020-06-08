[slide]

# Problem: Styling Tables

[code-task title="Problem: Styling Tables" taskId="c456515b-5d4d-4e5e-82dd-213559a00a8d" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document **title** to **Styling Tables**
* Use **table** tag
* Use **thead** and **tbody** tags
* Style the **odd tr** tags with **background**: rgb(241, 241, 241)
* The **table**, **td** and **th** tags must have
* Border **width** - 1px
* Border **color** - rgb(221, 221, 221)
* Border **style** - solid
* When you **hover** the table row, the following styles must be updated:
* **Background**: rgb(0, 0, 0)
* Text **color**: rgb(255, 255, 255)

You can find an example view 1 [here](https://i.imgur.com/GfBPPw2.png)

You can find an example view 2 [here](https://i.imgur.com/NHBzZ2O.png)

You can download the resources [here](https://mega.nz/file/uZJXBAyJ#2sBfBmdhgWIRnOIXLtZCUwt0nwMeWw-BL3Oh6O9-yH0)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Styling Tables","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let table = $("body table");
expect(table).to.have.lengthOf(1,"Incorrect amount of table tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let thead = $("table thead");
expect(thead).to.have.lengthOf(1,"Incorrect amount of thead tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let tbody = $("body tbody");
expect(tbody).to.have.lengthOf(1,"Incorrect amount of tbody tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("table thead th").css('text-align')).to.equal('left', "Incorrect text align.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("table tr:nth-child(odd)").css('background')).to.equal('rgb(241, 241, 241)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("table").css('border-width')).to.equal('1px', "Incorrect border width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("th").css('border-width')).to.equal('1px', "Incorrect border width.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("table th").css('border-color')).to.equal('rgb(221, 221, 221)', "Incorrect td background color.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("table td").css('border-style')).to.equal('solid', "Incorrect border style.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
