[slide]

# 01 Register Form

[code-task title="Problem: Register Form" taskId="0cd6zzde-96b4-4ca8-b3c0-68d4f092f6f5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Constraints

* Change the document **title** to **Register Form**
* Use a **form** tag
* Use **fieldset** tags with corresponding **legend**
* Each **input** tag should have a **label** and should be inside a **div**
* The **first** input field must be **focused**
* For each **input tag** use the corresponding **type** (**email**, **radio**, **tel**, etc...)
* Use **select** and **option** tags
* Use **button** tag of type submit
* Use **placeholders** where needed

You can find an example view 1 [here](https://i.imgur.com/webhN5g.png)
You can find an example view 2 [here](https://i.imgur.com/Iz3mlKs.png)
You can find an example view 3 [here](https://i.imgur.com/nHUCUJo.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Register Form","Incorrect title name.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let form = $('body').find('form');
expect(form).to.have.lengthOf(1, "Incorrect amount of form tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let fieldsets = $('form').find('fieldset');
let legends = fieldsets.find('legend');
expect(fieldsets).to.have.lengthOf(2, "Incorrect amount of fieldset tags.");
expect(legends).to.have.lengthOf(2, "Incorrect amount of legend tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let labels = $('form').find('div').find('label');
expect(labels).to.have.lengthOf(15, "Incorrect amount of label tags inside divs.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let firstInput = $($('form').find('input').get(0));
expect(firstInput.attr('autofocus')).to.equal('autofocus', "The first input is not focused.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let textInputs = $('form').find('input[type="text"]');
let telInputs = $('form').find('input[type="tel"]');
expect(textInputs).to.have.lengthOf(3, "Incorrect amount of inputs of type text.");
expect(telInputs).to.have.lengthOf(1, "Incorrect amount of inputs of type tel.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let selects = $('form').find('select');
let options = selects.find('option');
expect(selects).to.have.lengthOf(1, "Incorrect amount of select tags");
expect(options).to.have.lengthOf(4, "Incorrect amount of option tags");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let radioInputs = $('form').find('input[type="radio"]');
expect(radioInputs).to.have.lengthOf(3, "Incorrect amount of radio buttons");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let emailInputs = $('form').find('input[type="email"]');
expect(emailInputs).to.have.lengthOf(1, "Incorrect amount of inputs of type email.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let passwordInputs = $('form').find('input[type="password"]');
expect(passwordInputs).to.have.lengthOf(2, "Incorrect amount of inputs of type password.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let placeholderInputs = $('form').find('input[placeholder]');
expect(placeholderInputs).to.have.lengthOf(7, "Incorrect amount of inputs with placeholder.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
