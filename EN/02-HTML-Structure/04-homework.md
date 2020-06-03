# Homework

[slide]

# Problem: Semantic-Tags

[code-task title="Problem: Semantic-Tags" taskId="6af05e6b-ce89-4e6a-a4ed-723e6cc4980c" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create an **index.html** file with **Semantic Tags** title
* Create header section with a **header** tag 
* Use **h1** tag for heading
* Create a main section with a **main** tag
* Create two paragraphs inside the main section
* Use **footer** tag for the last section
* Create two paragraphs inside the footer


You can find an example view [here](https://i.imgur.com/CyqSQVg.png)

You can DOWNLOAD the resources [here](https://mega.nz/file/yIojERLL#nboU3_h_hxh-gEX8NBh9ALy1O7jzS05yI91vLDUwsRM)

[/task-description]

[tests]
[test open]
[input]
let title = (document.title);
expect(title).to.be.equal('Semantic Tags', "Incorrect title name.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $("body \> header");
expect(header).to.have.lengthOf(1, "Incorrect amount of header tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let main = $("body \> main");
expect(main).to.have.lengthOf(1, "Incorrect amount of main tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let footer = $("body \> footer");
expect(footer).to.have.lengthOf(1, "Incorrect amount of footer tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body \> footer \> p");
expect(p).to.have.lengthOf(2, "Incorrect amount of p tags in footer.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body \> main \> p");
expect(p).to.have.lengthOf(2, "Incorrect amount of p tags in main.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1 = $("body \> header \> h1");
expect(h1).to.have.lengthOf(1, "Incorrect amount of h1 tag in header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(document.body).find("h1").text()).to.include("I washed my face with sparkling water for a week","Incorrect text in h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]

# Problem: Semantic Article Page

[code-task title="Problem: Semantic Article Page" taskId="319b556a-3251-456b-824e-bd52a19f1b5a" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create an index.html file with **Semantic Article Page** title
* Follow the instructions
* Use **article** tag to create an article
* The article has header with **h1** heading and a **paragraph** for the Published date inside
* Use **p** tag to create 3 paragraphs after the **header**. The paragraphs contain the article content (info for apple). Use **b** tag where is need.     
* After that, you have to create the Comment section. Use **section** tag to create it. This section has **h2** heading and **two articles** inside    
* Each article contains a comment and has:    
* **Header** with an **h3** heading and a **paragraph** for the time
* Exactly one **paragraph** for the comment  

You can find an example view [here](https://i.imgur.com/VZ3G7ds.png)
You can DOWNLOAD the resources [here](https://mega.nz/file/DJZl2S4I#0VTmensITgR8ApVDNo9a2TLvNKNjHoNXbYM3oqu-uIE)

[/task-description]

[tests]
[test open]
[input]
let title = (document.title);
expect(title).to.be.equal('Semantic Article Page', "Incorrect title name.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let article = $("body \> article");
expect(article).to.have.lengthOf(1, "Incorrect amount of article tag.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1 = $("h1");
expect(h1).to.have.lengthOf(1, "Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body \> section \> article");
expect(section).to.have.lengthOf(2, "Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let article = $("article");
expect(article).to.have.lengthOf(3, "Incorrect amount of article tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h3 = $("section \> article \> header \> h3");
expect(h3).to.have.lengthOf(2, "Incorrect amount of h3 tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("p");
expect(p).to.have.lengthOf(8, "Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let b = $("b");
expect(b).to.have.lengthOf(1, "Incorrect amount of b tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let p = $("body \> article \> p");
expect(p).to.have.lengthOf(3, "Incorrect amount of p tags.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]

# Problem: Semantic Blog Layout

[code-task title="Problem: Semantic Blog Layout" taskId="a122986d-aed8-406f-8484-4e0077433c49" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create an index.html file with **Semantic Blog Layout** title
* First use **header** tag
* Use **h1** tag for the heading
* Use **nav** tag for the navigation with an unordered list inside
* Create two **list** items with **anchor** tags inside the nav
* Second use **main** tag    
* Create two **sections** in the main. Each section has:
* A header with an **h2** heading
* Two articles with **h4** heading and three **p** tags inside
* For the dates use **time** tag
* Third use **footer** tag with exacly two paragraphs inside
* Use **anchor** tag for the name in the last sentence

You can find an example view [here](https://i.imgur.com/2nzQn8u.png)

You can DOWNLOAD the resources [here](https://mega.nz/file/mAxW3A6T#bny_dYSk5pF4JsXJCTLjecwbh3N_VJM8CeW_VFDWx5g)

[/task-description]

[tests]
[test open]
[input]
let title = (document.title);
expect(title).to.be.equal('Semantic Blog Layout', "Incorrect title name.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $("body \> header");
expect(header).to.have.lengthOf(1, "Incorrect amount of header tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let main = $("body \> main");
expect(main).to.have.lengthOf(1, "Incorrect amount of main tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let footer = $("body \> footer");
expect(footer).to.have.lengthOf(1, "Incorrect amount of footer tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1 = $("body \> header \> h1");
expect(h1).to.have.lengthOf(1, "Incorrect amount of h1 tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let nav = $("body \> header \> nav");
expect(nav).to.have.lengthOf(1, "Incorrect amount of nav tag in header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let ul = $("body \> header \> nav \> ul");
expect(ul).to.have.lengthOf(1, "Incorrect amount of ul tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let a = $("body \> header \> nav \> ul \> li a");
expect(a).to.have.lengthOf(2, "Incorrect amount of a tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let section = $("body \> main \> section");
expect(section).to.have.lengthOf(2, "Incorrect amount of section tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let article = $("body \> main \> section article");
expect(article).to.have.lengthOf(4, "Incorrect amount of article tags in section.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let time = $("body \> main \> section \> article time");
expect(time).to.have.lengthOf(4, "Incorrect amount of time tags in main.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let a = $("body \> footer a");
expect(a).to.have.lengthOf(1, "Incorrect amount of a tag in footer.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
