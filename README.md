# p5collide
#### A 2d collision detection module for nodejs
p5collide provides tools for calculating collision detection for 2D geometry.

p5collide contains some versions of, and references to, the functions in [Jeffrey Thompson's Collision Detection Book](http://www.jeffreythompson.org/collision-detection/). His code is [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/), so, this is too! I highly, highly, reccomend [reading his book](http://www.jeffreythompson.org/collision-detection/) to better understand all of the details involved in collision detection. Implementing this library into your code will be much easier and more efficent after reading it!

It's an incredible resource for this kind of work! – [http://www.jeffreythompson.org/collision-detection/](http://www.jeffreythompson.org/collision-detection/)

All p5collide functions return `true` if the specified geometry is colliding and `false` if they are not.


## Install
```javascript
npm install p5collide
```

## Table of Contents

##### 2D Collision Detection
  + [collideAll()](#collideall)
  + [collidePointPoint()](#other-p5collides-function-examples--documentation)
  + [collidePointCircle()](#other-p5collides-function-examples--documentation)
  + [collidePointEllipse()](#other-p5collides-function-examples--documentation)
  + [collidePointRect()](#other-p5collides-function-examples--documentation)
  + [collidePointLine()](#other-p5collides-function-examples--documentation)
  + [collideRectRect()](#other-p5collides-function-examples--documentation)
  + [collideCircleCircle()](#other-p5collides-function-examples--documentation)
  + [collideRectCircle()](#other-p5collides-function-examples--documentation)
  + [collideLineLine()](#other-p5collides-function-examples--documentation)
  + [collideLineCircle()](#other-p5collides-function-examples--documentation)
  + [collideLineRect()](#other-p5collides-function-examples--documentation)
  + [collidePointPoly()](#other-p5collides-function-examples--documentation)
  + [collideCirclePoly()](#other-p5collides-function-examples--documentation)
  + [collideRectPoly()](#other-p5collides-function-examples--documentation)
  + [collideLinePoly()](#other-p5collides-function-examples--documentation)
  + [collidePolyPoly()](#other-p5collides-function-examples--documentation)
  + [collidePointTriangle()](#other-p5collides-function-examples--documentation)

## collideAll()
#### 1. Usage
With "Rect":
```javascript
const Rect = {
  type: "Rect",
  data: [x, y, width, height]
}
```
With "Circle":
```javascript
const Circle = {
  type: "Circle",
  data: [x, y, diameters]
}
```
With "Point":
```javascript
const Point = {
  type: "Point",
  data: [x, y]
}
```
With "Ellipse":
```javascript
const Ellipse = {
  type: "Ellipse",
  data: [x, y, width, height]
}
```
With "Line":
```javascript
const Line = {
  type: "Line",
  data: [x1, y1, x2, y2, buffer]
}
```
With "Poly":
```javascript
const PolyData = [
  { x1, y1 },
  { x2, y2 },
  { x3, y3 },
  { x4, y4 }
]
const Poly = {
  type: "Poly",
  data: [PolyData]
}
```
With "Triangle":
```javascript
const Triangle = {
  type: "Triangle",
  data: [x1, y1, x2, y2, x3, y3]
}
```
#### 2. Example
```javascript
const Collides = require("p5collide");

let object1 = {
    type: "RECT",
    data: [0, 1, 2, 3]
}

let object2 = {
    type: "CIRCLE",
    data: [1, 1, 2]
}

console.log(Collides.collideAll(object1, object2)); // Yes, it's true
```
#### 3. List possible object type
+ Rect
+ Circle
+ Point
+ Ellipse
+ Line
+ Poly
+ Triangle

## Other p5collide's function examples & documentation
You can see it here: https://github.com/bmoren/p5.collide2D

## Source
https://github.com/bmoren/p5.collide2D
