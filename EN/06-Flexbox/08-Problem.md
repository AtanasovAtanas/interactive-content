[slide]

# Problem: Navigation Flex

[code-task title="Problem: Navigation Flex" taskId="8db25eed-cef4-45b1-9e39-cbebfaa0f1e4" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

You can find an example view [here](https://i.imgur.com/eDpyU5c.jpg)

You can download the resources [here](https://mega.nz/file/uNgxTJoR#GBEE5LU6ETJA8FxYO0mmsY9cgK8FTefDiY3IeF3cb5Y)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Navigation - Flexbox","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $("body header")
expect((header).css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let headerUnderline = $("body header");
expect((headerUnderline).css('border-bottom')).to.equal('2px solid rgb(0,0,0)', "Incorrect underline color.")
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let headerUl = $("header nav ul");
expect((headerUl).css('display')).to.equal('flex', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let headerAnchor = $("header nav ul li a")
expect((headerAnchor).css('color')).to.equal('rgb(0, 153, 0)', "Incorrect anchor text color.");
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
let header = $("body \> header");
expect(header).to.have.lengthOf(1,"Incorrect amount of header tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
