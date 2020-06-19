[slide]

# Problem: Responsive Tables

[code-task title="Problem: Responsive Tables" taskId="c697b445-da1a-4cb2-b995-4baa96817b8e" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description

* Change the document title to **Responsive Tables**
* Create a **table** with **3 columns**: First Name, Last Name, Job Title
* **Get** the latest **reset.css**
* **Get** the latest **typography.css**
* Make the **table responsive**

You can find an example for **desktop** view [here](https://i.imgur.com/nTtLmvj.png)

You can find an example for **laptop** view [here](https://i.imgur.com/JmkaVPq.png)

You can find an example for **phone** view [here](https://i.imgur.com/i7gTN37.png)

You can find an example for **tablet** view [here](https://i.imgur.com/mTJvJum.png)

[/task-description]

[tests]
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
let typographyCSS = $('\<link rel="stylesheet" href="typography.css" type="text/css"/\>');
expect(typographyCSS).to.have.lengthOf(1,"Missing typography.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let resetCSS = $('\<link rel="stylesheet" href="reset.css" type="text/css"/\>');
expect(resetCSS).to.have.lengthOf(1,"Missing reset.css.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect(document.title).to.equal("Responsive Tables","Incorrect document title");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
