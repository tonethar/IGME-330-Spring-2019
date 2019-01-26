# Week 5A - Tuning up our Audio Visualizers

## I. Overview
Today we'll discuss some potential enhancements to our audio visualizer project - [Project 1 - Audio Visualizer](../projects/project-1.md)

## II. Review Questions <a id="review-questions"></a>

- We covered these concepts last week:

### II-A. Web Audio
1. Web Audio API *nodes* and their connections are commonly visualized as a ___________
1. True or False. An *analyser node* modifies the audio data
1. If we request 32 samples from a sound, how many elements will be present in the typed array we get back?
1. Give 3 differences between a typical JS Array created with `[]`, and a JS *typed array* such as a `Uint8Array`
1. What is an [OscillatorNode](https://developer.mozilla.org/en-US/docs/Web/API/OscillatorNode)?
1. Give 3 possible sources for a "source node"
1. What does a "destination node" typically point at?

### II-B. Bitmap Data
1. Suppose your canvas is has dimensions of 500 x 500 pixels. How many elements will be in the *typed array* you get back from `ctx.getImageData(0, 0, canvasWidth, canvasHeight)`
1. Why do we step through the image data array 4 elements at a time?
1. Describe how to implement a *brightness* filter

### II-C. Other
1. What does **IIFE** stand for?
1. What is the primary benefit of using an IIFE in your JS code?

## III. Required Reading & Assignments

**Data Viz in General:**
  - https://datavizcatalogue.com
  - https://informationisbeautiful.net/visualizations/what-makes-a-good-data-visualization/
  
**Audio Viz Specifically:**
- https://medium.com/@delu/a-perceptually-meaningful-audio-visualizer-ee72051781bc (some practical tips)
- https://www.awwwards.com/awwwards/collections/web-audio-api-and-adio-visualization/ (really nice examples!)
- https://99designs.com/blog/design-other/sound-visualization-design-inspiration/ (cool, but out there!)

<a id="effective-audio-visualizer"></a>

## IV. Presentation
- ***What makes for an effective audio visualization?***
  - there should be an analogous relationship between the sound data and what people are seeing on the screen - drawing should not be random like our "screen savers" at the beginning on the semester were. Can you instead help your viewer **learn** about sound & music by making new connections, and seeing new patterns, such as:
    - visualizing the "beat"
    - human voices fall into the lower frequencies
    - electronic instruments have a different "shape" than natural instruments
  - have a good "starting state" to your visualization - the controls should be pre-set to where the visualization has a pleasing state when the user first opens it. Here's a good example of this: https://mcs2515.github.io/Magical_Visualizer/#
  - don't bore the user - have the visualization periodically change in major ways, automatically. Here's an example: http://igm.rit.edu/~acjvks/courses/2015-fall/330/demos/p1-demo/web-audio-example.html
  - give the user controls (sliders, check boxes, pull downs) to effect the visualization. The relationship between what the controls do and what happens on the screen should be obvious
- ***Other tips for project 1***:
  - you will only get credit for code that goes beyond what was given to you in the exercises. For example, a "lines" checkbox (from Audio Viz II) was done for you and adds nothing to most visualizations.
  - the circles from Audio Viz I should not be a component of your finished version - you should be looking to create something new and unique
  - try to do something interesting for the "curves" requirement - not just a single bouncing control point - here's an example done entirely with `ctx.bezierCurveTo()`: http://igm.rit.edu/~acjvks/courses/2018-spring/330/code-examples/viz/web-audio-4B-demo/three-spirographs.html
  - the UI should follow general CRAP principles covered elsewhere
  - you MAY use a library for your UI such as **dat.gui.js**, which is a popular lightweight GUI library  -> https://workshop.chromeexperiments.com/examples/gui/#1--Basic-Usage


## V. Demo
- Today's demo, where we add multiple controllable audio effect nodes to a previous demo, is detailed here: [demo-more-web-audio.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-more-web-audio.md)


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-04B-notes.md**](week-04B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-05B-notes.md**](week-05B-notes.md)
