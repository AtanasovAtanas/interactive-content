[slide]

# Problem: Flexbox Layout

[code-task title="Problem: Flexbox Layout" taskId="da8a5a6d-feb0-4585-9d6c-a70c95f087f9" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Flexbox Layout**
* Create **header**, **main**, **aside** and **footer** elements
* Set to the **body** display property **flex**
* Each element must have **flex grow**, **flex shrink** and **flex basis**

You can find an example view [here](https://i.imgur.com/oRg7HiJ.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Flexbox Layout","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $("body header");
expect(header).to.have.lengthOf(1,"Incorrect amount of header tag.");
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
let aside = $("body aside");
expect(aside).to.have.lengthOf(1,"Incorrect amount of aside tag.");
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
expect($("body").css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
