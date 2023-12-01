# Frogger Background and Tile Map

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

game.onUpdateInterval(500, function () {
    if (Math.percentChance(50)) {
        let projectile = sprites.createProjectileFromSide(img`
    . . . . . . f . . . f . . . . .
    . . . . f f 4 f f f 4 f . f . .
    . . f f 2 4 c f 2 4 2 f f 4 f .
    . f 4 2 f f f f 4 f f 4 2 2 f .
    . . f 4 2 e e e e 4 f 2 f f . .
    . . . f e c c c c c e e f . . .
    . . f e c 4 4 e c e b 2 e f . .
    . . f e 4 d d 4 e e 4 4 4 f . .
    . . f e 4 d d 4 e e 4 4 4 f . .
    . . f e c 4 4 e c e b 2 e f . .
    . . . f e c c c c c e e f . . .
    . . f 4 2 e e e e 4 f 2 f f . .
    . f 4 2 f f f f 4 f f 4 2 2 f .
    . . f f 2 4 c f 2 4 2 f f 4 f .
    . . . . f f 4 f f f 4 f . f . .
    . . . . . . f . . . f . . . . .
`, 50, 0)
        projectile.setPosition(0, 40)
    }
})

sprites.onOverlap(SpriteKind.Player, SpriteKind.Projectile, function (sprite, otherSprite) {
    game.gameOver(false)
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

Now that we've got our player and an enemy, let's add an environment.

In this tutorial, we'll add a background and a tilemap to the game.

## Step 1

**Background**

First, we'll add a simple background to add contrast for our player and enemy sprites.

## Step 2


Get a ``||scene:setBackgroundColor "___"||`` block and place it within **on start** block.

Set your prefered background color and test it to ensure you have your desired contrast.

```blocks
game.splash("Welcome to Frogger")
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
mySprite.setStayInScreen(true)
scene.setBackgroundColor(13)
```
## Step 3

A **background** is the foundation for creating our environment and is useful to fill in transparent tiles of a **tilemap**.

Let's now create a tilemap to go over our background and to serve as the game space.

## Step 4

To add a tilemap go into ``||scene:Scene||`` and grab ``||scene:setCurrentTilemap "___"||`` 
to place below our ``||scene:setBackgroundColor "___"||`` block.

Click the blank box to begin drawing your tilemap. In the **bottom left** I recommend setting 
the dimensions to **14** by **32**, but as long as it's longer than it is wide that's okay.

Have fun with this and be sure to use at least **three** different tiles to construct your map. This will be important later.

```blocks
game.splash("Welcome to Frogger")
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
mySprite.setStayInScreen(true)
scene.setBackgroundColor(13)
tiles.setCurrentTilemap(tilemap`Frogger_Lake1`)
```

## Step 4

Let's simulate again and see if anything is missing...

Currently if our player comes into contact with the enemy sprite, nothing happens. 
Let's fix that!

## Complete

Congratulations text.
