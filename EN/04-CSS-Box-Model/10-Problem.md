[slide]

# Problem: Photo Gallery Inline Block

[code-task title="Problem: Photo Gallery Inline Block" taskId="5ca63611-d253-4c58-a887-a40ae0bca967" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Photo Gallery Inline Block**
* Create **unordered list** with **class** gallery (ul.gallery) 
* Add **list items** with images inside
* The **list items** must have
* Border **width** - 0.4rem
* Border **color** - black
* Border **style** - solid

You can find an example view [here](https://i.imgur.com/1i4nU0x.png)

You can download the resources [here](https://mega.nz/file/SEJyTarD#VkQOABHPYEBCwUHE5O9YU3wL-P8rYfdSeT9m7LsItA4)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Photo Gallery - Inline Block","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
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
let img = $("body img");
expect(img).to.have.lengthOf(12,"Incorrect amount of img tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li = $("body ul li");
expect(li).to.have.lengthOf(12,"Incorrect amount of li tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let gallery = $(".gallery");
expect(gallery).to.have.lengthOf(1,"Incorrect amount of ul tag with class gallery.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("li").css('display')).to.equal('inline-block', "Incorrect display property to the list items.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
