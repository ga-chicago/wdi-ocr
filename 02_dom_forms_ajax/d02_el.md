## Protip: 'el'

You can add a DOM selector to an object and modify it inside of your object for easy reference.

```js
var lifeMeter = {
	el: document.getElementById('life-meter'),
	function: updateHealth(number) {
    	this.el.innerHTML = number;
	}
};
lifeMeter.updateHealth(42);
```
