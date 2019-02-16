# Week 6B - ES5/ES6 "Sprites" & Delegation

## Overview
- Sprites (using either Object literals, or ES6 classes) are an optional component of Project 1, and whether you use them or not on your project, understanding how the JavaScript runtime engines represent classes and objects is important for developers


## II. Lecture Notes
- [1 - Intro to Canvas Sprites](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-1.md)
  - First we try to build a sprite object using script-scoped variables such as `x`, `y`, `radius`, `color`  - BAD!
  - then we group these variables into an object literal - BETTER!
  - lastly we create a factory function to produce multiple object literals - BEST!
  - take a look in the web inspector to see these objects and the default *prototype chains* created via the `__proto__` - i.e. "dunder proto" property - http://2ality.com/2012/10/dunder.html - we will discuss  *prototype* chains soon
  - isn't this inefficient, storing multiple copies of all of these properties and methods?
    - In a class-based environment, each instance of a class would have their own copies of instance variables (like `x` and `y`), but share all of the methods (like `move()`, `reflectX()`, and `reflectY()`)
    - interestingly, all major JavaScript engines already perform this optimization on object literals, and basically generate a "super class/super object" for you. The concept is called *shapes*, and you can read about it here: https://mathiasbynens.be/notes/shapes-ics
    -  No matter how many objects there are, as long as they have the same *shape*, they only have to store the shape and property information once. All JavaScript engines use shapes as an optimization, but they don't all call them shapes:
        - Academic papers call them *Hidden Classes* (confusing w.r.t. JavaScript classes)
        - [V8](https://github.com/v8/v8) calls them *Maps* (confusing w.r.t. JavaScript Maps)
        - [Chakra](https://github.com/Microsoft/ChakraCore) calls them *Types* (confusing w.r.t. JavaScript’s dynamic types and typeof)
        - [JavaScriptCore](https://trac.webkit.org/wiki/JavaScriptCore) calls them *Structures*
        - [SpiderMonkey](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey) calls them *Shapes*
        
- [2 - Object.create() & Delegation](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-2.md)
  - In JavaScript, how can we benefit from the concept of `inheritance` without using classes - answer: the JavaScript *prototype chain*:
    - this is called *prototype-based inheritance*
    - "own" properties and properties 
    - *property shadowing* is basically like "overriding" in class-based languages
  - `Object.create()`
  - Delegation & OLOO - "Objects Linked to Other Objects"
  
- [3 - Canvas & ES6 Classes](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-3.md)
  - JavaScript classes = "syntactical sugar"!
    - but sugar tastes so good!
    - even with classes, behind the scenes, the JS engine is still using the *prototype chain*
    - POLL: do you prefer ES5 delegation, or ES6 classes?
    

## III. Demo/Challenge in Time Remaining

- The [revealing module pattern example](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-revealing-module-pattern.md) we worked with created sprite objects by utilizing ES5 object literals and a factory function
- Your mission: take either the start or end version of the code (it doesn't matter which) and modify the `createSprites()` function to utilize ES6 class syntax

## IV. Videos of lecture & demos

We aren't always going to have video links, but here is a re-cap of today's major topics:

- [Objects Part I  - Literals Factory Functions(14:40)](https://video.rit.edu/Watch/Jc7k9LPx)
- [Objects Part II - ES5 Delegation - (16:03)](https://video.rit.edu/Watch/Eb67XqZd)
- [Objects Part III - ES6 Classes - (13:59)](https://video.rit.edu/Watch/m9KRj43F)



<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-06A-notes.md**](week-06A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-07A-notes.md**](week-07A-notes.md)
