## DOM Children Manipulation

We can access the child of a selected node.

Let's build an `<hgroup>` that contains an `<h1>` and an `<h3>`.

```js
var hgroup = document.createElement('hgroup');
hgroup.appendChild(document.createElement('h1'));
hgroup.appendChild(document.createElement('h3'));
```

We now have:

```
<hgroup> (parent/root)
|
|- <h1> (child)
|- <h3> (child)
```

#### Seeing all Children

You can use the `.children` method to return an array of child elements.

```js
hgroup.children
// => [<h1>​</h1>​, <h3>​</h3>​]
```

You could then loop through or check the length.

```js
hgroup.children.length
// => 2
hgroup.childElementCount
// => 2
```

#### Inserting Before (prepend)

We can insert a new element before all other child elements inside of our `hgroup`. We will use .insertBefore. The syntax is like so: `.insertBefore(elementToInsert, target);`

```js
var jerk = document.createElement('strong');
hgroup.insertBefore(jerk, hgroup.firstChild);
```

The first argument is the element you want to add. The second argument is the element you'd like to insert your item in front of.


#### Inserting After (append)

We can add an element after all other children elements using `.appendChild()`.

```js
hgroup.appendChild(document.createElement('h4'));
```
