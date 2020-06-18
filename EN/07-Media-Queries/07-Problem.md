[slide]

# Problem: MQs Playground

[code-task title="Problem: MQs Playground" taskId="0cd6aede-96b4-4ca8-b3c0-68d4f092f6f5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Media Queries Playground**
* Create three sections
* Each section has **span** and **after** element
* In the **span** you must write the text **before** ":". The text **after** ":" will be in **after** element
* First section with class **mq-width** must contain text that will change based on **width** queries
* Add a **width media query** to change the contents of the after elements when a query match
* Second **section** with class **mq-height** to contain text that will change based on height queries
* Add a **height media query** to change the contents of the after elements when a query match
* Third **section** with class **mq-ar** to contain text that will change based on aspect ratio queries
* Add an aspect ratio media query to change the contents of the after elements when a query match

You can find an example view [here](https://i.imgur.com/YlIrlMQ.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Media Queries Playground","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body section");
expect(section).to.have.lengthOf(3,"Incorrect amount of section tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let resetCSS = $('\<link rel="stylesheet" href="reset.css" type="text/css"/\>');
expect(resetCSS).to.have.lengthOf(1,"Missing reset.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let typographyCSS = $('\<link rel="stylesheet" href="typography.css" type="text/css"/\>');
expect(typographyCSS).to.have.lengthOf(1,"Missing typography.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body section\[class='mq-width'\]");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag or different class name.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
