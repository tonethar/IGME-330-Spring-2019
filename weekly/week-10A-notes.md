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





<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-09B-notes.md**](week-09B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-10B-notes.md**](week-10B-notes.md)
