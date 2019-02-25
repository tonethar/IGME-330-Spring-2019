# Week 10A

## I. Review Questions (in ES6 & strict mode) <a id="review"></a>

### A - ES6 Classes
1. Write a ES6 class named `Car`:
    - it will have `year` and `speed` properties
    - it will have a `.speedUp()` method that increases the car speed by 1
    - it will have a constructor that takes `year` and `speed` parameters
  
2. Is adding properties and methods to an object created with an ES6 class *legal*?

```js
let car1 = new Car('2019',0);
car1.stop = function(){
  this.speed = 0;
}
car1.stop();
```

3. Is this legal in JavaScript?

```js
const car1 = new Car('2019',0); // constant 
car1 = new Car('2019',0); // this car instance has same values as first car
```

4. Which of the following are legal in JavaScript?

```js
var car1 = new Car('2019',0);
var car1 = new Car('2019',0);

let car2 = new Car('2019',0);
let car2 = new Car('2019',0);

const car3 = new Car('2019',0);
const car3 = new Car('2019',0);
```

5. Is this legal in JavaScript?

```js
const car1 = new Car('2019',0); // constant 
car1.speed = 0;
```
6. What does **OLOO** stand for, and what method is used to implement this concept?

7. Describe *prototypical inheritance* & the *prototype chain*


### B - ES6 Modules

1. Should you be adding `'use strict";` to the top of your ES6 modules?
2. At the "top level" of an ES6 module (i.e. outside of a function or class definition), what is the *scope* of variables/functions/objects declared with:
    - `var`
    - `let`
    - `const`
    - `function`
    - `class`
3. How do we declare *script scoped* variables from an ES6 module?
4. How do we declare *globally scoped* variables from an ES6 module?

### C - JS Compiler *Shapes*

1. Give a 1 sentence description of what a *shape* is.


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-09B-notes.md**](week-09B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-10B-notes.md**](week-10B-notes.md)
