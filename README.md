<!--- header image --->
<p align="left">
  <img alt="" style="{max-height: 0px}" src="./Dinosaur Game/The Dinosaur Game.png">
</p>

## How to play Dinosaur Game

You can click [here](chrome://dino/) to play or turn off your internet to access `Dinosaur Game`

- Just open `chrome://dino` in your web browser, and you’ll be taken to an "arcade mode" where you can practice in a full-window environment.

- Press `Space` to play `▶`.

- You can see `HI` to check your `Highest` & `Current` Score.

<p align="left">
  <img alt="" style="{max-height: 0px}" src="./Dinosaur Game/Press space to play.PNG">
</p>

# Automation/Hack for Dinasour Game

#### Tweaking Speed

Type the following command in Console and press enter. You can use any other speed in place of 1000.

```js
Runner.instance_.setSpeed(1000)
```

#### Immortality

After every command press enter. All the commands are case-sensitive.

We store the original game over function in a variable:

```js
var original = Runner.prototype.gameOver
```

Then, we make the game over function empty:

```js
Runner.prototype.gameOver = function(){}
```

Stopping the game after using Immortality

When you want to stop the game, Revert back to the original game over function:

```js
Runner.prototype.gameOver = original
```

#### Setting the current score

Let’s set the score to 12345. You can set any other score less than 99999. The current score is reset on game over.

```js
Runner.instance_.distanceRan = 12345 / Runner.instance_.distanceMeter.config.COEFFICIENT
```

#### Dino jumping too high?

You can control how high the dino jumps by using the below function. Adjust the value as necessary.

```js
Runner.instance_.tRex.setJumpVelocity(10)
```

#### Fully Automation Dino / Auto Jumping

You can fully automate your dino using the given code on console.

```js
function keyDown(e){Podium={};var n=document.createEvent("KeyboardEvent");Object.defineProperty(n,"keyCode",{get:function(){return this.keyCodeVal}}),n.initKeyboardEvent?n.initKeyboardEvent("keydown",!0,!0,document.defaultView,e,e,"","",!1,""):n.initKeyEvent("keydown",!0,!0,document.defaultView,!1,!1,!1,!1,e,0),n.keyCodeVal=e,document.body.dispatchEvent(n)}function keyUp(e){Podium={};var n=document.createEvent("KeyboardEvent");Object.defineProperty(n,"keyCode",{get:function(){return this.keyCodeVal}}),n.initKeyboardEvent?n.initKeyboardEvent("keyup",!0,!0,document.defaultView,e,e,"","",!1,""):n.initKeyEvent("keyup",!0,!0,document.defaultView,!1,!1,!1,!1,e,0),n.keyCodeVal=e,document.body.dispatchEvent(n)}setInterval(function(){Runner.instance_.horizon.obstacles.length>0&&(Runner.instance_.horizon.obstacles[0].xPos<25*Runner.instance_.currentSpeed-Runner.instance_.horizon.obstacles[0].width/2&&Runner.instance_.horizon.obstacles[0].yPos>75&&(keyUp(40),keyDown(38)),Runner.instance_.horizon.obstacles[0].xPos<30*Runner.instance_.currentSpeed-Runner.instance_.horizon.obstacles[0].width/2&&Runner.instance_.horizon.obstacles[0].yPos<=75&&keyDown(40))},5);

Runner.instance_.setSpeed(1000)

var original = Runner.prototype.gameOver
Runner.prototype.gameOver = function(){}

//Runner.prototype.gameOver = original

Runner.instance_.distanceRan = 12345 / Runner.instance_.distanceMeter.config.COEFFICIENT

Runner.instance_.tRex.setJumpVelocity(10)
```

## End of Dinosaur Game

- It's an `endless` running game, like a `straight-line` version of Temple Run with no levels. 

- Literally endless : get to the `maximum` possible score of `99,999` and the game simply `resets` itself.
