[slide]
# 03 NewsPaper

[code-task title="Problem: NewsPaper" taskId="0cd68ede-9zx4-4118-b3c0-68d4f092faa5" executionType="tests-execution" executionStrategy="html-and-css-zip-file" requiresInput="false"]

[code-upload allowedMemory="30" /]

[task-description]

## Description
* Create a Web page **(HTML5 + CSS3)** that looks and behaves like the provided screenshots
* You have been given all of the **required resources**

## Constraints
* Change the document **title** to **NewsPaper**
* **Reset** the deafault **paddin**, **margin** and **box-sizing**
* Use **rgb(245, 239, 235)** for background of the **body**
* Set the **text** of the **header** in **center**, and use **rgb(255, 255, 255)** for the **background**
* Set the **styles** of the **div-container** with class .top-news to achieve the view like on the screenshot
* Use **rgb(60, 63, 68)** for the **background** of the **footer header**
* Use **rgb(26, 31, 36)** for the **background** of the **footer**
* Use **space-evenly** value to style the ul's
* Use **baseline** for the element with class name **themes**

## Submission
* Do **NOT** add the **images folder** inside the archive when submitting

You can find an example view [here](https://i.imgur.com/w8mdrC6.png)

You can download the resources [here](https://mega.nz/file/OQhzxAgS#XnXvo8hSRnq_DlbpJ-Tbtax2CRopMyXJVhI4Ttp7o_o)

[/task-description]

[tests]
[test]
[input]
expect(document.title).to.equal("NewsPaper","Incorrect title name");
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const htmlBoxSizing = $('html').css('box-sizing');
const pagePadding = $('*').css('padding');
const pageMargin = $('*').css('margin');
expect(htmlBoxSizing).to.equal('inherit');
expect(pagePadding).to.equal('0px');
expect(pageMargin).to.equal('0px');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const backgroundColor = $('body').css('background-color');
expect(backgroundColor ).to.equal('rgb(245, 239, 235)');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const headerTextAlign = $('header').css('text-align');
const headerBackgroundColor = $('header').css('background-color');
expect(headerTextAlign).to.equal('center');
expect(headerBackgroundColor).to.equal('rgb(255, 255, 255)');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const containerDisplay = $('.top-news').css('display');
const flexDirection = $('.top-news').css('flex-direction');
expect(containerDisplay).to.equal('flex');
expect(flexDirection).to.equal('column');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const articlesContainerDisplay = $('.articles-container').css('display');
expect(articlesContainerDisplay).to.equal('flex');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const sliceDisplay = $('.slice').css('display');
const sliceJustifyContent = $('.slice').css('justify-content');
expect(sliceDisplay).to.equal('flex');
expect(sliceJustifyContent).to.equal('center');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const footerWrapperColor = $('.footer-wrapper>h2').css('background-color');
const footerContainerColor = $('.footer-container').css('background-color');
expect(footerWrapperColor).to.equal('rgb(60, 63, 68)');
expect(footerContainerColor).to.equal('rgb(26, 31, 36)');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const ulDisplay = $('.unordered-lists').css('display');
const ulJustifyContent = $('.unordered-lists').css('justify-content');
expect(ulDisplay).to.equal('flex');
expect(ulJustifyContent).to.equal('space-evenly');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const ulDisplay = $('.unordered-lists ul').css('display');
const ulFlexDirection = $('.unordered-lists ul').css('flex-direction');
expect(ulDisplay).to.equal('flex');
expect(ulFlexDirection).to.equal('column');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const themesAlignItems = $('.themes').css('align-items');
expect(themesAlignItems).to.equal('baseline');
[/input]
[output]
yes
[/output]
[/test]
[test]
[input]
const showMoreBtnTextTransform = $('.show-more').css('text-transform');
expect(showMoreBtnTextTransform).to.equal('uppercase');
[/input]
[output]
yes
[/output]
[/test]
[/tests]

[/code-task]
[/slide]
