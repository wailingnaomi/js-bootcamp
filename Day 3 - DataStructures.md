### Day 3

## Arrays

```jsx
var words = ["rainbow", "heart", "purple", "friendship"];

var index = 0;

function show(){
	text(words[index], 12, 200);
}

function mousePressed(){
	index = index + 1;

	if (index == words.length){ 
		index = 0;
	}
}
```

## Objects
```jsx
//ipv
var x = 0;
var y = 100;
var diameter = 50;

//
var circle = {
	x: 0,
	y: 100,
	diameter: 50
};

function draw(){
	ellipse(circle.x, circle,y, circle.diameter, circle.diameter);
	
	circle.x = circle.x + 1;
}
```