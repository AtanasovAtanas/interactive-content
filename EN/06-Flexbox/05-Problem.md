[slide]

# Problem: Flex Model Articles

[code-task title="Problem: Flex Model Articles" taskId="f7442ee5-baa5-490b-9c1a-cc9a196acf3e" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Articles**
* Create a **section** with three **articles** inside
* The **article** should have a **h2** title and a **paragraph** (p)
* **Font family** Helvetica, sans-serif with font **size** 16px and line **height** 1.5 for the **html**
* **Font family** Georgia, serif with font **size** 1em and line **height** 1.2 for the **headings**
* Change the **section display property** to flex and set **justify-content: space-between**
* Set on the **section** **max-width** 70vw

You can find an example view [here](https://i.imgur.com/GtvQoWN.png)

You can download the resources [here](https://mega.nz/file/7EIwlaoS#CdP5FcvtfQ6n4xqrbFa3t-4ZW1CchdnvXq5sPkqVGCo)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Articles","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let section = $("body section");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let articles = $("body \> section \> article");
expect(articles).to.have.lengthOf(3,"Incorrect amount of article tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h2 = $("body \> section article");
expect(h2).to.have.lengthOf(3,"Incorrect amount of h2 tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body \> section p");
expect(p).to.have.lengthOf(3,"Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section").css('max-width')).to.equal('70vw', "Incorrect section width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section").css('display')).to.equal('flex', "Incorrect section display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("section").css('justify-content')).to.equal('space-between', "Incorrect text align for items.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("h2").css('font-family')).to.equal('Georgia, serif', "Incorrect font-family for h2 tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("h2").css('line-height')).to.equal('1.2', "Incorrect line height for h2 tags.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
