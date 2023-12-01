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
  "tilemap.g.ts": // Auto-generated code. Do not edit.
\nnamespace myTiles {
    //% fixedInstance jres blockIdentity=images._tile
    \nexport const transparency16 = image.ofBuffer(hex``);
    //% fixedInstance jres blockIdentity=images._tile
    \nexport const tile1 = image.ofBuffer(hex``);
\n
    \nhelpers._registerFactory(\"tilemap\", function(name: string) {
        \nswitch(helpers.stringTrim(name)) {
            \ncase \"Frogger_Strip\":
            \ncase \"Frogger_Lake1\":return tiles.createTilemap(hex`0e001800030301020201010102030303030303030302030202020202030202010103030303030202020202020201010101010102020101010101010107070707070707070707070707070707070707070707070707070707070707070707070707070707070706060606060606060606060606060505050505050505050505050505010303030303030103010103030104040404040404040404040404040606060606060606060606060606050505050505050505050505050504040404040404040404040404040404040404040404040404040404010101030303030302020202010202020202020303030201010102020202020202010303030303030201010101010202020101010201010103030102030101020201010202010101030101030202020102020201010201030302030301010202020101020203030203030301010102020201020303030103030103020202`, img`
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n..............
\n`, [myTiles.transparency16,sprites.castle.tileGrass2,sprites.castle.tileGrass1,sprites.castle.tileGrass3,sprites.vehicle.roadHorizontal,sprites.castle.tilePath2,sprites.castle.tilePath8,sprites.dungeon.hazardWater], TileScale.Sixteen);
     \n   }
       \n return null;
   \n })
\n
  \n  helpers._registerFactory(\"tile\", function(name: string) {
        \nswitch(helpers.stringTrim(name)) {
          \n  case \"transparency16\":return transparency16;
           \n case "Log":
           \n case "tile1":return tile1;
        \n}
       \n return null;
    \n})

\n}
\n// Auto-generated code. Do not edit.,
"tilemap.g.jres": {
    \n\"transparency16\": {
        \n\"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",
        \n\"mimeType\": \"image/x-mkcd-f4\",
        \n\"tilemapTile\": true
    \n},
    \n\"tile1\": {
        \n\"data\": \"hwQQABAAAAAAAPD//////wAA8N7d3d3+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw3t3d3f4AAPD//////w==\",
        \n\"mimeType\": \"image/x-mkcd-f4\",
        \n\"tilemapTile\": true,
        \n\"displayName\": \"Log\"
    },
    \n\"Frogger_Lake1\": {
        \n\"id\": \"Frogger_Lake1\",
        \n\"mimeType\": \"application/mkcd-tilemap\",
        \n\"data\": \"MTAwZTAwMTgwMDAzMDMwMTAyMDIwMTAxMDEwMjAzMDMwMzAzMDMwMzAzMDMwMjAzMDIwMjAyMDIwMjAzMDIwMjAxMDEwMzAzMDMwMzAzMDIwMjAyMDIwMjAyMDIwMTAxMDEwMTAxMDEwMjAyMDEwMTAxMDEwMTAxMDEwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNjA2MDYwNjA2MDYwNjA2MDYwNjA2MDYwNjA2MDUwNTA1MDUwNTA1MDUwNTA1MDUwNTA1MDUwNTAxMDMwMzAzMDMwMzAzMDEwMzAxMDEwMzAzMDEwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDYwNjA2MDYwNjA2MDYwNjA2MDYwNjA2MDYwNjA1MDUwNTA1MDUwNTA1MDUwNTA1MDUwNTA1MDUwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDAxMDEwMTAzMDMwMzAzMDMwMjAyMDIwMjAxMDIwMjAyMDIwMjAyMDMwMzAzMDIwMTAxMDEwMjAyMDIwMjAyMDIwMjAxMDMwMzAzMDMwMzAzMDIwMTAxMDEwMTAxMDIwMjAyMDEwMTAxMDIwMTAxMDEwMzAzMDEwMjAzMDEwMTAyMDIwMTAxMDIwMjAxMDEwMTAzMDEwMTAzMDIwMjAyMDEwMjAyMDIwMTAxMDIwMTAzMDMwMjAzMDMwMTAxMDIwMjAyMDEwMTAyMDIwMzAzMDIwMzAzMDMwMTAxMDEwMjAyMDIwMTAyMDMwMzAzMDEwMzAzMDEwMzAyMDIwMjAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",
        \n\"tileset\": [
            \n\"myTiles.transparency16\",
            \n\"sprites.castle.tileGrass2\",
            \n\"sprites.castle.tileGrass1\",
            \n\"sprites.castle.tileGrass3\",
            \n\"sprites.vehicle.roadHorizontal\",
            \n\"sprites.castle.tilePath2\",
            \n\"sprites.castle.tilePath8\",
            \n\"sprites.dungeon.hazardWater\"
        \n],
        \n\"displayName\": \"Frogger_Strip\"
    \n},
    \n\"*\": {
        \n\"mimeType\": \"image/x-mkcd-f4\",
        \n\"dataEncoding\": \"base64\",
        \n\"namespace\": \"myTiles\"
    \n}
\n},
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
