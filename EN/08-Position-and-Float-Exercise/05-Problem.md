[slide]

# Problem: Floating Images and Quotes

[code-task title="Problem: Floating Images and Quotes" taskId="f21553f1-9f44-4471-8834-3f09f19cb99c" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Floating Images and Quotes**
* Create a **header** with **h1** inside
* Add an **article** and look the screenshot for some insight for the other items inside
* Use color - rgb(238, 238, 238) for **body background**
* Use color - rgb(255, 255, 255) for **image background** and rgba(0, 0, 0, 0.25) for **image box shadow**
* Use **font family** Georgia, serif for the blockquote and headings

You can find an example view [here](https://i.imgur.com/gH5TgWW.jpg)

You can download the resources [here](https://mega.nz/file/vIwkVCiA#o1Cgl3pnfZvG_fziEv3b8DHhM7rVM4cjMKtd0ynm1qU)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Floating Images and Quotes","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let article = $("body article");
expect(article).to.have.lengthOf(1,"Incorrect amount of article tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let main = $("body main");
expect(main).to.have.lengthOf(1,"Incorrect amount of main tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let blockquote = $("body blockquote");
expect(blockquote).to.have.lengthOf(1,"Incorrect amount of blockquote tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let img = $("body img");
expect(img).to.have.lengthOf(2,"Incorrect amount of img tag.");
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
expect($("blockquote").css('font-family')).to.equal('Georgia, serif', "Incorrect font-family for blockquote tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
