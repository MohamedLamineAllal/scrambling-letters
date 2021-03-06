
[![npm](https://img.shields.io/npm/dt/scrambling-letters.svg)]()
[![npm](https://img.shields.io/npm/v/scrambling-letters.svg)]()
[![license](https://img.shields.io/github/license/recidvst/scrambling-letters.svg)]()

# Scrambling Letters
A lightweight javascript library for scrambling letters within a piece of text, giving a nice decoding effect.

Loops through any elements with the relevant selector or data attribute and scrambles the letters randomly for a couple of seconds before returning them one by one to their original state.

[Demo Page](https://recidvst.github.io/scrambling-letters 'Scrambling Letters demo')

[Codepen initial POC](https://codepen.io/Recidvst/pen/ZrjmJj "Scrambling Letters Codepen")


To-do:
- Test suite.
- Better handling of nested tags?


## Get Scrambling Letters

### Download
- Download the Scrambling Letters dist files from [Github](https://github.com/Recidvst/scrambling-letters/archive/master.zip 'Github download') or from [NPM](https://www.npmjs.com/package/scrambling-letters 'npm download') or [Yarn](https://yarnpkg.com/en/package/scrambling-letters 'yarn download').
- Pick the dist file you desire - ES6, ES5 or babel polyfilled. The standard ES6 version will not support IE.
- Include the minified js file in the manner of your choice. This will allow you to access the new Scrambler() function.

### Initiate
- Scrambler() needs to be told which piece of text to scramble.
- Initiate a Scrambler instance by calling Scrambler() with a valid selector or data-attribute. 
- If you wish to add configuration, pass Scrambler an object containing config options (see below).

### Configure
You can configure your Scrambler instance by passing an object. The available options are as follows:

#### Target
**Purpose:** This is the text you wish to Scramble! Pass a selector or data attribute (or anything else valid for document.querySelectorAll).    
**Type:** string  
**Default:** '[data-scrambler]'  
**Required:** Yes.  
#### Random
**Purpose:** This controls the randomised time before each letter returns to its original state. The first value is the minimum delay and the second value is the maximum. E.g. changing [1000, 3000] to [1000, 6000] would increase the maximum time.  
**Type:** array  
**Default:** [1000, 3000]  
**Required:** No.   
#### Speed
**Purpose:** This controls the speed a which the letters will change. I would advise leaving it at the default 100, but you can tweak this value if you desire.  
**Type:** integer  
**Default:** 100  
**Required:** No.  

#### Warning:
- Scrambler will temporarily lose unique styling from text within child nodes e.g. link tags within a paragraph. This will be replaced at the end of the cycle but can result in FOUC. This is planned to be addressed later, but best practice is to be more granular in your targeting.
