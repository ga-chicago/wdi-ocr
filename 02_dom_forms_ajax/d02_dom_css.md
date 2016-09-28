## Modify Element Style (CSS)

#### Through dot notation (everything is an object)

> *Try this out in Chrome*; autocomplete will show you all style properties!

The `el.style` is an object; it will contain attributes such as `width` and `backgroundColor`.

``` js
// first grab the body, we use the [0] at the end because
// getElementsByTagName method returns an array
var body = document.getElementByTagName('body')[0];

body.style.backgroundColor = "blue";
//  when you press enter the page should turn blue
// "body has a style property, what else can you change?"

// next lets create an element to 'append' to the body
// first create the object/ element
var obj = document.createElement('div')
// now that we created the element lets set
// some 'properties'
obj.style.backgroundColor = 'red';
obj.style.width = '100px';
obj.style.height = '100px';

// now we have to append 'obj' to the body in order
// to put it on the page
body.appendChild(obj);
```

#### Through classList and className

We can modify an element's class list by hand:

```js
var body = document.getElementById('body')[0];
body.classList
// => [] (an array like collection/list of classes)
// add classes
body.classList.add('six');
body.classList.add('columns');
// check the length
body.classList.length;
// toggle classes on/off by adding/removing it to an element
body.classList.toggle('meow');
// => false / true
// do we have a class?
body.classList.contains('meow');
// => false / true
```
