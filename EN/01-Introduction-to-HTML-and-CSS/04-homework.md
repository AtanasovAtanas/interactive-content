[slide]
# Problem: Simple HTML Page

[code-task title="Simple HTML Page" taskId="c71fd240-cf92-43e1-95db-d79255ead525" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]
[code-upload allowedMemory="30" /]
[task-description]
## Description

* Create a html document
* Change the document **title** to *Simple HTML Page* 
* Use **paragraph** tag for plain text and **strong** tag for bold text

You can find an example [here](https://imgur.com/a/hQDhEFG)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Simple HTML Page","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("p")).to.have.lengthOf(1,"Incorrect amount of p tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("strong")).to.have.lengthOf(2,"Incorrect amount of strong tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(document.body).find("strong").text()).to.include("CSS","Incorrect text in strong tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]