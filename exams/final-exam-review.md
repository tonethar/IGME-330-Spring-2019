# Final Exam Review

## I. When is it?
- The final written exam:
  - It will be given in class during our final regular, meeting week 14

## II. What's on it? How do I study?
- Everything that was covered for the entire semester is fair game, so be sure to review the course material from prior to the midterm --> [Midterm Exam Review](../exams/midterm-exam-review.md)
- Review questions covered since midterm exam:
  - [week-10A-notes.md#review](../weekly/week-10A-notes.md#review)
  - [week-12A-notes.md#review](../weekly/week-12A-notes.md#review)
  - [week-12B-notes.md#review](../weekly/week-12B-notes.md#review)
- Review course notes and lecture videos, they are linked in mycourses

## III. More review questions

### III-A. Text

1) Give examples of *constrained writing* techniques

2) What do the following JavaScript methods do?
  - `array.join()`
  - `string.replace()`
  - `string.split()`
  - `string.trim()`
  
3) Give an example of a regular expression *Metacharacter*

4) What are *stop words*?

5) What is a *grammar*?

6) What is the difference between a *terminal symbol* and a *non-terminal symbol*?

7) What happens when we `.expand()` a grammar?


### III-B. ES6 Classes & Modules

1) Let's suppose we have a web service that returns "pet of the day" data in a JSON format. Properties of the JSON include the `species`, `description`, and `url` of the pet:
  - create an ES6 class named `CutePet` that contains these 3 values as properties
  - the class will have a constructor to initialize these values
  - BONUS: create JS setters and getters for this class, and write validation code in the setters that guarantees that these 3 properties will always have a default value
  
  
2) Turn the following code into an ES6 module by making just the `doubleIt()` function "public" and visible from the outside of the file. `SECRET` should be "private" to the file.

```js
// this code in a file named mylib.js

const SECRET = 42;

function doubleIt(num){
  return num * 2;
}
```

### III-C. Node & npm

1) Which JavaScript *engine* does **Node.js** use?

2) Does **Node.js** run on the *client-side*, *server-side*, or *both*?

3) Why doesn't **Node.js** have a `window` object and *DOM manipulation*  methods?

4) Write the line of code that imports a package named `cowsay`

5) What does `npm` allow us to download and manage?

6) What is contained in a *package.json* file?

7) What is *transpiling*?

8) What does the **webpack** package do?


### III-D. Web Services

- Also see the other web service review questions linked above (12A)

```js
let json = {
  "statusCode": 200, 
  "results": [{"firstName": "Jimmy"},{"firstName": "Johnny"}, {"firstName": "Jilly"}]
 };
 ```

1) Write code that logs out the value of `statusCode` above

2) Write code that loops though all of the `results` above and logs out the value of all the `firstName` properties

3) What is the name of the format of the following data?

```js
dataLoaded({
  "statusCode": 200, 
  "results": [{"firstName": "Jimmy"},{"firstName": "Johnny"}, {"firstName": "Jilly"}]};
});
```

4) Give the HTTP response header than "turns on" CORS so that a web browser can access a web service directly

5) Explain what a *proxy server* does

6) Write code that will access the &lt;city> value below. Assume that this XML is a parseable DOMDocument that is stored in a variable named `doc`:

```xml
<locations>
  <place>
    <title>
      RIT
    </title>
    <location>
      <street>
        Jefferson Road
      </street>
      <city>
        Henrietta
      </city>
    </location>
  </place>
</locations>
```

7) Describe how DOM Injection (aka XSS "Cross-Site Scripting") works when downloading JSON-P web services from another domain.

### III-E. Firebase

1)  Which method of a firebase reference adds a new JSON object to that reference AND auto-assigns a new key?

2)  Which method of a firebase reference replaces a JSON object and allows the developer to assign the object’s key?

3)  Which method of a firebase reference is used to "listen" for the change in a value?



### III-F. Vue.js

- See the "ReVue" web service review questions (12B) linked above


