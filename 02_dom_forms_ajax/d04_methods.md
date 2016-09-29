## Methods

#### Event Listeners

```js
$("button").on("click", function() {
  // do something
});
```

#### CSS Modification

```js
$(selector).css({ "display": "none",
    "visibility": "hidden"
});
```

#### Collection Manipulation

- `$.each(collection, function(index, item){});`
- `$.map(collection, function(item, index){});`

###### $.each vs $.map
- $.each returns original array unchanged
- $.map runs function for each item in array and creates/returns a new array from returned result


```js
var cities = ['paris', 'london', 'orlando'];

$.each(cities, function(index, city) {
	var result = city + " " + index;
	console.log(result);
});

$.map(cities, function(city, index) {
	var result = city + " " + index;
	console.log(result);
	return result;
});
```

#### detach

`.detach()` removes an element from DOM, preserving all data/events. Useful for DOM insertions and replacement.
