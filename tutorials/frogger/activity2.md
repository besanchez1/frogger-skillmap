# Frogger Enemies

```template
game.splash("Welcome to A Frogger Clone")
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . f f f f f . . . . f f f f f .
    f f 7 f 7 f . . . . f 7 f 7 f f
    f 7 7 7 7 f f f f f f 7 7 7 7 f
    f f f 7 7 7 7 7 7 7 7 7 7 f f f
    . f 7 7 7 7 7 7 7 7 7 7 7 7 f .
    f f 7 7 7 7 7 7 7 7 7 7 7 7 f f
    f 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f
    f 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f
    f 7 7 7 1 8 1 7 7 1 8 1 7 7 7 f
    f 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f
    f 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f
    f f 7 7 7 7 7 3 3 7 7 7 7 7 f f
    f f 7 7 7 f f 3 3 f f 7 7 7 f f
    f 7 7 7 7 7 f 3 3 f 7 7 7 7 7 f
    f f 7 f 7 f f f f f f 7 f 7 f f
`, SpriteKind.Player)
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

```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"/></xml>",
  "main.ts": "\n",
  "pxt.json": "{\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n    \"targetVersions\": {\n        \"branch\": \"v1.3.44\",\n        \"tag\": \"v1.3.44\",\n        \"target\": \"1.3.44\",\n        \"pxt\": \"6.8.33\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n"
}
```

### @explicitHints true

## Introduction @unplugged

Are you ready to present the player with some obstactes?

In this tutorial, you'll learn to have projectiles cross the screen, 
which players will have to avoid.

## Step 1

**Time for some enemies!**

Now that we have the basic character movement complete let's add some enemies.

Let's look at how we can add enemies that come from the side every so often.

## Step 2

Start by grabbing an ``||game:onUpdateInterval "___"||`` from ``||game:Game||`` and leave it at 500 ms.

Next go into ``||sprites:Sprites||`` and get a ``||sprites(variables):createProjectileFromSide||`` 
to place in the ``|game:onUpdateInterval "___"|`` block,
and draw an enemy for your character to avoid. 

If you don't want to draw it yourself, you can select a premade asset. 
An enemy sprite will also be provided in the next skillmap step.

Once finished, set **vy** to **0**. Othwerise, the sprite will be moving diagonally. 

```blocks
game.onUpdateInterval(500, function () {
projectile = sprites.createProjectileFromSide(assets.image`Spider_Down`, 50, 0)
})
```

## Step 3

If we simulate our game right now you'll notice the 
enemy sprite is appearing at the top of the screen.

To fix this, put a ``||sprites(variable):set Position "Projectile" to "___"||`` below and set it to **(0,40)**.

Now our enemy sprite should be right above where the player starts.

```blocks
game.onUpdateInterval(500, function () {
projectile = sprites.createProjectileFromSide(assets.image`Spider_Down`, 50, 0)
projectile.setPosition(0, 40)
})
```

## Step 4

Let's simulate again and see if anything is missing...

Currently if our player comes into contact with the enemy sprite, nothing happens. 
Let's fix that!

## Step 5

Grab an ``||sprites:onOverlap||`` block and change the second dropdown to ``|sprites.Projectile|``.

Then place a ``||game:gameOver||`` within and set it to **LOSE**.

Simulate and see what happens!

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Projectile, function (sprite, otherSprite) {
    game.gameOver(false)
})
```

## Step 6

Notice, now when the player comes into contact with the enemy we get a **Game Over**.

But right now our player can't get through the line of enemies, so we're going to change that.

## Step 7

To space out our enemies we will use an ``||logic:if "___"||`` with a ``||Math:percentChance||``.

By dragging the ``||Math:percentChance||`` into the ``||logic:if "___"||`` we can set a chance of an enemy appearing
everytime our ``|Game:onUpdateInterval "___"|`` runs.

```blocks
if (Math.percentChance()) {}
```

## Step 7

Place everything that was in ``|Game:onUpdateInterval "___"|`` in to ``|Logic:if "___"|``, then place the ``|Logic:if "___"|``
into ``|Game:onUpdateInterval "___"|``. 

Set the ``|Math:percentChance|`` to **50%**, and let's see the result!

```blocks
game.onUpdateInterval(500, function () {
    if (Math.percentChance(50)) {
        projectile = sprites.createProjectileFromSide(assets.image`Spider_Down`, 50, 0)
        projectile.setPosition(0, 40)
    }
})

sprites.onOverlap(SpriteKind.Player, SpriteKind.Projectile, function (sprite, otherSprite) {
    game.gameOver(false)
})
```

## Complete

Now our enemies work as intended and the player can get past. Fantastic work!
