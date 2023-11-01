# Frogger Enemies

```template
game.splash("Welcome to Frogger")
let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
mySprite.setFlag(SpriteFlag.ShowPhysics, true)
mySprite.setStayInScreen(true)

controller.up.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.y += -16
})
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x += -16
})
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x += 16
})
controller.down.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.y += 16
})
```

### @explicitHints true

## Introduction @unplugged

**Are you ready to begin creating your own Frogger game?**

Complete this tutorial to learn how to:
- Find blocks in the toolbox
- Build code using those blocks in the workspace
- Add a simple splash screen
- Create/Add sprites to your game
- Add movement to a sprite
- Run your Frogger game on the built-in simulator

Soon enough you'll have your very own Frogger clone!

## Step 1

**Welcome!**

Let's hit the ground running and add our splash screen.

Grab a ``||game:splash "___"||`` block and add some text to welcome your players.

```blocks
game.splash("Welcome to Frogger")
```

## Step 2

Now that we have a splash screen to greet players, let's add our Frogger!

 Go get a ``||variables:set mySprite to||`` block from ``||sprites:Sprites||``. 
 Add this below the ``||game:splash "___"||`` block.
 
 Click on the grey image in the block to add the provided sprite 
 or to open the Image Editor, and draw an image for your sprite.

 ```blocks
game.splash("Welcome to Frogger")
 let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
 ```

## Step 3

Pull out a ``||sprites:set mySprite stay in screen||`` block and add it to the bottom. 
Click the slider button to make it say **ON**.

```blocks
game.splash("Welcome to Frogger")
let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
mySprite.setStayInScreen(true)
```

## Step 4

Now let's make the sprite move! Find the ``||controller:ControllerButtonEvent||`` block
in ``||controller:Controller||``. Pull out a total of four for each direction on the gamepad.

In **MakeCode** sprites are 16x16 pixels, so we need to add 
or subract 16 pixels for each button pressed for our movement.

```blocks
game.splash("Welcome to Frogger")
let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
mySprite.setStayInScreen(true)

controller.up.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.y += -16
})
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x += -16
})
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x += 16
})
controller.down.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.y += 16
})
```

## Step 5

Go to the game simulator and run your program. Are you able to move the sprite 
and does it stay in the screen? Good!

## Step 6

To make things more interesting, get another ``||sprites:set mySprite||`` setting block.
Place it right after the ``||variables:set mySprite to||``. Select the ``show physics`` setting
and set the toggle button to **ON**

```blocks
game.splash("Welcome to Frogger")
let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
mySprite.setFlag(SpriteFlag.ShowPhysics, true)
mySprite.setStayInScreen(true)

controller.up.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.y += -16
})
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x += -16
})
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x += 16
})
controller.down.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.y += 16
})
```

## Complete

That's it. You've got Frogger moving around. You're awesome!
