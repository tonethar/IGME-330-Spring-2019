# Week 9A - Review Exam & Computational Text Libraries

<a id="review"></a>
## I. Review Exam, and touch on major concepts
  - canvas API, paths, drawing state properties, drawing state stack
  - manipulating bitmaps for pixel effects
  - web audio routing graph, effect node, destination node, analyzer node, oscillator node
  - JS typed arrays (we used these with both image data and audio data)
  - DOM: did the page load? Event handlers and function *references*
  - Other JavaScript concepts:
    - writing ES5 function declarations and ES6 arrow functions
    - Modular code: 
      - use a single IIFE to create scope
      - use multiple IIFEs to create modular code and "public/private" - the *ES5 Revealing Module Pattern*
    - value types v. reference types:
      - immutability of these with *const*
      - changing properties of reference types (see extra credit questions)
    - variable scope (outside of modules):
      - outside of another function, `function` declarations are **global**, otherwise the function is scoped to the enclosing function
      - `var` is **global** if declared outside of a function, otherwise the variable is scoped to the enclosing function (the Chrome debugger calls this scope **local**)
      - `let` is **script** scoped if declared outside of a function, otherwise the variable is scoped to the enclosing **block**
      - `const` scoping is the same as `let`
  - Objects: literals, methods, classes
  
## II. New Stuff needed for Project 2

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-08B-notes.md**](week-08B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-09B-notes.md**](week-09B-notes.md)
