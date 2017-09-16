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

## Tool 1 : Quokka

> Live Scratchpad for JavaScript

----

### Install

1. head over to [https://quokkajs.com/](https://quokkajs.com/)
2. click the icon matching your editor
3. click the big green "Install in &lt;_your editor_&gt;" button
4. install the downloaded package
5. when asked, yes, you do want the pro version options

----

### Quokka Commands

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
5. also explore the following:
```
//?.
```

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

### Set-up Project's Test Environment

1. `⌘-N` (create a new generic file)
2. add the following:
```
module.exports = function(wallaby) {
     return {
       files: ['./src/*.js', '!./src/*.test.js'],

       tests: ['./src/*.test.js'],

       testFramework: 'tape',

       env: {
         type: 'node'
       },
     }
}
```
3. `⌘-S` , save it as `wallyby.js`

----

### Wallaby Commands

- via Sequential keyboard shortcut commands _or_ the "Command Palette"
- `⌘-T` , `R` : Run tests
- `⌘-T` , `S` : Stop tests
- `⌘-T` , `T` : Toggle test panel

Note: In most editors, you can change these keyboard shortcuts ([Atom example](https://github.com/wallabyjs/quokka/issues/91#issuecomment-328700694))


----

### Start Testing

- `⌘-K` , `O` : Toggle Quokka panel
- `⌘-T` , `T` : Toggle test panel
- `⌘-T` , `R` : Run tests

- Note both the:
  - 'tape node module is not found...' prompt in the test panel!
    (Do _not_ install it 😉)
  - the red Utah~ish shaped Wallaby logo in the lower-right

----

### Prepare the test track!

1. `⌘-K` , `J` (create a new Quokka JS file)
2. `⌘-S` , save it as `src/reverse-str.test.js`
3. add the require statement for `tape`  
```
const test = require('tape')
```
4. Note the first two lines in the Quokka panel!


----

### Finish prepping the track!

1. Install the "tape" package into the project  
   (may need to restart the Wallaby tests)
2. Add the first basic test.  
   Your reverse-str.test.js file should look something like:  
  ```
  const test = require('tape');

  test('reverse a string', t => {
    t.plan(1) // EITHER - set async count

    t.equals(reverseStr('abcde'), 'edcba')

    t.end()  // OR - set end
  })
  ```
3. Fix the first error message

----

### Start your engines!

1. `⌘-K` , `J` (create a new Quokka JS file)
2. `⌘-S` , save it as `src/reverse-str.js`
3. write a call to the non-existent `reverseStr` function, followed by `//?`  
```
reverseStr('stressed') /*?*/
```
4. build out the `reverseStr` function, watching Quokka and Wallaby outputs

----

### Off to the races!

- replace  
  ```
  reverseStr('stressed') /*?*/
  ```
- with  
  ```
  const reverseStr = s =>
    s
      .split('') /*?*/
      .reverse()
      .join('')

  const stressed = reverseStr('stressed') /* ?
   $.toUpperCase()
     .split('') */

  const desserts = reverseStr('desserts') // ?.

  stressed

  module.exports = { reverseStr }
  ```
- review results & experiment a little or a lot 😉

---

## tangent : IDE tweaking


Atom-specific (_sorry VS Coders_😔 )

----

### Atom's customizable stylesheet

```css
/******************************************************************************

                   _    _            _                  _ _       _           
                  | |  | |          | |                | | |     | |          
  __ _ _   _  ___ | | _| | ____ _   | |  __      ____ _| | | __ _| |__  _   _
 / _` | | | |/ _ \| |/ | |/ / _` |  | |  \ \ /\ / / _` | | |/ _` | '_ \| | | |
| (_| | |_| | (_) |   <|   | (_| |  | |   \ V  V | (_| | | | (_| | |_) | |_| |
 \__, |\__,_|\___/|_|\_|_|\_\__,_|  | |    \_/\_/ \__,_|_|_|\__,_|_.__/ \__, |
    | |                             | |                                  __/ |
    |_|                             |_|                                 |___/

*******************************************************************************/

/*
    QUOKKA INLINE
*/

/* other colors for use with quokka inline
   - #3f1c1c - reddish
   - #3f1c3f - purplish
   - #3f3f1c - monkey pukish
*/

.qlc .syntax--comment,
.qlc .syntax--comment + .invisible-character.eol,
.atom-text-editor .line.qlc::after,
atom-text-editor .line.qlc::after,
.atom-text-editor .line.qle::after,
atom-text-editor .line.qle::after {
  font-weight: bold;
  border-top: thin solid #9d9da5;
  border-bottom: thin solid #9d9da5;
}

/* ANY comment on the same line as Quokka inline results */
.qlc .syntax--comment {
  padding-left: 0.25ex;
  color: hsl(240, 4%, 92%);
}

/* The invisible eol for any line with Quokka inline results */
.qlc .syntax--comment + .invisible-character.eol {
  background-color: #9d9da5;
  color: #9d9da5;
}

/* actual Quokka inline result */
.atom-text-editor .line.qlc::after,
atom-text-editor .line.qlc::after {
  padding-right: 1ex;
  background-color: #9d9da5;
  color: #0f4c19;
}

.atom-text-editor .line.qle::after,
atom-text-editor .line.qle::after {
  background-color: #9d9da5;
  color: #631913;
}

/*
    QUOKKA & WALLABY PANELS
*/
.quokka-results-view,
.wallaby-tests-view {
  font-size: 115%;
}
```

----

### Atom's customizable keymap

```cson
'.platform-darwin atom-text-editor':
  'cmd-k e': 'quokka:make-quokka-from-existing-file'
```

1. `⌘-.` - Toggle keybinding-resolver
2. type the _current_ command you are replacing
3. click the command in the keybinding-resolver panel
4. copy the commands you want to modify to _your customized_ `keymap.cson`
5. don't forget to toggle the keybinding-resolver off again


---

## Tool 3 : VerbalExpression

> Regular Expressions made easy

----

### Let's just have some fun

1. `⌘-K` , `J` (create a new Quokka JS file)
2. `⌘-S` , save it as `src/reg-exp.js`
3. grab an [example from VerbalExpression's GitHub repo](https://github.com/VerbalExpressions/JSVerbalExpressions#examples)
4. make it our own...

----

### Our example - take 1  

```
// the verbalExpressions module
const VerEx = require('verbal-expressions');

// Create an example of how to test for correctly formed URLs
const tester = VerEx()
    .startOfLine()
    .then('http')
    .maybe('s')
    .then('://')
    .maybe('www.')
    .anythingBut(' ')
    .endOfLine();

// Create a function that uses the RegExp object's native test() function
const test = input => (tester.test(input) ? 'valid' : 'invalid')

// Try it on several urls
test('https://www.google.com') //?
test('ww.google.com') //?

// Output the actual expression used: /^(http)(s)?(\:\/\/)(www\.)?([^\ ]*)$/
console.log(tester.toRegExp())
```


----

### Our example - take 2  

```
// the verbalExpressions module
const VerEx = require('verbal-expressions')

// Create an example of how to test for correctly formed URLs
const verEx = VerEx()
  .startOfLine()
  .then('http')
  .maybe('s')
  .then('://')
  .maybe('www.')
  .anythingBut(' ')
  .endOfLine()

// If invalid, we want an honest-to-goodness Error, so hit MDN
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error#Custom_Error_Types
// Create a new object, that prototypically inherits from the Error constructor
function urlError(message) {
  this.name = 'urlError'
  this.message = message || 'invalid url'
  this.stack = new Error().stack
}
urlError.prototype = Object.create(Error.prototype)
urlError.prototype.constructor = urlError

// Create a function that uses the RegExp object's native test() function
const test = input => {
  if (verEx.test(input)) return 'valid'
  else throw new urlError()
}

// Try it on several urls
test('https://www.google.com') //?
test('ww.google.com') //?

// Output the actual expression used: /^(http)(s)?(\:\/\/)(www\.)?([^\ ]*)$/
console.log(verEx.toRegExp())
```
