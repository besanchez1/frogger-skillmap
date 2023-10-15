## Frogger

## Introduction @unplugged

In this tutorial you will create a simple Frogger game.
Let's start with giving a sprite movement!

## Step 1

 Go get a ``||variables:set mySprite to||`` block from ``||sprites:Sprites||``.
 Click on the grey image in the block to add the provided sprite or to open the Image Editor, and draw an image
 for your sprite.

 ```blocks
 let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
 ```

## Step 2

Pull out a ``||sprites:set mySprite stay in screen||`` block. Click the slider button to make it say **ON**.

```blocks
let mySprite = sprites.create(assets.image`Frogger`, SpriteKind.Player)
mySprite.setStayInScreen(true)
```

## Step 3

Now let's make the sprite move! Find the ``||controller:ControllerButtonEvent||`` block
in ``||controller:Controller||``. Put one for each direction on the gamepad.

```blocks
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

## Step 4

Go to the game simulator and run your program. Are you able to move the sprite 
and does it stay in the screen? Good!

## Step 5

To make things more interesting, get another ``||sprites:set mySprite||`` setting block.
Place it right after the ``||variables:set mySprite to||``. Select the ``show physics`` setting
and set the toggle button to **ON**

```blocks
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
