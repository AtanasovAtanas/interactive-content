[slide]

# Problem: My First CSS Document

[code-task title="Problem: My First CSS Document" taskId="82450ec0-5224-4ad9-bff1-9c1e81a07dbb" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to "My First CSS Document"
* Use h1 and h2 tags for headings
* Use background with color - rgb(51, 102, 153)
* Use white color for text


You can find an example view [here](https://i.imgur.com/zQabaWw.png)

You can download the resources [here](https://mega.nz/file/KRhlGKrT#SIRHX5heH3biQhXWfhiD717QRhzHsXC55qGqFaqLi3U)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("My First CSS Document","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('background')).to.equal('rgb(51, 102, 153)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1 = $("body \> h1");
expect(h1).to.have.lengthOf(1,"Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('color')).to.equal('white', "Incorrect text color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body p");
expect(p).to.have.lengthOf(5,"Incorrect amount of paragraphs.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h2 = $("body \> h2");
expect(h2).to.have.lengthOf(1,"Incorrect amount of h2 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
