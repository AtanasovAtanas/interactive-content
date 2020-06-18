[slide]

# Problem: MQs in Typography

[code-task title="Problem: MQs in Typography" taskId="58968712-3c70-433c-9969-13cf93e4591f" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Media Queries in Typography**
* Make the **font size** for **phones** 12px
* Make the **font size** for screens **larger than 500** 14px
* Make the **font size** for screens **larger than 600** 16px
* Make the **font size** for screens **larger than 800** 18px
* Make the **font size** for screens **larger than 1300** 21px
* Make the **font size** for screens **larger than 1800** 23px

You can find an example for **desktop** view [here](https://i.imgur.com/UpACBOD.png)

You can find an example for **laptop** view [here](https://i.imgur.com/N3u2gMO.png)

You can find an example for **phone** view [here](https://i.imgur.com/x9Ta5Er.png)

You can find an example for **tablet** view [here](https://i.imgur.com/MqP6wRU.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Media Queries in Typography","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let img = $("body img");
expect(img).to.have.lengthOf(2,"Incorrect amount of img tag.");
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
let section = $("body section");
expect(section).to.have.lengthOf(1,"Incorrect amount of section tag.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
