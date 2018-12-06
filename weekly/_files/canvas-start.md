# canvas-start.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Canvas Starter</title>
	<style>
	canvas{
		border:1px solid gray;
	}
	</style>
</head>
<body>
	<canvas width="640" height="480">
		Get a real browser!
	</canvas>
	<script>
		'use strict';
		
	init();
	
	function init(){
		let ctx = document.querySelector('canvas').getContext('2d');
		ctx.fillStyle = 'red'; 
		ctx.fillRect(20,20,600,440); 
	}
	</script>
</body>
</html>
```
