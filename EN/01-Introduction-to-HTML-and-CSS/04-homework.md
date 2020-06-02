# Homework

[slide]
# Problem: Simple HTML Pagee

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


[slide]

# Problem TagsCardio Paragraphs

[code-task title="# L1_02_TagsCardio-Paragraphs" taskId="54728b5a-74cd-4128-bbcc-ae48f9b61be4" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document **title** to *Paragraphs*
* Use the **h1** tag for heading
* Use **p** tags for each line of the text
* See the screenshot and use **strong** and **em** tags where needed

You can find a example [here](https://imgur.com/a/TjnWR9n)

Paragraphs
Top Tips for Effective Presentations
This page draws on published advice from expert presenters around the world, which will help to take your presentations from merely good to great.
By bringing together advice from a wide range of people, the aim is to cover a whole range of areas.
Whether you are an experienced presenter, or just starting out, there should be ideas here to help you to improve.
It’s hard to be relaxed and be yourself when you’re nervous.
But time and again, the great presenters say that the most important thing is to connect with your audience, and the best way to do that is to let your passion for the subject shine through.
Be honest with the audience about what is important to you and why it matters.
Your presentation needs to be built around what your audience is going to get out of the presentation.
As you prepare the presentation, you always need to bear in mind what the audience needs and wants to know, not what you can tell them.
While you’re giving the presentation, you also need to remain focused on your audience’s response, and react to that.
For more ideas, see our page on Coping with Presentation Nerves.
Author: Jhon Devis

## Examples

[/task-description]

[tests]
[test open]
[input]
let title = document.title;
expect(title).to.equal("Paragraphs","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = \\$(document.body).find("p");
expect(p).to.have.lengthOf(11,"Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect(\\$(document.body).find("p").text()).to.include("This page draws on published","Incorrect text in paragraph");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let strong = \\$(document.body).find("strong");
expect(strong).to.have.lengthOf(10,"Incorrect amount of strong tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let em = \\$(document.body).find("em");
expect(em).to.have.lengthOf(3,"Incorrect amount of em tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = \\$(document.body).find("h1");
expect(header).to.have.lengthOf(1,"Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect(\\$(document.body).find("h1").text()).to.include("Top Tips for Effective Presentations","Incorrect text in h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]