# Week 1B - Introduction to Canvas

## I. Overview
Canvas is a 2D bitmap drawing API that allows the developer to write code that draws shapes and images into a browser window without the need for a plug-in like Flash or Java. 

## II. Required Reading & Assignments
* "Hello Canvas" HW -> [HW-hello-canvas.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-hello-canvas.md)
* Study Guide-1 -> [HW-SG-1.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-1.md)

## III. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial

### III-A. The canvas specification
*When in doubt, read the spec!*
- https://www.w3.org/TR/2dcontext/
- https://html.spec.whatwg.org/multipage/canvas.html#2dcontext

## IV. Presentation
- [Intro-to-Canvas.pdf](https://github.com/tonethar/IGME-330-Master/blob/master/presentations/Intro-to-Canvas.pdf)

## V. Today's Topic - *Intro to the Canvas 2D Drawing API*
- start file for today's demo is here -> [first-canvas.md](_files/first-canvas.md)
- Concepts covered:
  - Getting a reference to the 2D drawing context with `canvas.getContext('2d')`
  - setting context "state" attributes like `.fillStyle`, `.strokeStyle`, `.lineWidth` and `.globalAlpha`
  - drawing rectangles, circles and lines
  - creating paths, and stroking and filling them
  - setting up an animation loop
- and here are some handy helper functions we will be using today, they are provided below for your copy and paste pleasure:

```js
function getRandomColor(){
  function getByte(){
    return 55 + Math.round(Math.random() * 200);
  }
  return "rgba(" + getByte() + "," + getByte() + "," + getByte() + ",.8)";
}

function getRandomInt(min, max) {
  return Math.round(Math.random() * (max - min)) + min;
}
```
- and if we have time, we might re-factor `getRandomColor()` into something a little more "ES6ish" - for example:
  - replace `getByte()` with an [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
  - replace the string concatenation in the return statement above with [string template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01A-notes.md**](week-01A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-02A-notes.md**](week-02A-notes.md)
