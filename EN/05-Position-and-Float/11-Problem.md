[slide]

# Problem: Social Media Icons

[code-task title="Problem: Social Media Icons" taskId="2cbed203-6ab2-4e75-b7b2-32a9c9ed23b2" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Social Media Icons**
* All you need for your HTML are **ul**, **li** and **a** tags
* Use **FontAwesome** to add social icons
* Change the **ul** display property to **inline-block**
* **Remove** list items **default** style
* Each **a** tag must have **border-radius**: 50%;
* Check the provided screenshots to see the hover effects

You can find an example view [here](https://i.imgur.com/BMcLCLg.png)

You can find an example view 2 (hover the first icon) [here](https://i.imgur.com/EtKugYG.png)

You can find an example view 3 (hover the second icon) [here](https://i.imgur.com/xRkWkHK.png)

You can find an example view 4 (hover the third icon) [here](https://i.imgur.com/hdqVuXH.png)

You can find an example view 5 (hover the fourth icon) [here](https://i.imgur.com/riOBoCz.png)

You can find an example view 6 (hover the fifth icon) [here](https://i.imgur.com/XyBDGVm.png)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Social Media Icons","Incorrect document title");
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
let li = $("body \> ul \> li");
expect(li).to.have.lengthOf(5,"Incorrect amount of li tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let a = $("body \> ul \> li \> a");
expect(a).to.have.lengthOf(5,"Incorrect amount of a tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("i").length).to.equal(5, "Incorrect amount of i tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("ul").css('display')).to.equal('inline-block', "Incorrect ul items display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("a").css('border-radius')).to.equal('50%', "Incorrect border radius.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("li").css('list-style')).to.equal('none', "Incorrect li items style.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
