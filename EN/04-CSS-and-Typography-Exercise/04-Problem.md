[slide]

# Problem: Buttons

[code-task title="Problem: Buttons" taskId="2f4271bf-520a-4dc5-9fe6-83b440dbd290" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

You can find an example gif [here](https://i.imgur.com/YLkbuxO.gif)

You can download the resources [here](https://mega.nz/file/fNpFmaSL#2t_KPboaPK6AElrkL-tChF4YJ-Kgd0HCIUstRGm1wiQ)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Buttons CSS","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test open]
[input]
let h2 = $("body h2");
expect(h2).to.have.lengthOf(3,"Incorrect amount of h2 tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let a = $("body a");
expect(a).to.have.lengthOf(3,"Incorrect amount of a tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("body button");
expect(button).to.have.lengthOf(6,"Incorrect amount of button tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("body .button");
expect((button).css('cursor')).to.equal('pointer', "Incorrect cursor.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("body .button");
expect((button).css('outline')).to.equal('none', "Incorrect outline.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("body .hover");
expect((button).css('color')).to.equal('rgb(51, 51, 51)', "Incorrect button text color.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $(".button.fill.hover");
expect((button).css('color')).to.equal('rgb(251, 251, 251)', "Incorrect text color.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
