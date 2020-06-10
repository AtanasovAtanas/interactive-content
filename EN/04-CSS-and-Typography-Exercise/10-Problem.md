[slide]

# Problem: Create Typography CSS

[code-task title="Problem: Create Typography CSS" taskId="69b68913-3b79-4d43-a453-aa77319837aa" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Create an **index.html** and **style.css** files
* Change the document **title** to **Typography**
* Use **Helvetica, sans-serif** font-family for the document
* Make the **font-size** 16px
* Change the **line-height** to 1.5
* Use **Georgia, serif** font-family for the headings
* Use **headings** from h1 to h6
* Create a HTML **table** and style it
* Use **blockquote** tag
* Style its **left border** with **rgb(221,221,221)** color
* Style its **font** to italic
* Use **hr** tag for the horizontal lines

You can find an example view [here](https://i.imgur.com/BuxglXR.png)

You can download the resources [here](https://mega.nz/file/2FgQzYjQ#qfmOBoZ0Bfj677wAblo_JXqdd1quFpk5BVmOa4Ygcwg)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Typography","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let table = $("body table");
expect(table).to.have.lengthOf(1,"Incorrect amount of table tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h5 = $("body \> h5");
expect(h5).to.have.lengthOf(1,"Incorrect amount of h5 tag.");
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
let thead = $("body table \> thead");
expect(thead).to.have.lengthOf(1,"Incorrect amount of thead tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("blockquote").css('font-style')).to.equal('italic', "Incorrect blockquote font-style.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let tbody = $("body table \> tbody");
expect(tbody).to.have.lengthOf(1,"Incorrect amount of tbody tag.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let hr = $("body hr");
expect(hr).to.have.lengthOf(2,"Incorrect amount of hr tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body h1").css('font-family')).to.equal('Georgia, serif', "Incorrect font family for headings.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("html").css('font-family')).to.equal('Helvetica, sans-serif', "Incorrect font family.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
