[slide]

# Problem: Sticky Footer Flexbox

[code-task title="Problem: Sticky Footer Flexbox" taskId="b611c727-744a-436b-aead-38f3dac38be0" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Sticky Footer - Flexbox**
* Divide your content into **header**, **main** and **footer** tags
* The **body** must have **flex** display property
* The **body background** must be rgb(238, 238, 238)
* Set **height** to the **body: 100vh**
* The **footer** should be at the **bottom** of the page
* The **footer** text **color** must be rgb(255, 255, 255)
* The **footer** **background color** must be rgb(102, 102, 102)

You can find an example view [here](https://i.imgur.com/7kh5HOS.jpg)

You can download the resources [here](https://mega.nz/file/3UZ0ESKZ#s8Ze1YQcFnA8ZIHTYf9XDVh7wD-FaTLuaYw4x53m1z4)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Sticky Footer - Flexbox","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("body").css('background')).to.equal('rgb(238, 238, 238)', "Incorrect background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let pageFooter = $("body footer");
expect((pageFooter).css('color')).to.equal('rgb(255, 255, 255)', "Incorrect footer text color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let pageFooter = $("body footer");
expect((pageFooter).css('background')).to.equal('rgb(102, 102, 102)', "Incorrect footer background color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let footer = $("body footer");
expect(footer).to.have.lengthOf(1,"Incorrect amount of footer tag.");
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
[/tests]
[/code-task]
[/slide]
