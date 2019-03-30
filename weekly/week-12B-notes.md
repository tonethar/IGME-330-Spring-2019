# Week 12B - More Vue.js

## I. Topics
- [Vue Part II - Ajax and Vue.js](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-2.md)
- [Vue Part III - Simple Vue Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-3.md)
- [Vue Part IV - Nested Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-4.md)

## II. Videos

- [More Vue.js - Part I - Vue & Ajax - (26:29)])https://video.rit.edu/Watch/Ao8n6ZFf)
- [More Vue.js - Part II - Simple Vue Components - (15:17)](https://video.rit.edu/Watch/Jo2k6XDz)
- More Vue.js - Part III - Nested Vue Components - There's not a video! You can just read the "Vue Nested Components" notes yourself: https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-4.md

<a id="review"></a>

## III. ReVue Questions (get it?)
1. What is ***Reactive Programming*** ?
1. In a ***MVVM*** Vue.js app - what is role of the:
    - Model
    - View
    - ViewModel
1. Using Vue's "handlebar" syntax, create a 1-way binding between a paragraph and a Vue.js `data` property named `title`
1. Now do the same thing instead using a Vue.js *directive*
1. Using a Vue.js *directive*, create a 2-way binding between an &lt;input> field and a Vue.js `data` property named `score`
1. Suppose you have a Vue.js `app.method` named `doStuff` and a button with an id of `btn`. Write code that calls `doStuff()` when the button is clicked on:
    - do this ***imperatively*** utilizing DOM methods such as `document.querySelector()` as well as DOM event handlers
    - do this ***declaratively*** utilizing a Vue *directive*
1. Utilizing Vue *directive(s)* and HTML, write the markup necessary to display an unordered list named `favorites`
1. Are Vue.js "handlebars" and directives visible in browsers when we "View Source"?
1. Are Vue.js "handlebars" and directives visible in browsers when we "Inspect" a page for a live view of the DOM? 

## III. Reference
- **Reactive Programming** - I like the definition from [here](https://dl.acm.org/citation.cfm?id=2501666) - "Reactive programming has recently gained popularity as a paradigm that is well-suited for developing event-driven and interactive applications. It facilitates the development of such applications by providing abstractions to express time-varying values and automatically managing dependencies between such values."
- **MVVM ("Model–view–viewmodel")** - https://en.wikipedia.org/wiki/Model-view-viewmodel - the ViewModel of MVVM is a value converter, meaning the view model is responsible for exposing (converting) the data objects from the model in such a way that objects are easily managed and presented. ViewModel handles data binding, ensuring that the data changed in the Model immediately affects the View layer and vice versa. 
- **MVC v. MVVM** - https://stackoverflow.com/questions/667781/what-is-the-difference-between-mvc-and-mvvm
<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-12A-notes.md**](week-12A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-13A-notes.md**](week-13A-notes.md)
