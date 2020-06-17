[slide]

# Problem: Style Lists

[code-task title="Problem: Style Lists" taskId="dc210cfe-0179-49f0-b2a2-6123084d14c2" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document **title** to **Style Lists**
* Use **font-family**: Helvetica, sans-serif, with **font-size**: 16px and line-height: 1.5
* Add **section** with two **articles** inside (for each list)
* Each article must have a **h2** heading
* Use **ul** for unordered list
* Add 4 **list items**
* Use **ol** **reversed** for ordered reversed list
* Add 3 **list items**

You can find an example view [here](https://i.imgur.com/BPOf8LA.png)

You can download the resources [here](https://mega.nz/file/mUJ0gApA#QyX07cidXa4oge1IZd12t1PhP_Ja2x7R_JKUkq1VtRA)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Style Lists","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let ul = $("body ul");
expect(ul).to.have.lengthOf(1,"Incorrect amount of ul tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ol = $("body \> section \> article \> ol\[reversed\]");
expect(ol).to.have.lengthOf(1,"Incorrect amount of ol tag. tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-family')).to.equal('Helvetica, sans-serif', "Incorrect font family.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-size')).to.equal('16px', "Incorrect font size.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('line-height')).to.equal('1.5', "Incorrect line height.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let heading = $(document.body).find("h2");
expect(heading).to.have.lengthOf(2,"Incorrect amount of h2 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
