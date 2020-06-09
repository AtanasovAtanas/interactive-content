[slide]

# Problem: Fonts Speciment Part 2

[code-task title="Problem: Fonts Speciment Part 2" taskId="c01f3963-56d5-45b6-8524-645b719e9dd0" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create an **index.html** file with **Fonts Speciment Part 2** title. (You can use the content of the previous task.)
* Use **Raleway, sans-serif**  font-family for the document
* Make the **font-size** 16px
* Change the **line-height** to 1.5
* Use **Great Vibes**, cursive **font-family** for the headings
* Change the **line-height** to 1.2
* Change the **font-weight** to bold


You can find an example view [here](https://i.imgur.com/Fx0LTEC.png)

You can download the resources [here](https://mega.nz/file/CBYSDaaA#IO0HwciNW-4Xz2SvkFub4SO9Vms6kZVtb4ir5kjUQ54)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Fonts Speciment Part 2","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let ul = $("ul");
expect(ul).to.have.lengthOf(3,"Incorrect amount of ul tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let listItems = $("body ul li");
expect(listItems).to.have.lengthOf(9,"Incorrect amount of li tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li = $("body ol \> li");
expect(li).to.have.lengthOf(3,"Incorrect amount of list items in ordered list.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-family')).to.equal('Raleway, sans-serif', "Incorrect font family.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-size')).to.equal('16px', "Incorrect font size.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('line-height')).to.equal('1.5', "Incorrect line height.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body h1").css('line-height')).to.equal('1.2', "Incorrect line height.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body h1").css('font-family')).to.equal('Great Vibes, cursive', "Incorrect font family for headings.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body h2").css('font-weight')).to.equal('bold', "Incorrect font weight for headings.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
