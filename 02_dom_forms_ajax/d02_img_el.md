## Image Element

```javascript
// now, we need to create an image!
var kittenImage = document.createElement('img');
// alt text (alt) - ADA compliancy text for the blind
kittenImage.alt = 'A cute random kitten';
kittenImage.id = 'kitten';
// src = image source
kittenImage.src = 'http://vignette3.wikia.nocookie.net/clubpenguinpookie/images/d/d0/Extremely-cute-kitten_large.jpg/revision/latest?cb=20140614000321';
// append my element as a child to a selector
body.appendChild(kittenImage);
```
