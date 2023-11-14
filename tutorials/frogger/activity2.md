# Frogger Enemies

```template
game.splash("Welcome to Frogger")
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . f f f f f . . . . f f f f f .
    f f 7 f 7 f 1 1 1 1 f 7 f 7 f f
    f 7 7 7 7 f f f f f 7 7 7 7 7 f
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

Start by grabbing a ``||game:onUpdateInterval "___"||`` and leave it at 500 ms.

```blocks
game.onUpdateInterval(500, function () {})
```

## Step 3
