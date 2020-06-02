# Homework

[slide]
# Problem: Simple HTML Pagee

[code-task title="Simple HTML Page" taskId="c71fd240-cf92-43e1-95db-d79255ead525" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]
## Description

* Create a HTML document.
* Change the document **title** to *Simple HTML Page* 
* Use **paragraph** tag for plain text and **strong** tag for bold text

You can find an example view [here](https://imgur.com/a/hQDhEFG)

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

# Problem: TagsCardio Paragraphs

[code-task title="TagsCardio-Paragraphs" taskId="54728b5a-74cd-4128-bbcc-ae48f9b61be4" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create a HTML document.
* Change the document **title** to *Paragraphs*
* Use the **h1** tag for heading
* Use **p** tags for each line of the text
* See the screenshot and use **strong** and **em** tags where needed

You can find an example view [here](https://imgur.com/a/Bfl4Lub)

You can use the text below in your HTML:

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
let p = $(document.body).find("p");
expect(p).to.have.lengthOf(11,"Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(document.body).find("p").text()).to.include("This page draws on published","Incorrect text in paragraph");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let strong = $(document.body).find("strong");
expect(strong).to.have.lengthOf(10,"Incorrect amount of strong tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let em = $(document.body).find("em");
expect(em).to.have.lengthOf(3,"Incorrect amount of em tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $(document.body).find("h1");
expect(header).to.have.lengthOf(1,"Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(document.body).find("h1").text()).to.include("Top Tips for Effective Presentations","Incorrect text in h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]

# Problem: Single Article Page 

[code-task title="Single Article Page " taskId="99d9c4dc-4e2b-45fb-ba21-351551e15cdf" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create a HTML document.
* Change the document **title** to *Single Article Page*
* Create an **article** with several items inside
* Use **h2** and **h4** tags for headings
* Use **p** tags for the text
* Use **img** tag for the photo

You can DOWNLOAD the resources [here](https://mega.nz/file/jNhzXKTQ#SrUcTz0oSFMTgzj3UqlPo5vMfvfql9fMhVwt0aqpvC4)

## Examples

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Single Article Page","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("article")).to.have.lengthOf(1,"Incorrect amount of article.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("h2")).to.have.lengthOf(1,"Incorrect amount of h2 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("h4")).to.have.lengthOf(1,"Incorrect amount of h4 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("p")).to.have.lengthOf(2,"Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("img")).to.have.lengthOf(1,"Incorrect amount of img tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(document.body).find("h2").text()).to.include("Egyptian Mau","Incorrect text in h2 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]

# Tags Cardio - Lists

[code-task title="Tags Cardio - Lists" taskId="74d19b02-e0c8-47dd-826f-c71e099967a2" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create HTML document
* Change the document **title** to *Lists*
* Add section with two articles inside (for each list)
* Each article must have a **h2** heading
* Use **ul** for unordered list
* Add four list items
* Use **ol reversed** for ordered reversed list
* Add three **list** items

You can download the resources [here](https://mega.nz/file/HY4jxA5L#KUt-Q7VkYnFKmCLT8Xb8oE7AcJhvqbp5Fppbc6O7giY)

## Examples

[/task-description]

[tests]
[test open]
[input]
let title = document.title;
expect(title).to.equal("Lists","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $(document.body).find("section");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let article = $(document.body).find("article");
expect(article).to.have.lengthOf(2,"Incorrect amount of article tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ul = $("body \> section \> article \> ul");
expect(ul).to.have.lengthOf(1,"Incorrect amount of ul tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ol = $("body \> section \> article \> ol\[reversed\]");
expect(ol).to.have.lengthOf(1,"Incorrect amount of ol tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li= $("body \> section \> article \> ul \> li");
expect(li).to.have.lengthOf(4,"Incorrect amount of li tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let li = $("body \> section \> article \> ol \> li");
expect(li).to.have.lengthOf(3,"Incorrect amount of li tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let articles = $("body \> section \> article");
expect(articles).to.have.lengthOf(2,"Incorrect amount of article tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let heading = $(document.body).find("h2");
expect(heading).to.have.lengthOf(2,"Incorrect amount of h2 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
