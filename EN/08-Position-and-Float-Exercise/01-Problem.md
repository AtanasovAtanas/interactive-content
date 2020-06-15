[slide]

# Problem: Article With Quotes and Media

[code-task title="Problem: Article With Quotes and Media" taskId="62b129b4-7f49-43ed-b528-60c128cce8f6" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Article with Quotes and Media**
* Divide your content into **header** and **main** tags
* The **entire page font** should have the following properties:
* **Size** - 16px
* **Line height** - 1.5
* **Font family** - Helvetica, sans-serif
* Add **class** site-title to the paragraph in the header (p.site-title)
* Change the **display** property to **inline-block**
* Set the **font weight** to bold
* Transform the text to **uppercase**

You can find an example view [here](https://i.imgur.com/AV7xrpw.png)

You can download the resources [here](https://mega.nz/file/KdIFkIhS#xCb8PhhAbxhCyY6ESn5HULlu1AUIQfc2Sn82T_GQs_o)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Article with Quotes and Media","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(".site-title").text()).to.include("Site title","Incorrect text in paragraph.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let main = $("body main");
expect(main).to.have.lengthOf(1,"Incorrect amount of main tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let img = $("body img");
expect(img).to.have.lengthOf(2,"Incorrect amount of img tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let blockquote = $("body blockquote");
expect(blockquote).to.have.lengthOf(1,"Incorrect amount of blockquote tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(".site-title").css('display')).to.equal('inline-block', "Incorrect display property in the header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(".site-title").css('font-weight')).to.equal('bold', "Incorrect font property in the header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($(".site-title").css('text-transform')).to.equal('uppercase', "Incorrect text transform property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("blockquote").css('float')).to.equal('right', "Incorrect float property for the blockquote.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
