### Day 2

## Functions; parameters and arguments
```jsx
//Call a function
ellipse(100, 100, 50, 50); 
```

```jsx
//Define a function
function setup(){
	key1: 'first',
	key2: 'last'
}
```

1. Modularity

    organize functions, break them up in pieces

```jsx
function draw(){
	background(0);
	move(); //calls the function
	bounce(); //calls the function
	display(); //calls the function
}

//Define the functions
function move() {
	ball.x = ball.x + ball.xspeed;
	ball.y = ball.y + ball.yspeed;
}

function bounce() {
	if (ball.x > width || bal.x < 0) {
		ball.xspeed = ball.xspeed * -1;
	}
	if (ball.y > height || ball.y < 0) {
	ball.yspeed = ball.yspeed * -1;
	}
}

function display() {
	stroke(255);
	strokeWeight(4);
	noFill();
	ellipse(ball.x, ball.y, 24, 24);
}
```

## Higher order functions
`=>` arrow function

```jsx
function multiplier(factor) {
	return function(x){
		return x * factor;
	}
}

//console log
let doubler = multiplier(2);
// undefined
let tripler = multiplier(3);
// undefined
doubler
/* function multiplier(factor) {
		return function(x){
			return x * factor;
		}
	}*/
doubler(4);
// 8
tripler(4);
// 12

```

```jsx
function multiplier(factor) {
	return function(x){
		return x * factor;
	}
}

/* kun je ook schrijven als*/
function multiplier(factor) {
	return x => x * factor;
}

let doubler = multiplier(2);
let tripler = multiplier(3);

//console
doubler(4);
// 8
tripler(4);
// 12
```