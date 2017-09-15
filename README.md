---
title: Tools for Junior Devs (2017 Sep)
theme: sky
highlight-theme: dracula
revealOptions:
    transition: 'fade'
---

## Tools for Junior Devs

- for SLC JS Learners/SLC Free Code Camp
- at September 2017 meeting
- by metasean

----

### Presentation

The presentation and this repo use [reveal-md](http://webpro.github.io/reveal-md/).  

To view the presentation:
- ensure you've run
```
git clone git@github.com:SLC-JS-Learners/2017-09-tools-for-jrs.git
npm install
```
- then simply run
```
reveal-md README.md
```


---

### Prereq 1 : Supported Editors
- Atom - https://atom.io/
- VS Code - https://code.visualstudio.com/
- Jet Brains - https://www.jetbrains.com/


----

### Prereq 2 : Slack Group

- Ensure you're a member of the JS Learners group  
  join at: **https://jslearners-slack.herokuapp.com/**
- Ensure you're subscribed to: **`#current-presentation`**

----

### Prereq 3 : Alias node_modules

> **_OPTIONAL Prereq_**

1. open your `.bash_profile` in your editor of choice, e.g.  
  - `atom ~./bash_profile` for Atom
  - `code ~./bash_profile` for VS Code
2. add the following, including comment 😉  
```
## npm use local package bin
## (won't need to install most npm modules with `-g`)
export PATH=${PATH}:node_modules/.bin
```
3. save and close the file
4. completely quit and restart all terminal/command line applications, including Atom and VS Code

---

### Tool 1 : Quokka

> Live Scratchpad for JavaScript

----

### Install

1. head over to [https://quokkajs.com/](https://quokkajs.com/)
2. click the icon matching your editor
3. click the big green "Install in &lt;_your editor_&gt;" button
4. install the downloaded package
5. when asked, yes, you do want the pro version options

----

### Commands

- via Sequential keyboard shortcut commands _or_ the "Command Palette"
- `⌘-K` , `J` : Create a new Quokka JavaScript file
- `⌘-K` , `Q` : Make current file a Quokka file
- `⌘-K` , `O` : Toggle output


----

### Let's Start This Party!

1. `⌘-K` , `J`
2. `⌘-S` , save as `src/fizz-buzz.js`
3. write a call to the non-existent `fizzBuzz` function, followed by `//?`  
```
fizzBuzz(30) //?
```

----

### What The Output?!?

4. note the output next to the comment  
   and in the panel below  
   (yours _will_ look different -  
    I've already customized mine)

----

### Let's Keep the Party Rockin'!

- write an implementation of `fizzBuzz`
- note the 2 quokka outputs changing as you write your implementation

---

## Tool 2 : Wallaby

> Integrated Continuous Testing Tool for JavaScript

----

## [Officially supported frameworks](https://wallabyjs.com/docs/integration/overview.html#supported-testing-frameworks)
- jasmine
- mocha
- qunit
- jest
- ava


----

### Install

1. head over to [https://wallabyjs.com/](https://wallabyjs.com/)
2. click the big green "Install" button
3. click the big green "Download" button for your editor
4. install the downloaded package
5. copy the key metasean posted in the **`#current-presentation`** channel

----

### Set-up Test Environment

1. install the "tape" testing module  
```
npm install --save-dev tape
```


----

### Commands

- via Sequential keyboard shortcut commands _or_ the "Command Palette"
- `⌘-T` , `R` : Run tests
- `⌘-T` , `S` : Stop tests
- `⌘-T` , `T` : Toggle test panel


----

### Off to the races!

1. `⌘-K` , `J` (create a new Quokka JS file)
2. `⌘-S` , save it as `src/reverse-str.js`
3. `⌘-N` (create just a normal new file)
4. `⌘-S` , save it as `src/reverse-str.test.js`
3. write a call to the non-existent `reverseStr` function, followed by `//?`  
```
reverseStr(30) //?
```

----

### What The Output?!?

4. note the output next to the comment  
   and in the panel below  
   (yours _will_ look different -  
    I've already customized mine)

----

### Let's Keep the Party Rockin'!

- write an implementation of `fizzBuzz`
- note the 2 quokka outputs changing as you write your implementation

---

Tool 3: VerbalExpression
