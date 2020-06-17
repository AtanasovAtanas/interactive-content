[slide]

# Problem: Blog Layout Flexbox

[code-task title="Problem: Blog Layout Flexbox" taskId="6f6d7b8c-6841-467c-92af-5da594b16017" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Blog Layout - Flexbox**
* The entire content must be in **div container** with class **page** (div.page)
* The page **container (div)** must be **flexed** and **wrapped**
* **Body** **background** color must be **rgb(238, 238, 238)**
* **Image background** color should be **rgb(255, 255, 255)**
* **Blockquote** **font** family must be Georgia, serif
* The **anchors** text **color** in the **aside** section must be **rgb(0, 153, 0)**
* Page **headings** **font family** must be Georgia, serif

You can find an example view [here](https://i.imgur.com/r8mik5Y.jpg)

You can download the resources [here](https://mega.nz/file/bBp3yKCS#lhMw-QiuyKF6c-cRVD8zdRENDik6XUSUMyTnC8hLo50)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Blog Layout - Flexbox","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let pageDiv = $(".page");
expect((pageDiv).css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let pageDiv = $(".page");
expect((pageDiv).css('flex-wrap')).to.equal('wrap', "Incorrect flex property.");
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
expect($("img").css('background')).to.equal('rgb(255, 255, 255)', "Incorrect image background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("blockquote").css('font-family')).to.equal('Georgia, serif', "Incorrent font family for the blockquote.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let asideAnchor = $("aside a")
expect((asideAnchor).css('color')).to.equal('rgb(0, 153, 0)', "Incorrect anchors text color.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
