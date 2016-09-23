## Jim's Example

#### HTML

```html
<div class="parent">
   <p>Parent div with 50% width.</p>
   <div class="child">
     <p>Child div with 90% width, 4px black border, and 20% padding </p>
   </div>
   <div class="twins">
     <p>Child div with 50% width, 4px black border, and 1em padding</p>
   </div>
   <div class="twins">
     <p>Child div with 50% width, 4px black border, and 1em padding</p>
   </div>
 </div>
```

#### CSS

```css
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

body {
  background-color: white;

}

.parent {
  width: 50%;
  border: 5px solid green;
  float: left;
}

.child {
  width: 90%;
  padding: 20%;
  border: 4px solid black;
  margin: 0 auto;
}

.twins {
  width: 40%;
  padding: 0;
  float: left;
  border: 4px solid black;
  margin-left: 1%;
}

.twins:nth-child(2n){
  margin-left: 3%;
  background-color: indigo;
}
```

#### Javascript

```javascript
console.log('window is loaded')


// Create a function that takes two strings and combines them together

document.getElementById()

var array = ['phish', 'burriot', 'george']
// creating a funciton that takes the argument of an array,
// and combines contents into a string
function stringCombinerOfAnArray(starbucksArray){
  var combinedString;
  for (var i = 0; i < starbucksArray.length; i++){
    combinedString = starbucksArray[i] + combinedString
    console.log(combinedString)
  }

  return combinedString;
}

function returnsAnArray(){
  return ["jim", "james"]
}



function stringCombiner(str1, str2){
  var combinedString = str1 + str2;
  console.log(str1, str2)
  combinedString = str1 + str2;
  return combinedString;
}


stringCombiner("i love", "tacos")
```
