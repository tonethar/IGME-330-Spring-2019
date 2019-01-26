# Project 1 - Audio Visualizer - *DRAFT*

I. [Overview](#I)
  
    A. [Mission](#mission)
    B. [Resources](#resources)
    C. [Examples](#examples)
  
II. [Project Requirements](#II)
  
  A. [Functionality](#functionality)
  
  B. [Design & Interaction](#design)
  
  C. [Canvas & Experience](#canvas)
  
  D. [WebAudio & Experience](#webaudio)
  
  E. [HTML/CSS & Media](#media)
  
  F. [Code](#code)
  
  G. [Impact](#impact)
  
III. [Milestones](#III)

IV. [Documentation](#IV)

V. [Grading](#V)

VI. [Submission](#VI)

<hr><hr>

<a id="I"></a>

## I. Overview

<a id="mission"></a> 

- A) Your mission:
  - First, get a partner, and post both of your names to the discussion thread in mycourses. If you like, give your team a name. A partner is optional, you may work solo if you wish.
  - to build on the Web Audio Visualizer ICE and create a unique interactive audio visualization experience that utilizes the Web Audio and Canvas APIs:
  - This could be a great portfolio piece for you - so give it your best effort!
  - Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome
  - The assignment is graded out of 100 points. An A grade will be awarded only for meeting the requirements below, AND going sufficiently "above and beyond" the what we did in the Audio Visualizer ICE
  - You will be evaluated on:
    - the quality of the experience you create
    - the soundness of your programming
    - meeting the requirements detailed below
    - how far you went beyond what we did in class, as described below
    
<a id="resources"></a> 
    
- B) Resources:
  - [HW - Audio Visualizer - Part I](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-1.md)
  - [HW - Audio Visualizer - Part II](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2.md)
  - [HW - Audio Visualizer - Part III](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-3.md) - *there is no dropbox for this and it will not be collected. But this is where some very helpful info on adding audio effect nodes to the visualizer (which is a requirement of the final project submission) is given to you.*
  
<a id="examples"></a> 

 - C) Examples:
   - [Project 1 Showcase Video (2181)](https://video.rit.edu/Watch/Si56JxGd) - projects are shown starting at 5:00
   - Here are some examples from 2171 & 2175 (most run best in Chrome):
     - https://mcs2515.github.io/Magical_Visualizer/#
     - https://people.rit.edu/lpn4937/330/project1/audioVisualizer.html
     - https://people.rit.edu/bev4807/330/exercises/audio-visualizer-project/audio-visualizer-project.html
     - https://people.rit.edu/rep4975/330/project1/audio_visualizer.html
     - https://people.rit.edu/etn6701/330/Project%201/
     - https://people.rit.edu/pfw4498/330/projects/audioViz/wilsonAudioVizProject.html
     - https://people.rit.edu/sbm7101/330/projects/MayerWalker_AudioViz/WalkerMayer_AudioViz.html
     - https://people.rit.edu/bfc6072/330/projects/Project1_Audio_Visualizer/Audio_Visualizer.html
     - https://people.rit.edu/tjc3255/330/audio-visualizer/audio-visualizer-project.html
     - http://igm.rit.edu/~acjvks/courses/2015-fall/330/demos/p1-demo/web-audio-example.html
 
<a id="II"></a>

## II. Project Requirements

<a id="functionality"></a>

### A. Functional Requirements
1. Required Controls:
    - The &lt;audio> element and its progress indicators, and standard play, pause, scrub, and volume controls. Optionally, you are allowed to omit this element and create custom controls that give the same functionality
    - At least 3 sliders
    - At least 3 checkboxes
    - At least 1 radio button group
    - A way to choose between at least 3 distinct audio tracks
    - A "fullscreen" button
2. Be sure that the default settings of these controls results in an app that starts up in a visually pleasing state.
3. There will be no JavaScript errors or exceptions thrown by the app
4. Ideas for optional controls:
    - Mouse control (clicking or moving the mouse changes how the visualizer looks)
    - Web Cam input changes how the visualizer looks
    - The user can load their own tracks using [HTML Drag and Drop API](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API) or the [HTML `File` API](https://developer.mozilla.org/en-US/docs/Web/API/File)
    

<a id="design"></a>

### B. UI Design & Interaction
- ***Throw out the AV exercise and start over. You may NOT reuse the HTML and CSS from that exercise. Instead, build a custom layout yourself.***

1) Pleasing graphic design:
    - with a custom interface coded in HTML/CSS, by you
    - this interface does not resemble the AV homework's UI
    - it MUST utilize a CSS framework or modern web layout technology - see section D. below
2) Widgets are well labeled and follow interface conventions, for example:
    - radio buttons are for mutually exclusive options, checkboxes are for when you want to let the user choose *multiple* options --> https://delib.zendesk.com/hc/en-us/articles/203430309-Radio-button-vs-checkbox-what-s-the-difference-
3) Users should be able to figure out how to use the app with minimal instruction:
    - be sure to provide instruction and tooltips if necessary
    - setting the `title` attribute of an element gives us a tooltip - easy!
4) User errors must be handled gracefully:
    - for example, if the user forgets to type in a search term before clicking the Search button, the app should tell the user something like "Please enter a search term first"


<a id="canvas"></a>

### C. Canvas & Experience
1) Bitmap info fetched with `ctx.getImageData()` will be manipulated and displayed to the user in some way using `ctx.putImageData()` -  ideally the user will be able to control or toggle the effects on and off.
2) Audio data (frequency or waveform) must be sampled and used to draw graphics on the canvas using the following methods:
    - Lines
    - Bezier and Cubic Bezier curves (see SG-2)
    - Circles/Ovals
    - A gradient will be used in at least one fill() or stroke() operation (see SG-2)
    - Rectangles
    - Bitmapped Images (optional)
3) Use drawing context state variables where appropriate such as `.strokeStyle`, `.fillStyle`, `.lineWidth`, `.lineCap`, `.lineJoin`, `.globalAlpha` etc ...
4) Use the canvas transforms where appropriate - `ctx.translate()`, `ctx.rotate()` and `ctx.scale()`
    - "Push" and "pop" the canvas drawing state where appropriate
    - Recall that if your functions manipulate any drawing state variables, it's a good idea to `ctx.save()` the drawing state at the top of the function, and `ctx.restore()` the state at the bottom of the function

<a id="webaudio"></a>

### D. Web Audio & Experience
1) Give the user the ability to view both the frequency AND the waveform data (not necessarily simultaneously)
2) Add at least one audio node (besides the analyser), and give the user the ability to manipulate it
3) Be sure that the effect is *aesthetically pleasing* and not merely tacked on to meet requirements



<a id="media"></a>

### E. HTML/CSS & Media
1) Valid HTML5 - https://validator.w3.org
    - Use HTML5 semantic and structural elements where practical
2) Valid CSS - https://jigsaw.w3.org/css-validator/
    - Most CSS is in an external style sheet.
3) Images are properly *optimized* (both dimensions and file size) for Web delivery
4) You MUST use either a CSS framework or a modern web layout technology for the UI of this project:
  - CSS Frameworks:
    - https://bootstrap-vue.js.org
    - http://getbootstrap.com
    - http://materializecss.com
    - https://purecss.io
    - https://github.com/troxler/awesome-css-frameworks
  - Modern Layout Technology:
    - [CSS Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
    - [CSS Grid](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids)

<a id="code"></a>

### F. Code Requirements
1) You MUST use data binding and an MVC or MVVM framework such as Vue.js, React.js or Angular.js
    - Also utilize at least one custom MVVM component, created by you (don't just re-use what we did in the exercises)
2) Ajax - use jQuery.ajax(), XHR, Fetch or [Axios](https://github.com/axios/axios)
3) Use at least 1 ES6 custom class, written by you:
    - for example, if your web service was downloading and displaying state parks in a list, you could create a class called `StatePark` to model the data
4) Conventions and structure:
    - All code is an external JavaScript files
    - ES6 module pattern preferred
    - `let` and `const` must be used to declare variables
    - D.R.Y. - Don't Repeat Yourself. Repeated blocks of nearly identical code must be factored out and placed in a separate function
    - Variable and function names must begin with a lowercase letter
    - Well-commented code. Each and every function gets a comment indicating what it does
5) It is expected and required that the code in the assignment (other than from approved libraries) is written by you. If you do end up using a small amount of code you found on the web, you must document where you got it from.  Give credit and a link for all code (fragments or otherwise) that are not written you. Failing to give credit opens you to charges of **academic dishonesty**:
   - examples of acceptable use for this project:
     - copying a GUID generating function "whole cloth" from StackOverflow - https://stackoverflow.com/questions/105034/create-guid-uuid-in-javascript
     - copying and lightly modifying code for a "hamburger" menu - https://www.google.com/search?q=vanilla+javascript+hamburger+menu
   - Cite the code source **both** in the source code itself as a comment, and in your final documentation
   - Be sure to make borrowed code "your own" as much as possible for example by simplifying or improving the clarity of the code,  using `let` or `const` instead of `var`, getting rid of inline event handlers (which are prohibited in this project) and so on
   - You do not need to cite code that you received from our in-class exercises, demos or HW
   - **If you have any doubt about what is acceptable to "borrow", ask the professor *in advance* of using it**
6) **NOT allowed**:
    - DOM queries and manipulation via `document.querySelector()`, `document.querySelectorAll()`, `element.innerHTML`, `element.appendChild()` and so on. Instead, use data-binding and your MVVM framework to update the DOM
    - jQuery DOM manipulation - for example `$.html()` - is NOT allowed
    - `var`
    - inline event handlers in your HTML
    - `console.log()` calls (delete or comment them out)

<a id="impact"></a>

### G. Impact
  - Does the app work as intended and do something useful?
  - Does the app functionality and programming go beyond what we did in class?
  - Is this project "portfolio quality" that you would not hesitate to show a potential employer?
  - Be sure that the app functions as expected when posted to `banjo.rit.edu` - for example, be sure that there are not any security issues caused by using `http` instead of `https` in links to libraries and so on

<a id="III"></a>

## III. Milestones
  - Project proposal with working prototype - see myCourses for due date/time:
    - a 2 or 3 paragraph description of the project and what web services you are using should be in the comments field of the dropbox
    - the working prototype must be utilizing your MVC or MVVM framework, and have at least one of your web services functioning
    - one submission per team please. Make sure both team members' names are included.
  - Final project deliverable - see myCourses for due date/time. One submission per team please. Again, make sure both team members' names are included.

<a id="IV"></a>

## IV. Documentation
  - As with Project 2, include a file where you document your process, cite any sources, tell me where to find anything special you want me to see, and also explain how you met the requirements. Finally, give yourself a grade for the project that you feel fairly represents what its worth
  - If you worked in a team, explain what each team member did. Remember, everyone is responsible for contributing throughout the project, not just to one aspect

<a id="V"></a>

## V. Grading
  - *Both* partners must contribute *both* JavaScript code AND HTML/CSS to the project. This is NOT a project where team members are allowed to specialize into "Art Director" and "Software Developer" roles! Both team members shall be "Artist/Coders" (doing both) for this project.

Your project will be graded on the following criteria:

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **A. [Functionality](#functionality)** | **40** | |
|    1. TWO web services are used | |
|    2. Cloud storage is used | |
|    3. Last term searched stored in browser  | |
|    4. Has required Controls | |
|    5. Runs without errors | |
|    - *Missing web services* | *(-20 each)* |
|    - *Missing cloud storage or **admin.html*** | *(-10)* |
|    - **admin.html** uses DOM manipulation instead of Vue.js | *(-5)* |
|    - *Does not remember last search term* | *(-10)* |
|    - *Missing controls* | *(-10 each)* |
|    - *Errors* | *(-? depending on severity)* |
| **B. [Design & Interaction](#design)** | **20** | |
|    1. Visual design is pleasing | |
|    2. Widgets are well labeled and follow interface conventions | |
|    3. Users should be able to figure out how to use the app with minimal instruction | |
|    4. User errors must be handled gracefully | |
|    5. The *state* the application is in is obvious | |
|    6. The app should look good on a range of displays. | |
|    - *Interface looks like GIF Finder HW* | *(-15)* |
|    - *Interface "broken" at 1024x768 or higher resolutions* | *(-10)* |
| **C. [HTML/CSS/Media](#media)**  | **10** | |
|    1. Valid HTML | |
|    2. Valid CSS | |
|    3. Images properly optimized | |
| **D. [Code](#code)**  | **10** | |
|    1. MVVM Framework used | |
|    2. Ajax used | |
|    3. *ES6 Custom Class not used* | *(-5)* |
|    4. *Conventions NOT followed* | *(-5 per incident)* |
|    5. *Code that is NOT allowed* | *(-5 per incident)* |
| **E. [Impact](#impact)**  | **10** | |
|    - Does the app work as intended and do something useful? | |
|    - Does the app functionality and programming go beyond what we did in class? | |
|    - Is this project "portfolio quality" that you would not hesitate to show a potential employer? | |
| **Above and Beyond (see below)** | **10** | |
| **Possible Total Points** | **100** | |
| **Deductions** | **&darr; Don't lose points for any of these! &darr;** | |
| *Deduction if required proposal/prototype is not submitted to dropbox on time* | *(-10)* | |
| *Deduction if final documentation is not submitted to dropbox on time* | *(-10)* | |
| *Deduction if MVVM framework "created by you" component is missing* | *(-10)* | |
| *Deduction if MVVM framework is not used* | *(-30)* | |
| *Deduction if app does not function when deployed to web* | *(-15)* | |
| *Deduction if students does not attend finals week meeting to present app to either class or professor* | *(-15)* | |

Note:
- **Good** (Meet all requirements above reasonably well) = 90%
- **Better** (Go beyond expectations in 2 or more areas) = 95%
- **Best** (Go significantly beyond expectations in 2 or more areas) = 100%

<a id="VI"></a>

## VI. Submission
- ZIP and post the completed project and documentation page to to the mycourses dropbox
- Post the project to Banjo, and put the link in the mycourses dropbox comments field



