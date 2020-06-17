[slide]

# Problem: Photo Gallery Flexbox

[code-task title="Problem: Photo Gallery Flexbox" taskId="26b47638-08f7-4ef7-b542-d2e3a04b9bba" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Photo Gallery - Flexbox**
* Add **section** with **class gallery** (section.gallery)
* Add **unordered list** with **list items** and **images** inside
* Change the **body**, **ul** and **li** display property to **flex**
* Use **font** Georgia, serif with **size** 1em/1.2 for the **headings**

You can find an example view [here](https://i.imgur.com/WWomfl0.png)

You can download the resources [here](https://mega.nz/file/DNRzxY5J#FE8nYa8dZ8F8Y-KdBrxAsTgeokocZOyQSYlpnyRnQHM)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Photo Gallery - Flexbox","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let gallery = $(".gallery");
expect(gallery).to.have.lengthOf(1,"Incorrect amount of section with class gallery.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li = $("body li");
expect(li).to.have.lengthOf(9,"Incorrect amount of li tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let img = $("body img");
expect(img).to.have.lengthOf(9,"Incorrect amount of img tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(".gallery ul").css('justify-content')).to.equal('space-between', "Incorrect justify content property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
