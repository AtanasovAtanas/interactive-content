
[slide]

# 02 Simple Article

[code-task title="Problem: Simple Article" taskId="0cd68ede-96b4-4ca8-b3c0-6aa4zz92f6f5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description
* Create a Web page **(HTML5 + CSS3)** that looks and behaves like the provided screenshots
* You have been given all of the **required resources**

## Constraints
* Change the document **title** to **Simple Article**
* Use the **flex property** in the main for positioning the sections
* Use **rgb(227, 243, 253)** for the left section background
* **Remove** the default **list style**
* Use **rgb(129, 197, 251)** for color of the **i-tags**
* Use **2px** for the **border** of the **right section**
* The **button** should have **no borders**, the **padding on top** and **on bottom** should be exactly **16px**, and **on the left** and **right** should be **32px**
* Set a **cursor** property to the **button** (pointer)
* The **size** of the **button text** should be exactly **16px**

You can find an example view [here](https://i.imgur.com/jJ84BM9.png)

You can download the resources [here](https://mega.nz/file/mR5D2Ayb#-hV_GOaBo1V9YUD9Ryd7fftKq4-cMrAQV5HYmuWgXBA)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Simple Article","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let main = $(".main");
let style = window.getComputedStyle(main);
let dispalyProp = style.getPropertyValue('display');
expect(dispalyProp).to.equal("flex","Incorrect dispaly property");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let leftSection = $(".left");
let style = window.getComputedStyle(leftSection);
let backGround = style.getPropertyValue('background-color');
expect(backGround).to.equal("rgb(227, 243, 253)","Incorrect background of the left section");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li = $(".left li").get(3);
let style = window.getComputedStyle(li);
let liStyle = style.getPropertyValue('list-style');
expect(liStyle).to.equal("none","Incorrect list-style property value");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let iTag = $(".left li i");
let style = window.getComputedStyle(iTag);
let color = style.getPropertyValue('color');
expect(color).to.equal("rgb(129, 197, 251)","Incorrect color of the itags");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let rightPart = $(".right");
let style = window.getComputedStyle(right);
let borderWidth = style.getPropertyValue('border-width');
let borderStyle = style.getPropertyValue('border-style');
expect(borderWidth).to.equal("2px","Incorrect border width of the right section");
expect(borderStyle).to.equal("solid","Incorrect border style of the right section");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("button").get(0);
let style = window.getComputedStyle(button);
let border = style.getPropertyValue('border');
expect(border).to.equal("none","Incorrect border property value of the button");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("button").get(0);
let style = window.getComputedStyle(button);
let paddingTop = style.getPropertyValue('padding-top');
let paddingLeft = style.getPropertyValue('padding-left');
expect(paddingTop).to.equal("16px","Incorrect padding value of the button");
expect(paddingLeft).to.equal("32px","Incorrect padding value of the button");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("button").get(0);
let style = window.getComputedStyle(button);
let cursor = style.getPropertyValue('cursor');
expect(cursor).to.equal("pointer","Incorrect cursor property value of the button");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("button").get(0);
let style = window.getComputedStyle(button);
let fontSize = style.getPropertyValue('font-size');
expect(fontSize).to.equal("16px","Incorrect fontSize of the button");
[/input]
[output]
yes
[/output]
[/test]
[/tests]

[/code-task]
[/slide]