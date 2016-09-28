## Creating Elements and Putting them on the DOM

> *When we createElement*, it is **not** on the DOM. It lives in memory. We _must attach it to the DOM ourselves_.


```javascript
// basic selectors
// declare a selector named container
// access that container via document.getElementById('name-of'id)
var container = document.getElementById('container');
console.log(container);
var monsters = ['Wreck-it Ralph', 'The giraffe from Lion King SNES', 'Ganon'];

for (var baddie in monsters) {
  // create a new dom element using document.createElement('name-of-tag');
  var li = document.createElement('li');
  console.log(li);
  // access and assign a property to my dom element
  li.innerHTML = monsters[baddie];
  // append it to a container using selector.appendChild(domElement)
  container.appendChild(li);
}
```
