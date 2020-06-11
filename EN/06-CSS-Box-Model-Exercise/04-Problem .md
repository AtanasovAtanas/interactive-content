[slide]

# Problem: Navigation Inline Block

[code-task title="Problem: Navigation Inline Block" taskId="00dc40db-2b53-4c0f-a883-0a116ec838ef" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

You can find an example view [here](https://i.imgur.com/iN6xIbU.png) .

You can download the resources [here](https://mega.nz/file/uZxzDaRJ#CJ9QOWjUG_ayNIa0B3T51ZZLpxJAkRdNlKm0G_aHUDg)

[/task-description]

[tests]
[test open]
[input]
expect(document.title).to.equal("Navigation Inline Block","Incorrect title name");
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
[test]
[input]
let listItems = $("body \> header \> nav \> ul \> li ");
expect(listItems).to.have.lengthOf(4,"Incorrect amount of list items in the navigation bar.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let nav = $("body \> header \> nav");
expect(nav).to.have.lengthOf(1,"Incorrect amount of nav tags.");
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
[test]
[input]
let a = $("body \> header \> nav a");
expect(a).to.have.lengthOf(4,"Incorrect amount of a tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("nav").css('display')).to.equal('inline-block', "Incorrect navigation display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("li").css('display')).to.equal('inline-block', "Incorrect li items display property.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
