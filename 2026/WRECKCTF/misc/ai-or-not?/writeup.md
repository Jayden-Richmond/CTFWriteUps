# ai-or-not? Writeup

**CTF EVENT:** WRECKCTF 2026
<br>**Category:** Misc
<br>**Points:** 174pts

## :spiral_notepad: Challenge Desciption
> Our research team just deployed ARIA — our most advanced AI assistant yet. Third generation, fully trained, supposedly impenetrable.
> <br> I also can't quite remember where I wrote down the override token...

## Background Information
When starting the challenge I was presented with a link to a website called ARIA. ARIA was presented as an intelligent chatbot with adapative reasoning. Going into this challenge my assumption was to find an override token that could modify ARIAs behavior to give me a flag. As is the case with any web challenge the first step should always be to inspect the websites behavior.
<img width="2246" height="1335" alt="image" src="https://github.com/user-attachments/assets/e289de0a-019c-49bd-8512-cdc0a74dfa87" />

## Reconnaissance
After looking at the behavior of ARIA and feeding a multitude of inputs I realized I was getting premade static phrases instead of more creative responses from an LLM. This mean I could not do anything to convince ARIA to give me the flag or override token. After understanding this concept I moved onto inspect the javascript index for the webstie. 

While inspecting the page source of the index, I found a deployment checklist hidden in the HTML comments. This leaked some highly sensitive internal deployment information:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ARIA — AI Assistant</title>
  <style>
```
jff


