## Selector Lab

```js
/* create a story */
/* accept 5 user inputs (so confirm/prompt) at least 5 times */
/* based on the user input, you will createStoryBoard */
/* you can modify/duplicate this function for various boards */
/* when done, you should add one final storyBoard that is 'the end' */


// create functions for user input
// save variables for user input to use later if you need them
// make this fun! this is all about you being creative

// challenge:
// add a class argument to accept different classes
// to style each storyboard a little differently
// row:nth-child() in CSS if you're lazy

function createStoryBoard(header, subheader, blob) {
	var divRow = document.createElement('div');
	divRow.classList.add('row');
	var firstColumn = document.createElement('article');
	var secondColumn = document.createElement('article');
	var h1 = document.createElement('h1');
	var h3 = document.createElement('h3');
	var p = document.createElement('p');
	h1.innerHTML = header;
	h3.innerHTML = subheader;
	p.innerHTML = blob;
	firstColumn.appendChild(h1);
	firstColumn.appendChild(h3);
	secondColumn.appendChild(p);
	firstColumn.classList.add('six');
	firstColumn.classList.add('columns');
	secondColumn.classList.add('six');
	secondColumn.classList.add('columns');
	divRow.appendChild(firstColumn);
	divRow.appendChild(secondColumn);
	var container = document.getElementById('game-board');
	//elememt.classList.contains() // => boolean
	//element.classList.toggle()
	//element.classList.remove()
	var allRows = document.getElementsByClassName('row');
	// an array-like structure (but it is immutable)
	var firstRow = allRows[0];
	container.insertBefore(divRow, container.firstChild);
	//container.appendChild(divRow);
	console.log('fin');
}


window.onload = function(event) {
	createStoryBoard('holy crap',
		'hurricanes everywhere',
		'oh no it awful');
};
```
