## Mid-Week Q&A

* What is the protocol for using `;`

Just do it; it follows naming conventions. Workplaces use style guides and you'll adhere to these.


* `"use strict";`

Do not use until wk5 at earliest.

* When do I use return?
When you want to assign the result of a function to a variable.

* Can I `return` instead of `;`?
```js
function stuff() {
  return; // void => undefined
}
```
Yes.

* How to build a function?

```js
function someName(args) {
  var ret = ""; // 0, false, etc
   // do code
  return ret;
}
```

* Can a function have multiple blocks?

```js
function dripCoffeeIntoIv(amount) {
  if (amount) {

  } // <-2nd block
} // <- 1st block
```

* Placement of functions

Global namespace should contain all functions; in any order needed. The only thing that order is weird on ('hoisting') variables (and this includes variables assigned to function).

```js
function stuff() {
  // cool anywhere
}
var x = function() {
  // top of page w/other variables
};
```

* Javascript file placement?!
document.

My advice: always use `window.onload` for selecting/manipulating elements. If you know jQuery, `$(document).ready()`.

Placement of JS file is personal choice.
