#WDI Week 2, Day 2:  GH-Pages & Objects have velocity

---

### Learning Objectives

- Create a git branch
- Merge into a branch
- Launch a static website to the world!

---

###OPENING -  Github Pages 5 minutes
Turns out… github will host your static websites for FREE!!!
All we need to do is push our static site to a specific ‘branch’
A git ‘branch’ is just another version of the code

---

###I DO - 10 minutes
While completing these commands, prompt the students to help describe the intention of each.  They should have seen most of this before, but we can trust it is not fresh for them
```bash
mkdir helloWeb
cd helloWeb
echo “HELLO” > index.html
git init
git add .
git commit -m "my initial commit"
git checkout -b gh-pages
    # Create a new repo on github & copy the ssh link
git remote add origin **ssh link to github repository**
git push origin gh-pages
```
Go to **username**.github.io/**repository name** in the browser


---

###YOU DO - 10 minutes
In pairs, help each other launch your favorite animation from the morning… to your own github page




---

###OPENING - Velocity
Let’s not add to our morning codebase with the squares
In the real world… things have velocity… which is just another way of saying… speed in different directions…
Let’s add velocity to our object animation problem domain!
Prompt the students to discuss what this could mean?
Question: Is this an attribute?
Answer: Yes
Question: Is this an ability?
Answer: No
Question: How would the updating ability be different?
Answer: We’d move by velocity instead of some random number of pixels

---

###WE DO: Velocity! - 10 minutes
- We want objects to move on the screen in different directions!
- Let's use 'velocity' to accomplish this task!
- Instead of saving direction of some kinds... let's save how much x direction and how much y direction the object should move for each tick
- Use the following example
- to add a ```xVel``` and ```yVel``` to the square objects and add a update function to the square itself
- All students should code along


```javascript
var Square = function(x, y, wallSize, color) {
  this.x = x;
  this.y = y;
  this.wallSize = wallSize;
  this.color = color;
  this.xVel = Math.random();
  this.yVel = Math.random();

  this.draw = function draw(ctx){
    ctx.fillStyle = this.color;
    ctx.fillRect(this.x, this.y, this.wallSize, this.wallSize);
  };

  this.update = function update(ctx){
    this.x += this.xVel;
    this.y += this.yVel;
  };
};
```

---

###WE DO: Clear Canvas! - 2 minutes
- Let's clear the canvas each time we draw!
```ctx.clearRect(0, 0, canvas.width, canvas.height);```

---

###YOU DO: More Squares! - 15 minutes
- On each ```tick``` create a new randomly sized square to the canvas

```javascript
setInterval(function(){
  squares.push(new Square(0, 0, Math.random()*25, 'red'));
  tick(squares);
  color(squares);
  draw(squares, ctx, canvas);
}, 30)
```


---

###YOU DO: Lab/Homework User Input
- Tell students to NOT worry about this!!!  Just use it for now!
- Provide this code via chat or gist
- Have students place this in the Square's constructor function
```javascript
var handleKeyDown = function(event) {
  console.log(event.keyCode)
  if (event.keyCode === 37) {
    console.log("left arrow pressed!... what should happen???? Maybe move left... or change xVel?");
    // Place Your Code HERE
  } else if (event.keyCode === 38) {
    console.log("up arrow pressed!... what should happen???? Maybe move up... or change yVel?");
    // Place Your Code HERE
  } else if (event.keyCode === 39) {
    console.log("right arrow pressed!... what should happen???? Maybe move right... or change xVel?");
    // Place Your Code HERE
  } else if (event.keyCode === 40) {
    console.log("down arrow pressed!... what should happen???? Maybe move down... or change yVel?");
    // Place Your Code HERE
  }
}
window.addEventListener('keydown', handleKeyDown.bind(this),true);
```


####Instructor Example:
```javascript
var handleKeyDown = function(event) {
  console.log(event.keyCode)
  if (event.keyCode === 37) {
    this.xVel -= 0.3;
  } else if (event.keyCode === 38) {
    this.yVel -= 0.3;
  } else if (event.keyCode === 39) {
    this.xVel += 0.3;
  } else if (event.keyCode === 40) {
    this.yVel += 0.3;
  }
}
window.addEventListener('keydown', handleKeyDown.bind(this),true);
```

---

###CLOSING - 10-20 minutes
Tell students:  You now have the tools to build entire games!
How would we build the classic game ‘Pong’
Whiteboard with the class what objects we would likely need to re-create pong
This is time for the students to apply these new tools to a problem domain
Guide the conversation
Bonus Homework:   Build “pong”   (this is DIFFICULT!)

---

###LAB/HOMEWORK
- Similar to the moving squares...
  - Draw a circles that fall on the screen like rain
  - Include wind!   (show demo before class leaves)


```js

var windXVel = 0;
var windYVel = 0;

function handleKeyDown (event) {
  if (event.keyCode === 37) {
    this.windXVel -= 0.1;
  } else if (event.keyCode === 38) {
    this.windYVel -= 0.1;
  } else if (event.keyCode === 39) {
    this.windXVel += 0.1;
  } else if (event.keyCode === 40) {
    this.windYVel += 0.1;
  }
}
window.addEventListener('keydown', handleKeyDown.bind(this), true);

```
