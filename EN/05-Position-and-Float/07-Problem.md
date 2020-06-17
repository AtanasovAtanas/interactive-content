[slide]

# Problem: Blog Layout Float

[code-task title="Problem: Blog Layout Float" taskId="622d4bae-b217-4f4d-97a2-de4f1d1ed981" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Blog Layout - Float**
* Divide your content into **header**, **main** and **aside** tags
* Create a **paragraph** inside the header for the site title
* Create an **article** inside the main
* Create two **sections** inside the aside
* The sections should have a **h3** heading and a **navigation** - nav with **ul**, **li** and **a** elements
* Use rgb(238, 238, 238) for **body background**
* Use rgb(255, 255, 255) for **image background** and rgba(0, 0, 0, 0.25) for **image box shadow**
* Use **font family** Georgia, serif for the **blockquote**
* Use **font family** Georgia, serif with **size** 1em/1.2 for the **headings**
* Use **float** property to position the **first** image on the right
* Use **float** property to position the **second** image on the left

You can find an example view [here](https://i.imgur.com/hUNHDR2.jpg)

You can download the resources [here](https://mega.nz/file/PZYmiYoL#aVOf_N5Bl8bFvhaOR4HNzjXo8Mv2SAbnVcjiTIUQBwI)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Blog Layout - Float","Incorrect title name");
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
let aside = $("body aside");
expect(aside).to.have.lengthOf(1,"Incorrect amount of aside tag.");
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
expect($("blockquote").css('font-family')).to.equal('Georgia, serif', "Incorrect font family.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("h1").css('font-family')).to.equal('Georgia, serif', "Incorrect font family.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("img:first-of-type").css('float')).to.equal('right', "Incorrect float property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ul = $("body ul");
expect(ul).to.have.lengthOf(2,"Incorrect amount of ul tags.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
