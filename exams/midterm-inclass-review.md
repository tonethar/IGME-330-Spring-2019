# Variables and scope and functions and objects *Review*

I. Declaring variables with `var`, `let` & `const`

II. Immutabilty

III. Writing JavaScript Functions

IV. Object Literals

V. Classes


## I. Variable Scope

### I-A. Declaring variables with `var`

- "The scope of a variable declared with `var` is its current execution context, which is either the enclosing function or, for variables declared outside any function, global. If you re-declare a JavaScript variable, it will not lose its value." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var
- PS: When a function is declared, it follows the same scope rules
- "Because variable declarations (and declarations in general) are processed before any code is executed, declaring a variable *anywhere* in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it's declared. This behavior is called "hoisting", as it appears that the variable declaration is moved to the top of the function or global code."

### I-B. Declaring variables with `let` & `const`

- "`let` allows you to declare variables that are limited in scope to the block, statement, or expression on which it is used. This is unlike the var keyword, which defines a variable globally, or locally to an entire function regardless of block scope." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let
- P.S. `const` has the same rules of scope as `let`
- P.P.S. If `let` is used to declare a variable *outside* of a function, method, or class, it ends up in what is called *script scope*, which is a "global-like" scope where it will be visible in other JavaScript files
- "Redeclaring the same variable (with `let`) within the same function or block scope raises a SyntaxError"
- `let` bindings are created at the top of the (block) scope containing the declaration, commonly referred to as "hoisting". Unlike variables declared with var, which will start with the value undefined, let variables are not initialized until their definition is evaluated. Accessing the variable before the initialization results in a `ReferenceError`. The variable is in a "temporal dead zone" from the start of the block until the initialization is processed.


### I-C. Questions on Variable Scope

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

<hr>

7. What is the scope of the `pi` function below?

```js
<script>
	function init(){
		console.log("pi is approximately " + pi());
		
		function pi(){
			return 3.1415;
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

8. What will be logged out below?

```js
<script>
	var x;
	console.log(x);
	x = 10;
</script>
```

A) This will produce a runtime error

B) 10

C) undefined

<hr>

9. What will be logged out below?

```js
<script>
	console.log(x);
	var x;
	x = 10;
</script>
```

A) This will produce a runtime error

B) 10

C) undefined

<hr>

10. What will be logged out below?

```js
<script>
	console.log(x);
	let x;
	x = 10;
</script>
```

A) This will produce a runtime error

B) 10

C) undefined

<hr>


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


## III. Writing JavaScript Functions

## IV. Object Literals

## V. Classes
