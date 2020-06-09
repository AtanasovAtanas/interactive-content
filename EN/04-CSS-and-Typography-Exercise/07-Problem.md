[slide]

# Problem: Contrasting Colors

[code-task title="Problem: Contrasting Colors" taskId="aadc33d6-af1c-46a7-aa63-9ae3e518bf20" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* The document **title** should be **Contrasting Colors** 
* Create an **article** inside the body
* Make the **background** with rgb(51, 102, 153) color
* Set the **border radius** to 1rem
* Use **Helvetica, sans-serif** font-family for the document
* Make the **font-size** 16px
* Change the **line-height** to 1.5
* Use **Georgia, serif** font-family for the headings

You can find an example view [here](https://i.imgur.com/Jys4q2I.png)

You can download the resources [here](https://mega.nz/file/rJhD0Szb#yCjY2c0tsolvu0TqKsFCfSmhRTFyesWBQpgip8tByV4)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Contrasting Colors","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let article = $("article");
expect(article).to.have.lengthOf(1,"Incorrect amount of article tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1 = $("h1");
expect(h1).to.have.lengthOf(1,"Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("p");
expect(p).to.have.lengthOf(3,"Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("article").css('background')).to.equal('rgb(51, 102, 153)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("article").css('border-radius')).to.equal('1rem', "Incorrect border radius width.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("h1").css('font-family')).to.equal('Georgia, serif', "Incorrect font family for the heading.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-family')).to.equal('Helvetica, sans-serif', "Incorrect font family for the document");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-size')).to.equal('16px', "Incorrect document font size");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
