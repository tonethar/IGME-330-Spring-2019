# Week 3A - Review recent HW & Build a paint app

## I. Overview
Today we will:
- review [HW-shape-viewer.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer.md) - an important concept is how to pass data *from* HTML elements *to* your JavaScript - there are several approaches that work - we will look at 5 of them:
  - `drawBox()`- pass color data inside an anonymous wrapper function
  - `drawBox()`- pass data from an `onclick` attribute of the button (but the mixing of HTML & code is not generally recommended)
  - `drawBox()`- pass color data by utilizing `e.target`
  - `drawBox()`- pass color data by utilizing `this`
    - in regular functions, the value of `this` in a function is determined by how the function is *called*. The `this` mechanism is thus resolved **dynamically** at run-time
    - BTW - arrow functions don't bind their own `this` -  `this` in an arrow function instead binds to its **lexical scope** (aka static scope) that is determined by where the code is written
  - `drawBox()`- pass color data via an HTML5 custom data attributes:
    - we briefly covered HTML5 custom data attributes in IGM-230 - see [web-apps-6.md#section7](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-6.md#section7)
    - how to do this? You need to create an attribute named `data-color`, and then access it with either `element.getAttribute("data-color")` or `element.dataset.color`
- review [HW-try-it.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-try-it.md)
  - to draw the squares, circles, and polygons, this requires a good understanding of `ctx.translate()`, `ctx.rotate()` and `ctx.scale()` as well as `ctx.save()` and `ctx.restore()`
  - note how we can flip the text along its horizontal or vertical axis with `ctx.scale(-1,1)` or `ctx.scale(1,-1)`
- review [HW-SG-2.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-2.md) - concepts:
  - line caps, line joins, line dashes
  - A **gradient** specifies a starting color, an ending color, and an area over which color changes. A single gradient can encompass more than one color change
    - linear gradient - https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/createLinearGradient
    - radial gradient - https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/createRadialGradient
    - see demo code below
  - bezier curves:
      - `ctx.quadraticCurveTo(ctrlX, ctrlY, endX, endY)` draws bezier curves with 1 control point
      - `ctx.bezierCurveTo(ctrlX, ctrlY, ctrlXa, ctrlYa, endX, endY)` draws cubic bezier curves with 2 control points
      - curve building demos
      - animating curves

## II. Demo Code

**linear-gradient.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Linear Gradient</title>
</head>
<body>
<canvas width="640" height="480"></canvas>
<script>
	let ctx = document.querySelector("canvas").getContext("2d");
	let grad = ctx.createLinearGradient(100, 0, 300, 0);
	grad.addColorStop(0, 'red');
	grad.addColorStop(1 / 6, 'orange');
	grad.addColorStop(2 / 6, 'yellow');
	grad.addColorStop(3 / 6, 'green')
	grad.addColorStop(4 / 6, 'aqua');
	grad.addColorStop(5 / 6, 'blue');
	grad.addColorStop(1, 'purple');
	
	ctx.fillStyle = grad;
	ctx.fillRect(0,0,640,480);
	
</script>
</body>
</html>
```

**radial-gradient.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Radial Gradient</title>
</head>
<body>
<canvas width="640" height="480"></canvas>
<script>
	let ctx = document.querySelector("canvas").getContext("2d");
	let grad = ctx.createRadialGradient(150,150, 20, 150, 150, 125);
	grad.addColorStop(0, 'red');
	grad.addColorStop(1 / 6, 'orange');
	grad.addColorStop(2 / 6, 'yellow');
	grad.addColorStop(3 / 6, 'green')
	grad.addColorStop(4 / 6, 'aqua');
	grad.addColorStop(5 / 6, 'blue');
	grad.addColorStop(1, 'purple');
	
	ctx.fillStyle = grad;
	ctx.fillRect(0,0,640,480);
	
// 	ctx.beginPath();
// 	ctx.arc(150,150,125,0,Math.PI*2,false);
// 	ctx.closePath();
// 	ctx.fill();
</script>
</body>
</html>
```

## III. Presentation
- Let's talk about [HW-drawing-app.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-drawing-app.md)

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02B-notes.md**](week-02B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-03B-notes.md**](week-03B-notes.md)
