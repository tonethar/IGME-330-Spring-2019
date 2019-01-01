# Week 1A: Course Introduction | JavaScript Review

Welcome to the course!

## I. Overview
Welcome to IGME-330 Rich Media Web Application Development I. In this course you will be building on top of IGME-230 and constructing compelling interactive experiences that can be viewed over the web. You will also be learning about how to build more robust and modular web software by utilizing more features of JavaScript ES6, and tools like Node.js and npm. 


## II. Prerequisites
IGME-230 is a pre-requisite, and you should have a solid understanding of these topics:
- HTML/CSS, and be able to post web files to `people.rit.edu` - if you forgotten how, [here are the instructions](https://github.com/tonethar/IGME-230-Master/blob/master/notes/posting-to-banjo.md)
- Basic JavaScript and the Web Browser DOM (Document Object Model)

### \*\*Important - Before class begins\*\*
- Review the topics in these ten [IGME-230 Web App tutorials](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-0.md#section4) - most of this material should have been covered in your IGME-230 section. If you need a refresher on any of these topics, just go through the applicable tutorials at the link above. If you have any questions at all, or would like to have an assignment checked for accuracy, go ahead and reach out to me via email.


## III. Course Description & Topics
Official description from SIS: *This course provides students the opportunity to explore the design and development of Media Rich Internet Applications (MRIAs).  This course moves beyond client and server side web development, and explores issues of presentation, interactivity, persistence, and extensibility common among such applications.  Specifically, items explored include framework characteristics, data management, persistence, data binding, information manipulation, as well as data presentation.*


## IV. Pedagogy (how this course is taught!)
- ***You need to review the week's lecture notes *prior* to attending class for that week***
- A typical classroom day will be:
    - a review of the days topics our Github lecture notes
    - a live demo by the professor that reinforces the day's topics
    - if time remains, students will be able to work on homework assignments
- The assignments given in this class break into two categories:
    - homework assignments or in-class exercises that focus narrowly on one or more concepts
    - three projects with more flexible requirements that allow you to exercise considerable freedom and creativity in demonstrating key skills and understanding
- A large part of this course is taught similar to a typical math course: there will be several small homework assignments given every week, and because these assignments build upon one another, it is essential that they be completed both on-time and in-order, thus they have strict due dates.
- Keep an eye on the dropboxes in myCourses for what and when things are due. HW assignments will not be accepted late without prior permission from the instructor:
    - if something comes up and you need an extension you need to get in touch with us ASAP *before* the assignment is due
    - **Reminder:** *all code files (HTML, CSS, JavaScript) must be zipped when put in a dropbox, because otherwise myCourses strips out the JavaScript and CSS, and you will likely get a zero on the assignment*
- The due dates for these assignments will be clustered around the same days, often on Sunday night. This means that you should plan ahead, and not try to tackle them all in the last hour before they are due.
- Please get to class on time! Lectures will begin promptly at the start of class.

## V. Required Reading & Assignments
* [syllabus.md](../syllabus.md)
* [schedule.md](../schedule.md)
* Course topics -> [topics.md](../topics.md)
* [Project 1 Web Audio Visualizer](../projects/project-1.md) - this is what we are working towards for the first 1/3 of the course
* [Project 1 Showcase (20:14)](https://video.rit.edu/Watch/Si56JxGd)
* Check the *Content* section of mycourses.rit.edu for "done" in-class demo files
* Check the mycourses.rit.edu dropboxes to see what is assigned and when it is due

## VI. Presentation
- [Course Overview (PDF)](https://github.com/tonethar/IGME-330-Master/blob/master/presentations/Course-Overview.pdf)

## VII. Today's topic - JavaScript/DOM Review & Demo <a id="review-questions"></a>

- 1. What is JavaScript?
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript
  - Used on both the client-side and server-side to create interactive web applications
  - Weakly typed:
    - after they are declared, variables can contain any type
    - JS uses *dynamic typing* to verify the type safety of a program at runtime, as opposed to compile time (static) typing
  - Multi-Paradigm:
    - *imperative* - a series of commands that describe how the program behaves (as opposed to *declarative* languages such as CSS or SQL)
    - *functional* - use functions to compose a program, avoid globals & mutable state
    - *event-driven* - program flow is driven by user and system events
    - *object-based* - an object literal, many built-in objects to use, and both prototypical and classical inheritance when the developer creates their own objects
    - *duck typed* - an object's suitability to be used for particular purpose is determined by the presence of certain methods and properties, rather than the type of the object itself
- 2. Setting up the development environment - easy!
  - A text editor
  - Chrome
  - create a web page, then run JavaScript in the console or type code into the &lt;script> tag
  - the console is an interactive **REPL** - "Read, Evaluate, Print, Loop"
    - shift-enter for multi-line code
    - up arrow to repeat last typed line
- 3. JavaScript Review & Demo
  - declaring variables with `var`, `let`, and `const`
  - operators
  - common types
  - `Boolean`, `Number`, `String`, `Symbol` (new for ES6), `Null`, `Undefined`, and `Object`
  - Functions are also Objects and thus “first class” values, and can be both passed to functions and returned from them
  - `console.log()`
  - Standard built-in objects - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects
    - `Date`
    - `Math`
    - `Array`
  - Putting JavaScript in a <script> tag
    - `"use strict";` (strict mode) - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
  - Functions
    - writing functions
    - calling functions
    - Some DOM Elements (DOM = Document Object Model)
      - https://en.wikipedia.org/wiki/Document_Object_Model
      - https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model
    - Add &lt;button>, &lt;input>, and &lt;p>
    - Manipulating the properties of DOM elements:
      - `document.querySelector()`
      - `document.querySelectorAll()`
    - Challenge:
      - Add a "last name" input so that we can greet the person using both their first and last name
      - *Declaratively* (using CSS) make the button 50 pixels tall by 100 pixels wide
      - *Imperatively* (using JavaScript) give the paragraph a red text color, and a yellow background color
    - Events:
      - DOM elements have to load before we can manipulate their properties
      - event handlers - the `onclick` attribute
      - `element.addEventListener()`
- 4. JavaScript Debugger:
  - setting breakpoints
  - inspecting variable values 
  - viewing the call stack
  - "View Page Source" v. the Debugger's "Inspect Elements" view

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
|   :-\  |  [**IGME-330 Schedule**](../schedule.md) | [**week-01B-notes.md**](week-01B-notes.md)
