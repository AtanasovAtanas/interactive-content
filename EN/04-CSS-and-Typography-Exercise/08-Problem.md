[slide]

# Problem: Icon Font Buttons

[code-task title="Problem: Icon Font Buttons" taskId="60f25f2a-8586-4680-a81f-f0296a679a52" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* The document **title** should be **Icon Fonts - Buttons**
* Use exactly 2 **paragraphs**
* Each of the **paragraphs** should have exactly 1 **anchor** (<a>)
* Each of the **anchors** should have exactly one **icon** element (<i>)
* The first anchor should have text - **"Click me!"**
* The second anchor should have text - **"E-mail me"**
* The page should be styled, exactly like the provided screenshot
* Use **FontAwesome** for this task. Import it in your CSS, with the **@import** rule

You can find an example view [here](https://i.imgur.com/Vvb6saO.png)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Icon Fonts - Buttons","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body p");
expect(p).to.have.lengthOf(2,"Incorrect amount of p elements.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ps = $("body p");
expect(ps.filter((x, y) =\> $(y).children().length === 1)).to.have.lengthOf(2, "Incorrect number of anchors in the paragraphs.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let anchors = $("body\>p\>a");

let anchor1 = $(anchors\[0\]);
let anchor2 = $(anchors\[1\]);

let anchor1IconsLength = anchor1.find('i').length;
let anchor2IconsLength = anchor2.find('i').length;

let testString = anchor1IconsLength + "-" + anchor2IconsLength;

expect(testString).to.equal("1-1", "Incorrect icon elements in list items");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
