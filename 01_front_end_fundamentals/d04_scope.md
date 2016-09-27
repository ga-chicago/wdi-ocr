## Scope, Global vs Local Variables

```javascript
// global variables
var items = [];
var message = "welcome";
// these can be used anywhere in any function
// or any block of code

window.onload = function(evt) {
	var welcome = htmlBuilder('h1', message);
	var body = document.getElementsByTagName('body');
	body[0].appendChild(welcome);
	console.log(welcome);
	console.log(body);
	// tell document to append an element
	// to the end of itself
};

function htmlBuilder(tagType, content) {
	var el = document.createElement(tagType);
	el.innerHTML = content;
	// <tag></tag>
	return el; // not a void method
	// why? we return :)
}

// we're trying to access or USE
// a local variable
//console.log(el); // undefined

function htmlBoldBuilder(tag, content) {
	var el = document.createElement(tag);
	el.innerHTML = "<strong>" + content + "</strong>";
	return el;
}

function htmlItalicBuilder(tag, content) {
	var el = document.createElement(tag);
	el.innerHTML = "<em>" + content + "</em>";
	return el;
}

// build a function
// it will have 0 arguments
// this function will prompt() a user for some input
// that input should be added as innerHTML
// to a brand new 'p' elemenet
// your function returns void
// your function ends with appending your element
// to the body (hint: use the body global variable)

function displayInput() {
	var input = prompt('hello, what do you say?');
	var el = document.createElement('p');
	el.innerHTML = input;
	var body = document.getElementsByTagName('body');
	body[0].appendChild(el);
	// no return - this is void :)
}



// create 2 more function
// htmlItalicBuilder <em></em>
// htmlBoldBuilder <strong></strong>
// bonus:
// element.style (console.log)
// element.style.color
```
