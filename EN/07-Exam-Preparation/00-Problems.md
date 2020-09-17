# Problems

[slide]

# 01 Register Form

[code-task title="Problem: Login Form" taskId="0cd66ede-96b4-4ca8-b3c0-68d4f092f6f5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Constraints

* Change the document **title** to **Register Form**
* Use a **form** tag
* Use **fieldset** tags with corresponding **legend**
* Each **input** tag should have a **label** and should be inside a **div**
* The **first** input field must be **focused**
* For each **input tag** use the corresponding **type** (**email**, **radio**, **tel**, etc...)
* Use **button** tag of type submit
* Use **placeholders** where needed

You can find an example view [here](https://i.imgur.com/mDo24Cv.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Register Form","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let form = $("body form");
expect(form).to.have.lengthOf(1,"Incorrect amount of form tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let fieldset = $("body fieldset");
expect(fieldset).to.have.lengthOf(1,"Incorrect amount of fieldset tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let legend = $("body legend");
expect(legend).to.have.lengthOf(1,"Incorrect amount of legend tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let input = $("body form div input");
expect(input).to.have.lengthOf(6,"Incorrect amount of input tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let label = $("body form div label");
expect(label).to.have.lengthOf(6,"Incorrect amount of label tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("body button");
expect(button).to.have.lengthOf(1,"Incorrect amount of button tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let autoFocus = document.querySelectorAll("input")[0].autofocus;
expect(autoFocus).to.equal(true,"Autofocus on name input missing");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let nameInput = document.querySelectorAll("input[type=text]");
expect(nameInput).to.have.lengthOf(1,"Incorrect amount of input-name tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let radioInputs = document.querySelectorAll("input[type=radio]");
expect(radioInputs).to.have.lengthOf(2,"Incorrect amount of input-radio tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let telInputs = document.querySelectorAll("input[type=tel]");
expect(telInputs).to.have.lengthOf(1,"Incorrect amount of input-tel tags.");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
[slide]

# 02 Login Form

[code-task title="Problem: Login Form" taskId="0cd68ede-96b4-4ca8-b3c0-68d4f092f6f5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description
* Create a Web page **(HTML5 + CSS3)** that looks and behaves like the provided screenshots
* You have been given all of the **required resources**

## Constraints
* Use the Google fonts - [**"Poppins"**](https://fonts.google.com/specimen/Poppins)
* The web page should open correctly in the latest version of Chrome
* Pixel-perfect implementation is **NOT** required

You can find an example view [here](https://i.imgur.com/ynNo6z2.png)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Login Form","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let form = $("body form");
expect(form).to.have.lengthOf(1,"Incorrect amount of form tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let input = $("body form div input");
expect(input).to.have.lengthOf(2,"Incorrect amount of input tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let label = $("body form div label");
expect(label).to.have.lengthOf(2,"Incorrect amount of label tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = $("body button");
let text = button.text();
expect(button).to.have.lengthOf(1,"Incorrect amount of button tags.");
expect(text).to.equal("Login","Incorrect text of the button");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let iTags = $("body i");
expect(iTags).to.have.lengthOf(2,"Incorrect amount of iTags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let fieldset = document.querySelector("fieldset");
let style = window.getComputedStyle(fieldset);
let backGround = style.getPropertyValue('background-color');
expect(backGround).to.equal("rgb(255, 255, 255)","Incorrect background of fieldset");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let button = document.querySelector("button");
let style = window.getComputedStyle(button);
let backGround = style.getPropertyValue('background-color');
expect(backGround).to.equal("rgb(212, 24, 114)","Incorrect background of button");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# 03 Travel Blog

[code-task title="Problem: Login Form" taskId="0cd68ede-96b4-4118-b3c0-68d4f092f6f5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description
* Create a web page **(HTML5 + CSS3)** that looks and behaves like the provided screenshot
* You are given all of the **required resources**
* The output should be valid **HTML + CSS + images** that implement the above web page

## Constraints
* Use the Google Font - **"Gelasio"** 
* Use **Font Awesome** for the icons
* The site should open correctly in the latest version of Chrome
* Pixel-perfect implementation is **NOT** required
* You are **NOT** permitted to use libraries like Bootstrap

You can find an example view [here](https://imgur.com/uo2Tz35)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("Travel Blog","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let header = $("body header");
let main = $("body main");
let footer = $("body footer");
expect(header).to.have.lengthOf(1,"Incorrect amount of header tags.");
expect(main).to.have.lengthOf(1,"Incorrect amount of main tags.");
expect(footer).to.have.lengthOf(1,"Incorrect amount of footer tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let aTags = $("header a");
expect(aTags).to.have.lengthOf(4, "Incorrect amount of a tags in header.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
expect($("a").css('text-decoration')).to.equal('none', "Incorrect display property.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let headerButton = $(".header-button");
expect(headerButton).to.have.lengthOf(1,"Incorrect amount of elements with className header-button tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let footerDiv = $("footer>div");
expect(footerDiv).to.have.lengthOf(1,"Incorrect amount of div tags in the footer.");
expect($("footer>div").css('display')).to.equal("flex","Incorrect display flex of the div container");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h3Tags = $("h3");
expect(h3Tags).to.have.lengthOf(3,"Incorrect amount of h3 tags.");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
let h1Text = $("h1").text();
expect(h1Text).to.equal("Make the most of every trip","Incorrect text content of the h1 tag");
[/input]
[output]
yes
[/output]
[/test]
[/tests]
[/code-task]
[/slide]