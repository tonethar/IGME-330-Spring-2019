# first-canvas

Here is a starter file for our canvas exercises.

**first-canvas.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>First Canvas Done</title>
	<style type="text/css">
	canvas{
		border:1px solid gray;
	}
	</style>
	<script>
		// #0 - in this class we will always use ECMAScript 5's "strict" mode
		// See what 'use strict' does here:
		// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode
		'use strict';
		
		// #1 call the `init` function after the pages loads
		window.onload = init;
	
		function init(){
			console.log("page loaded!");
			// #2 Now that the page has loaded, start drawing!
			
			// A - `canvas` variable points at <canvas> tag
			let canvas = document.querySelector('canvas');
			
			// B - the `ctx` variable points at a "2D drawing context"
			let ctx = canvas.getContext('2d');
			
			// C - all fill operations are now in red
			ctx.fillStyle = 'red'; 
			
			// D - fill a rectangle with the current fill color
			ctx.fillRect(20,20,600,440); 
		}
	</script>
</head>
<body>
	<canvas width="640" height="480">
		Get a real browser!
	</canvas>
</body>
</html>
```
