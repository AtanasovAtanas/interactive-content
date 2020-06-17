[slide]

# Problem: Navigation Float

[code-task title="Problem: Navigation Float" taskId="28aa1e99-7fb2-45eb-9ab8-74736a79ea1d" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Navigation - Float**
* Create a **header** with a **p** for the title
* Inside the header add a **nav** with a **ul** and **4 li** elements
* Create a **main**, which contains an **article** with a **header** and **h1** heading
* Add a **section** inside the **article**
* Create an **aside** element with **two sections** inside
* The sections should have a **h3** heading and a **navigation** - nav with **ul**, **li** and **a** elements
* Use rgb(0, 102, 0) for the **anchors**
* Use rgb(238, 238, 238) for **body background**
* Use rgb(255, 255, 255) for **image background** and rgba(0, 0, 0, 0.25) for **image box shadow**
* Use **font** Georgia, serif for the **blockquote**
* Use **font** Georgia, serif with **size** 1em/1.2 for the **headings**

You can find an example view [here](https://i.imgur.com/B9hsvP1.jpg)

You can download the resources [here](https://mega.nz/file/DUZggYRK#UynBTd1HjPiy7JlQBUlX08lloPj4e6RBwHx4l-O_f1g)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Navigation - Float","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let nav = $("body nav");
expect(nav).to.have.lengthOf(3,"Incorrect amount of navigation (\<nav\>) elements.");
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
expect($("blockquote").css('font-family')).to.equal('Georgia, serif', "Incorrect blockquote font family.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body header nav ul li").length).to.equal(4, "Incorrect header navigation. The navigation should have 4 (\<li\>) elements.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body aside section nav ul li").length).to.equal(7, "Incorrect aside navigation. There should be 7 (\<li\>) elements.");
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
[/tests]
[/code-task]
[/slide]
