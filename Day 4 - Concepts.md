### Day 4

## Scope
Global scope - For bindings defined outside of any function or block, the scope is the whole program (you can refer to such bindings wherever you want).

Local scope - Bindings created for function parameters or declared inside a function can be referenced only in that function.

Lexical scoping - The set of bindings visible inside a block is determined by the place of that block in the program text. Each local scope can also see all the local scopes that contain it, and all scopes can see the global scope. 

Use `var` for globals, reserve `let` and `const` for block scopes.

## Hoisting
```jsx
function catName(name) {
	console.log("My cat's name is " + name);
}

catName("Tiger");

// My cat's name is Tiger
```

```jsx
catName("Tiger");

function catName(name) {
	console.log("My cat's name is " + name);
}

// My cat's name is Tiger
```

JavaScript only hoists declarations, not initializations.

```jsx
console.log(num);
var num;
num = 6;

// undefined
```

```jsx
x = 1;
console.log(x + " " + y);
var y = 2;

// 1 undefined (because JavaScript only hoists declarations)
```

## Closures
```jsx
var me = "Naomi";
function greetMe() {
	console.log('Hello, ' + me + '!');
}

greetMe()

//Hello, Naomi!
```

```jsx
function sendRequest() {
	var requestID = '123';
	$.ajax({
		url: '/myurl',
		succes: function(response) {
			alert('Request ' + requestID + ' returned')
		}
	});
}
```

When you start a task and you want to specify something that happens when that task is done, with stuff that is available to you when you start the task, closures makes that easy and readable.