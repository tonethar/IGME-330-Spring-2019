# Variables and scope and functions and objects *Review*

I. Declaring variables with `var`

II. Declaring variables with `let` & `const`

III. Immutabilty

IV. Writing JavaScript Functions

V. Object Literals

VI. Classes


## I. Variable Scope

### Declaring variables with `var`

- "The scope of a variable declared with `var` is its current execution context, which is either the enclosing function or, for variables declared outside any function, global. If you re-declare a JavaScript variable, it will not lose its value." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var
- PS: When a function is declared, it also 

### Declaring variables with `let` & `const`

- "`let` allows you to declare variables that are limited in scope to the block, statement, or expression on which it is used. This is unlike the var keyword, which defines a variable globally, or locally to an entire function regardless of block scope." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let
- P.S. `const` has the same rules of scope as `let`
- P.P.S. If `let` is used to declare a variable *outside* of a function, method, or class, it ends up in what is called *script scope*, which is a "global-like" scope where it will be visible in other JavaScript files


### Questions on Variable Scope

1. What is the scope of the variable `myNum` below?

```js
<script>
	function init(){
		if(true){
		  var myNum = 0;
		  console.log(myNum);
		}
	}
</script>
```

A) block

B) function/local

C) global

D) property

E) script

<hr>

2. What is the scope of variable `myNum` below?

```js
<script>
	var myNum = 0;

	function init(){
		console.log(myNum);
	}
</script>
```


A) block

B) function/local

C) global

D) property

E) script


<hr>

3. What is the scope of variable `myNum` below?

```js
<script>
	let myNum = 0;

	function init(){
		console.log(myNum);
	}
</script>
```


A) block

B) function/local

C) global

D) property

E) script




4. What is the scope of variable `myNum` below?

```js
<script>
	const myNum = 0;

	function init(){
		console.log(myNum);
	}
</script>
```

A) block

B) function/local

C) global

D) property

E) script


<hr>


5. What is the scope of variable `myNum` below?

```js
<script>
	function init(){
		if(true){
			for(var i=0;i<5;i++){
				let myNum = 0;
			}
		}
	}
</script>
```

A) block

B) function/local

C) global

D) property

E) script


<hr>


6. What is the scope of the `init` function below?

```js
<script>
	function init(){
		console.log("Hi there!");
	}
</script>
```

A) block

B) function/local

C) global

D) property

E) script





## II. Immutability

1. What will be logged when this code runs?

```js
const x = {};
x.name = "fred";
console.log(x.name);
```

	A) A blank line

	B) “fred”

	C) undefined

	D) This code will produce an error before the console.log() executes

<hr>


2. What will be logged when this code runs?

```js
const y = 1;
y++;
console.log(y);
```

	A) 1

	B) 2

	C) undefined

	D) This code will produce an error before the console.log() executes
