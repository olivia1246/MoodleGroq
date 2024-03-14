<p align="center"><a
href="https://www.flaticon.com/free-icons/mortarboard" target="_blank" rel="noopener noreferrer"
title="Mortarboard icons created by itim2101 - Flaticon" ><img src="./extension/icon.png" alt="Mortarboard icons created by itim2101 - Flaticon" width="150" style="display:block; margin:auto;"></a></p>

# MoodleGPT 1.1.0

This extension allows you to hide CHAT-GPT in a Moodle quiz. You just need to enter <b>the code configured in the extension</b> on the keyboard and then click on the question you want to solve, and CHAT-GPT will automatically provide the answer. However, one needs to be careful because as we know, CHAT-GPT can make errors especially in calculations.

## Chrome Webstore

Find the extension on the Chrome Webstore right [here](https://chrome.google.com/webstore/detail/moodlegpt/fgiepdkoifhpcgdhbiikpgdapjdoemko)

## Summary

- [MoodleGPT 1.1.0](#moodlegpt-110)
  - [Chrome Webstore](#chrome-webstore)
  - [Summary](#summary)
  - [Disclaimer !](#disclaimer-)
  - [Donate](#donate)
  - [Update](#update)
  - [Set up](#set-up)
  - [Mode](#mode)
  - [Settings](#settings)
  - [Internal Features](#internal-features)
    - [Support table](#support-table)
  - [Supported questions type](#supported-questions-type)
    - [Select](#select)
    - [Put in order question](#put-in-order-question)
    - [Resolve equation](#resolve-equation)
    - [One response (radio button)](#one-response-radio-button)
    - [Multiples responses (checkbox)](#multiples-responses-checkbox)
    - [True or false](#true-or-false)
    - [Number](#number)
    - [Text](#text)
  - [What about if the question can't be completed ?](#what-about-if-the-question-cant-be-completed-)
  - [Test](#test)

## Disclaimer !

I hereby declare that I am not responsible for any misuse or illegal activities carried out using my program. The code is provided for educational and research purposes only, and any use of it outside of these purposes is at the user's own risk.

## Donate

Will be a pleasure if you want to support this project :)
<br/>
<a href="https://www.buymeacoffee.com/yoannchbpro" target="_blank" rel="noopener noreferrer"><img src="./assets/bmc-button.png" alt="Mortarboard icons created by itim2101 - Flaticon" width="150"></a>

## Update

See the [changelog](./CHANGELOG.md) to see every updates !

## Set up

> NOTE: This extension only works on Chromium-based browsers like Edge, Chrome, etc. Unfortunately, Firefox requires a click on the extension, which is not very discreet.

<p align="center">
<img src="./assets/setup.png" alt="Popup" width="300">
</p>

Go to <b>"Manage my extensions"</b> on your browser, then click on <b>"Load unpacked extension"</b> and select the <b>"extension"</b> folder. Afterwards, click on the extension icon and enter the ApiKey obtained from [openai api](https://platform.openai.com/api-keys). Finally, click on the <b>reload button</b> next to model (it should give you the last ChatGPT version, otherwise enter it by your self) and click on the save button (The extension need to be configured before entering the moodle quiz).

## Mode

<p align="center">
<img src="./assets/mode.png" alt="Popup" width="300">
</p>

- <b>Autocomplete:</b> The extension will complete the question for you.
- <b>Clipboard:</b> The response is copied into the clipboard.
- <b>Question to answer:</b> The question is converted to the answer and you can click on it to show back the question (or show back the answer).
  <br/><img src="./assets/question-to-answer.gif" alt="Question to Answer">

## Settings

<p align="center">
<img src="./assets/settings.png" alt="Popup" width="300">
</p>

- <b>Api key</b>: the openai api key.
- <b>Code</b>: a code to be more discret for injecting/removing the extension from the page. Simply type your code you entered into the configuration on the keyboard when you are on your moodle quiz and the extension will be inject. If you want to remove the injection just simply type back the code on your keyboard.
- <b>GPT Model</b>: the gpt model you want to use. You can click on the reload button to get the latest version of available gpt model for your account but you need to enter the api key first.
- <b>Cursor indication</b>: show a pointer cursor and a hourglass to know when the request is finished.
- <b>Title indication</b>: show some informations into the title to know for example if the code have been injected.
  <br/> ![Injected](./assets/title-injected.png)
- <b>Console logs</b>: show logs into the console for the question, chatgpt answer and which response has been chosen.
  <br/><img src="./assets/logs.png" alt="Logs" width="250">
- <b>Request timeout</b>: if the request is too long it will be abort after 20 seconds.
- <b>Typing effect</b>: create a typing effect for text. Type any text and it will be replaced by the correct one. If you want to stop it press <b>Backspace</b> key.
  <br/> ![Typing](./assets/typing.gif)
- <b>Mouseover effect</b>: you will need to hover (or click for select) the question response to complete it automaticaly.
  <br/> ![Mouseover](./assets/mouseover.gif)
  <br/> ![Mouseover2](./assets/mouseover2.gif)
- <b>Infinite try</b>: click as much as you want on the question (don't forget to reset the question).
- <b>Save history</b>: allows you to create a conversation with ChatGPT by saving the previous question with its answer. However, note that it can consume a significant number of tokens.
- <b>Include images</b> (only work with gpt-4): allows you to include the images from the question to be send to the chatgpt api. The quality is reduced to 75% to use less tokens.However, note that it can consume a significant number of tokens.
  <br/> ![Images](./assets/images.gif)

## Internal Features

### Support table

Table are formated from the question to make it more readable for CHAT-GPT. Example of formatted table output:

```
| id       | name  | birthDate  | cars |
----------------------------------------
| Person 1 | Yvick | 15/08/1999 | yes  |
| Person 2 | Yann  | 19/01/2000 | no   |
```

## Supported questions type

### Select

![Select](./assets/select.gif)

### Put in order question

![Order](./assets/order.gif)

### Resolve equation

![Equations](./assets/equations.gif)

### One response (radio button)

![Radio](./assets/radio.gif)

### Multiples responses (checkbox)

![Checkbox](./assets/checkbox.gif)

### True or false

![True-false](./assets/true-false.gif)

### Number

![Number](./assets/number.gif)

### Text

![Text](./assets/text.gif)

## What about if the question can't be completed ?

To know if the answer has been copied to the clipboard, you can look at the title of the page which will become <b>"Copied to clipboard"</b> for 3 seconds.

![Clipboard](./assets/clipboard.gif)

## Test

- <b>Solution 1</b>: Go on [this moodle test page](https://school.moodledemo.net/login/index.php) (username: `student`, password: `moodle`) and choose any quiz.
- <b>Solution 2</b>: Run the `index.html` file located in the `test/fake-moodle` folder.
