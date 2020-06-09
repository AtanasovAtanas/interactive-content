[slide]

# Problem: Icon Font List

[code-task title="Problem: Icon Font List" taskId="d92ce031-4ac5-479e-b447-3eae10f8590e" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* The **title** of the document should be **Icon Fonts - Lists**
* The **unordered lists** should have class - "icons"
* Each of the **unordered lists** should have exactly 3 **list** items
* Each of the **list** items should have exactly one **icon** element
* The page should be styled, exactly like the provided screenshot
* Use **FontAwesome** for this task. Import it in your CSS, with the **@import rule**

You can find an example view [here](https://i.imgur.com/45IjLLB.png)

You can download the resources [here](https://mega.nz/file/DQBGiIzB#L___Am11roaMmHgHFuuSQFw77bCf4LV0vI5FyTe5KzU)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Icon Fonts - Lists","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ul = $("body ul");
expect(ul).to.have.lengthOf(3,"Incorrect amount of ul elements.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ul = $("body ul.icons");
expect(ul).to.have.lengthOf(3,"Incorrect class on ul elements.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let uls = $("body ul.icons");
expect(uls.filter((x, y) =\> $(y).children().length === 3)).to.have.lengthOf(3, "Incorrect number of list items in the uls.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let uls = $("body ul.icons");
let listItems1 = $(uls\[0\]).children();
let listItems2 = $(uls\[1\]).children();
let listItems3 = $(uls\[2\]).children();

let listItems1Length = listItems1.filter((x, y) =\> $(y).find('i').length === 1).length;
let listItems2Length = listItems2.filter((x, y) =\> $(y).find('i').length === 1).length;
let listItems3Length = listItems3.filter((x, y) =\> $(y).find('i').length === 1).length;

let testString = listItems1Length + "-" + listItems2Length + "-" + listItems3Length;

expect(testString).to.equal("3-3-3", "Incorrect icon elements in list items");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let uls = $("body ul.icons");
let listItems1 = $(uls\[0\]).children();
let listItems2 = $(uls\[1\]).children();
let listItems3 = $(uls\[2\]).children();

let listItem1 = $(listItems1\[0\]);
let listItem2 = $(listItems1\[1\]);
let listItem3 = $(listItems1\[2\]);

let listItem4 = $(listItems2\[0\]);
let listItem5 = $(listItems2\[1\]);
let listItem6 = $(listItems2\[2\]);

let listItem7 = $(listItems3\[0\]);
let listItem8 = $(listItems3\[1\]);
let listItem9 = $(listItems3\[2\]);

let index1 = listItem1.text().indexOf('Phasellus dictum interdum efficitur');
let index2 = listItem2.text().indexOf('Maecenas eleifend sapien felis, quis interdum ex tempor a');
let index3 = listItem3.text().indexOf('Aenean sodales, eros ac fermentum elementum, enim nisi finibus nisi, sed tempus turpis mauris ac quam');

let index4 = listItem4.text().indexOf('Phasellus dictum interdum efficitur');
let index5 = listItem5.text().indexOf('Maecenas eleifend sapien felis, quis interdum ex tempor a');
let index6 = listItem6.text().indexOf('Aenean sodales, eros ac fermentum elementum, enim nisi finibus nisi, sed tempus turpis mauris ac quam');

let index7 = listItem7.text().indexOf('university@softuni.bg');
let index8 = listItem8.text().indexOf('https://twitter.com/softunibg');
let index9 = listItem9.text().indexOf('https://www.facebook.com/SoftwareUniversity');

let testIndex = index1 + index2 + index3 + index4 + index5 + index6 + index7 + index8 + index9;

expect(testIndex).to.be.above(0);
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
