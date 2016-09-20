
###### Prior Class Whiteboards

![data-types.jpg](data-types.jpg)

![variable-declaration.jpg](variable-declaration.jpg)

![data-types-js-java.jpg](data-types-js-java.jpg)

![arrays.jpg](arrays.jpg)


## Array & Loop

```javascript
var cocktails = ['gin & tonic', 'white russian', 'mojito', 'sangria', 'grape ape'];

cocktails.pop();  // pop() removes the last item in an array

// this didn't work...
//var lengthOfArray = cocktails.length;

// this will!
for (var i = 0; i <= cocktails.length; i++) {

  console.log('i = ' + i);
  //console.log('array length = ' + lengthOfArray);''
  console.log(cocktails[i]);

  console.log("I could use a... " + cocktails[i]);

  cocktails.pop();
}
```

##### Scope and Blocks

```javascript
// block of code
{
  console.log('hello, world');
}

var age = confirm('Are you over 21?');
if (age === true) {
  alert('huzzah');
} else {
  alert('soon.jpg');
}

// 'location' is a reserved word
var somewhere = window.location.host;
if (somewhere != 'ga-chicago.github.io') {
  alert('oh no! this is not the right website.');
} else {
  alert('awww yeaah u aint hackd');
}

var userInput = prompt('what is your name?');

if (userInput.length < 1) {
  alert('hey, you didn\'t give us your name');
} else {
  alert('thanks, ' + userInput + '!!!!!@121211212');
}

// and operator &&

if (age >= 21 && hasMoney == true) {
  // you can buy booze
}

if (21 >= 21 && true == true) {
  console.log('you can haz booze');
}


// OR operator ||

if (true || false) {
  console.log('boolean party!!@!212');
}

var name = 'james';
if (name === 'james' || name === 'jim') {
  console.log('j names rule');
}


var car = 'ford';
switch (car.toLocaleLowerCase()) {
  case "mazda": alert('mazdas zoom zoom');
    break;
  case "nissan": alert('the leaf is green');
    break;
  default:
    alert('your car is not here..?!@');
    break;
}
```
