# Frogger Splash Screen and Movement

```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"/></xml>",
  "main.ts": "\n",
 "images.g.jres": "{\n    \"image2\": {\n        \"data\": \"hwQQABAAAAAA8P////D/AAD/d3f3//cPAH93d3f3dw8Af3d3d3f3DwAfcXd3d3cPAI9xd3d3/w8AH3F3d3cPAAB/d3d3dw8AAH93d3d3DwAAH3F3d3cPAACPcXd3d/8PAB9xd3d3dw8Af3d3d3f3DwB/d3d393cPAP93d/f/9w8A8P////D/AA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Frogger_Jump_Up\"\n    },\n    \"image3\": {\n        \"data\": \"hwQQABAAAAAA/w////8PAPB//393d/8A8Hd/d3d39wDwf3d3d3f3APB3d3cRcfcA8P93d4Fx9wAA8Hd3EXH3AADwd3d3d/cAAPB3d3d39wAA8Hd3EXH3APD/d3eBcfcA8Hd3dxFx9wDwf3d3d3f3APB3f3d3d/cA8H//f3d3/wAA/w////8PAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Frogger_Jump_Down\"\n    },\n    \"image4\": {\n        \"data\": \"hwQQABAAAAD///////D/AH//d3f3//cPd3d3d3f3dw9/d3d3d3f3D3cXcXd3d3cPf49xd3d3/w//H3F3d3cPAAB/d3d3dw8AAH93d3d3DwD/H3F3d3cPAH+PcXd3d/8Pdxdxd3d3dw9/d3d3d3f3D3d3d3d393cPf/93d/f/9w////////D/AA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Frogger_Idle_Up\"\n    },\n    \"image1\": {\n        \"data\": \"hwQQABAAAAAA/w////////B//393d//38Hd/d3d3d3fwf3d3d3d39/B3d3cRcXd38P93d4Fx9/cA8Hd3EXH3/wDwd3d3dzPzAPB3d3d3M/MA8Hd3EXH3//D/d3eBcff38Hd3dxFxd3fwf3d3d3d39/B3f3d3d3d38H//f3d3//cA/w///////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Frogger_Idle_Down\"\n    },\n    \"image5\": {\n        \"data\": \"hwQQABAAAAAAAAD//////wAA/393d//3APB/d3d3d3cA8Hd3d3d39wDwd3cRcXd3APB3d4Fx9/cA8Hd3EXH3/wDwd3d3dzPzAPB3d3d3M/MA8Hd3EXH3/wDwd3eBcff3APB3dxFxd3cA8Hd3d3d39wDwf3d3d3d3AAD/f3d3//cAAAD//////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Frogger_Landing_Down\"\n    },\n    \"image6\": {\n        \"data\": \"hwQQABAAAAD//////wAAAH//d3f3/wAAd3d3d3f3DwB/d3d3d3cPAHcXcXd3dw8Af49xd3d3DwD/H3F3d3cPAAB/d3d3dw8AAH93d3d3DwD/H3F3d3cPAH+PcXd3dw8Adxdxd3d3DwB/d3d3d3cPAHd3d3d39w8Af/93d/f/AAD//////wAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Frogger_Landing_Up\"\n    },\n    \"image8\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAD/AAAAAP8A8CQP///wQg8AL/9O5P/yAPBP4kIkLvQPT/LvS7T+L/Lw9MTu7kxPD/BCzuzO7CQP8P/OTuTs/w9P/M7UTezP9PD0ztRN7E8P8PLiTMQuLw8AL/Tu7k/yAABPD///8PQAAPAAAAAADwAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Spider_Left\"\n    },\n    \"image7\": {\n        \"data\": \"hwQQABAAAAAAAAAPAA8AAAAA//T/8vAAAP9C/ELyTw/wJP//9E8iDwBP4u5OL/8AAPDOzMzuDwAA70zk7Cv+AADv1E3uRPQAAO/UTe5E9AAA70zk7Cv+AADwzszM7g8AAE/i7k4v/wDwJP//9E8iDwD/QvxC8k8PAAD/9P/08AAAAAAPAA8AAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Spider_Down\"\n    },\n    \"image9\": {\n        \"data\": \"hwQQABAAAAAAAPAA8AAAAAAPT/9P/wAA8PQvJM8k/wDwIvRP//9CDwD/8uTuLvQAAPDuzMzsDwAA77LOTsT+AABPRO7UTf4AAE9E7tRN/gAA77LOTsT+AADw7szM7A8AAP/y5O4u9ADwIvRP//9CD/D0LyTPJP8AAA8v/0//AAAAAPAA8AAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Spider_Up\"\n    },\n    \"image10\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAADwAAAAAA8AAE8P///w9AAAL/Tu7k/yAPDy4kzELi8P8PTO1E3sTw9P/M7UTezP9PD/zk7k7P8P8ELO7M7sJA/w9MTu7kxPD0/y70u0/i/y8E/iQiQu9A8AL/9O5P/yAPAkD///8EIPAP8AAAAA/wAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Spider_Right\"\n    },\n    \"image11\": {\n        \"data\": \"hwQQABAAAAAAAAAkQkQAAAAAQE1E/wAAAADUTfQRDwAAQN1E9BEPAABAu7u7/wAAAEBEREQEAAAAQERERAQAAABAREREBAAAAEBEREQEAAAAQERERAQAAABAu7u7CwAAAEDdTUT/AAAAQN1N9BEPAAAA1E30EQ8AAABATUT/AAAAAABERQQAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Car\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myImages\"\n    }\n}",
  "images.g.ts": "// Auto-generated code. Do not edit.\nnamespace myImages {\n\n    helpers._registerFactory(\"image\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"image2\":\n            case \"Frogger_Jump_Up\":return img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. f f f f f f f f f f f f f f . \nf f 7 7 1 8 1 7 7 1 8 1 7 7 f f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \n. f 7 7 7 7 7 7 7 7 7 7 7 7 f . \nf f f 7 7 7 7 7 7 7 7 7 7 f f f \nf 7 7 7 7 f f f f f f 7 7 7 7 f \nf f 7 f 7 f . . . . f 7 f 7 f f \n. f f f f f . . . . f f f f f . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image3\":\n            case \"Frogger_Jump_Down\":return img`\n. . . . . . . . . . . . . . . . \n. f f f f f . . . . f f f f f . \nf f 7 f 7 f . . . . f 7 f 7 f f \nf 7 7 7 7 f f f f f f 7 7 7 7 f \nf f f 7 7 7 7 7 7 7 7 7 7 f f f \n. f 7 7 7 7 7 7 7 7 7 7 7 7 f . \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 1 8 1 7 7 1 8 1 7 7 7 f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \n. f f f f f f f f f f f f f f . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image4\":\n            case \"Frogger_Idle_Up\":return img`\nf f 7 f 7 f f . . f f 7 f 7 f f \nf 7 7 7 7 7 f . . f 7 7 7 7 7 f \nf f 7 7 7 f f f f f f 7 7 7 f f \nf f 7 7 1 8 1 7 7 1 8 1 7 7 f f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \n. f 7 7 7 7 7 7 7 7 7 7 7 7 f . \nf f f 7 7 7 7 7 7 7 7 7 7 f f f \nf 7 7 7 7 f f f f f f 7 7 7 7 f \nf f 7 f 7 f . . . . f 7 f 7 f f \n. f f f f f . . . . f f f f f . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image1\":\n            case \"Frogger_Idle_Down\":return img`\n. . . . . . . . . . . . . . . . \n. f f f f f . . . . f f f f f . \nf f 7 f 7 f . . . . f 7 f 7 f f \nf 7 7 7 7 f f f f f f 7 7 7 7 f \nf f f 7 7 7 7 7 7 7 7 7 7 f f f \n. f 7 7 7 7 7 7 7 7 7 7 7 7 f . \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 1 8 1 7 7 1 8 1 7 7 7 f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf f 7 7 7 7 7 3 3 7 7 7 7 7 f f \nf f 7 7 7 f f 3 3 f f 7 7 7 f f \nf 7 7 7 7 7 f 3 3 f 7 7 7 7 7 f \nf f 7 f 7 f f f f f f 7 f 7 f f \n`;\n            case \"image5\":\n            case \"Frogger_Landing_Down\":return img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . f f f f f f f f f f f f . . \n. f f 7 7 7 7 7 7 7 7 7 7 f f . \n. f 7 7 7 7 7 7 7 7 7 7 7 7 f . \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 1 8 1 7 7 1 8 1 7 7 7 f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf f 7 7 7 7 7 3 3 7 7 7 7 7 f f \nf f 7 7 7 f f 3 3 f f 7 7 7 f f \nf 7 7 7 7 7 f 3 3 f 7 7 7 7 7 f \nf f 7 f 7 f f f f f f 7 f 7 f f \n`;\n            case \"image6\":\n            case \"Frogger_Landing_Up\":return img`\nf f 7 f 7 f f . . f f 7 f 7 f f \nf 7 7 7 7 7 f . . f 7 7 7 7 7 f \nf f 7 7 7 f f f f f f 7 7 7 f f \nf f 7 7 1 8 1 7 7 1 8 1 7 7 f f \nf 7 7 7 1 1 1 7 7 1 1 1 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf 7 7 7 7 7 7 7 7 7 7 7 7 7 7 f \nf f 7 7 7 7 7 7 7 7 7 7 7 7 f f \n. f 7 7 7 7 7 7 7 7 7 7 7 7 f . \n. f f 7 7 7 7 7 7 7 7 7 7 f f . \n. . f f f f f f f f f f f f . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image8\":\n            case \"Spider_Left\":return img`\n. . . . . f . . . f . . . . . . \n. . f . f 4 f f f 4 f f . . . . \n. f 4 f f 2 4 2 f c 4 2 f f . . \n. f 2 2 4 f f 4 f f f f 2 4 f . \n. . f f 2 f 4 e e e e 2 4 f . . \n. . . f e e c c c c c e f . . . \n. . f e 2 b e c e 4 4 c e f . . \n. . f 4 4 4 e e 4 d d 4 e f . . \n. . f 4 4 4 e e 4 d d 4 e f . . \n. . f e 2 b e c e 4 4 c e f . . \n. . . f e e c c c c c e f . . . \n. . f f 2 f 4 e e e e 2 4 f . . \n. f 2 2 4 f f 4 f f f f 2 4 f . \n. f 4 f f 2 4 2 f c 4 2 f f . . \n. . f . f 2 f f f 4 f f . . . . \n. . . . . f . . . f . . . . . . \n`;\n            case \"image7\":\n            case \"Spider_Down\":return img`\n. . . . . . . . . . . . . . . . \n. . . f . . . . . . . . f . . . \n. . f 4 f . f f f f . f 4 f . . \n. . f 2 4 f e e e e f 4 2 f . . \n. f 2 f 2 e c 4 4 c e 2 f 2 f . \n. f 4 f e c 4 d d 4 c e f 4 f . \nf 4 c f e c 4 d d 4 c e f c 4 f \n. f f f e c e 4 4 e c e f f f . \n. f 2 4 e c c e e c c e 4 2 f . \n. f 4 f 4 c e e e e c 4 f 4 f . \nf 2 2 f f e b 4 4 b e f f 2 4 f \n. f f 4 2 e 2 4 4 2 e 2 4 f f . \n. . f 2 f f e 4 4 e f f 2 f . . \n. f 4 2 f . f f f f . f 2 4 f . \n. . f f . . . . . . . . f f . . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image9\":\n            case \"Spider_Up\":return img`\n. . . . . . . . . . . . . . . . \n. . f f . . . . . . . . f f . . \n. f 4 2 f . f f f f . f 2 4 f . \n. . f 2 f f e 4 4 e f f 2 f . . \n. f f 4 2 e 2 4 4 2 e 2 4 f f . \nf 4 2 f f e b 4 4 b e f f 2 2 f \n. f 4 f 4 c e e e e c 4 f 4 f . \n. f 2 4 e c c e e c c e 4 2 f . \n. f f f e c e 4 4 e c e f f f . \nf 4 c f e c 4 d d 4 c e f c 4 f \n. f 4 f e c 4 d d 4 c e f 4 f . \n. f 2 f 2 e c 4 4 c e 2 f 2 f . \n. . f 2 4 f e e e e f 4 2 f . . \n. . f 4 f . f f f f . f 4 f . . \n. . . f . . . . . . . . f . . . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image10\":\n            case \"Spider_Right\":return img`\n. . . . . . f . . . f . . . . . \n. . . . f f 4 f f f 4 f . f . . \n. . f f 2 4 c f 2 4 2 f f 4 f . \n. f 4 2 f f f f 4 f f 4 2 2 f . \n. . f 4 2 e e e e 4 f 2 f f . . \n. . . f e c c c c c e e f . . . \n. . f e c 4 4 e c e b 2 e f . . \n. . f e 4 d d 4 e e 4 4 4 f . . \n. . f e 4 d d 4 e e 4 4 4 f . . \n. . f e c 4 4 e c e b 2 e f . . \n. . . f e c c c c c e e f . . . \n. . f 4 2 e e e e 4 f 2 f f . . \n. f 4 2 f f f f 4 f f 4 2 2 f . \n. . f f 2 4 c f 2 4 2 f f 4 f . \n. . . . f f 4 f f f 2 f . f . . \n. . . . . . f . . . f . . . . . \n`;\n            case \"image11\":\n            case \"Car\":return img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . 4 4 4 4 4 4 4 4 4 4 . . . \n. . 4 d b 4 4 4 4 4 b d d 4 . . \n. 4 d d b 4 4 4 4 4 b d d d 4 . \n4 d d 4 b 4 4 4 4 4 b d d d d 4 \n2 4 4 4 b 4 4 4 4 4 b 4 4 4 4 4 \n2 4 4 4 b 4 4 4 4 4 b 4 4 4 4 5 \n4 4 f f b 4 4 4 4 4 b 4 f f 4 4 \n4 f 1 1 f 4 4 4 4 4 b f 1 1 f 4 \n4 f 1 1 f . . . . . . f 1 1 f . \n. . f f . . . . . . . . f f . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`;\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"animation\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"song\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n",
"tilemap.g.jres": "{\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAAAAPD//////wAA8N7d3d3+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw7u7u7v4AAPDu7u7u/gAA8O7u7u7+AADw3t3d3f4AAPD//////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"Log\"\n    },\n    \"Frogger_Lake1\": {\n        \"id\": \"Frogger_Lake1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwZTAwMTgwMDA4MDgwODA4MDgwODA4MDgwODA4MDgwODA4MDgwMzAzMDMwMjAzMDIwMjAyMDIwMjAzMDIwMjAxMDEwMzAzMDMwMzAzMDIwMjAyMDIwMjAyMDIwMTAxMDEwMTAxMDEwMjAyMDEwMTAxMDEwMTAxMDEwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNTA1MDUwNTA1MDUwNTA1MDUwNTA1MDUwNTA1MDYwNjA2MDYwNjA2MDYwNjA2MDYwNjA2MDYwNjAxMDMwMzAzMDMwMzAzMDEwMzAxMDEwMzAzMDEwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDUwNTA1MDUwNTA1MDUwNTA1MDUwNTA1MDUwNTA2MDYwNjA2MDYwNjA2MDYwNjA2MDYwNjA2MDYwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDAxMDEwMTAzMDMwMzAzMDMwMjAyMDIwMjAxMDIwMjAyMDIwMjAyMDMwMzAzMDIwMTAxMDEwMjAyMDIwMjAyMDIwMjAxMDMwMzAzMDMwMzAzMDIwMTA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDkwOTA5MDkwOTA5MDkwOTA5MDkwOTA5MDkwOTAxMDIwMTAzMDMwMjAzMDMwMTAxMDIwMjAyMDEwMTAyMDIwMzAzMDIwMzAzMDMwMTAxMDEwMjAyMDIwMTAyMDMwMzAzMDEwMzAzMDEwMzAyMDIwMjAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"sprites.castle.tileGrass2\",\n            \"sprites.castle.tileGrass1\",\n            \"sprites.castle.tileGrass3\",\n            \"sprites.vehicle.roadHorizontal\",\n            \"sprites.castle.tilePath2\",\n            \"sprites.castle.tilePath8\",\n            \"sprites.dungeon.hazardWater\",\n            \"sprites.dungeon.darkGroundCenter\",\n            \"sprites.skillmap.islandTile4\"\n        ],\n        \"displayName\": \"Frogger_Strip\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"Frogger_Strip\":\n            case \"Frogger_Lake1\":return tiles.createTilemap(hex`0e001800080808080808080808080808080803030302030202020202030202010103030303030202020202020201010101010102020101010101010107070707070707070707070707070707070707070707070707070707070707070707070707070707070705050505050505050505050505050606060606060606060606060606010303030303030103010103030104040404040404040404040404040505050505050505050505050505060606060606060606060606060604040404040404040404040404040404040404040404040404040404010101030303030302020202010202020202020303030201010102020202020202010303030303030201040404040404040404040404040404040404040404040404040404040909090909090909090909090909010201030302030301010202020101020203030203030301010102020201020303030103030103020202`, img`\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n..............\n`, [myTiles.transparency16,sprites.castle.tileGrass2,sprites.castle.tileGrass1,sprites.castle.tileGrass3,sprites.vehicle.roadHorizontal,sprites.castle.tilePath2,sprites.castle.tilePath8,sprites.dungeon.hazardWater,sprites.dungeon.darkGroundCenter,sprites.skillmap.islandTile4], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"transparency16\":return transparency16;\n            case \"Log\":\n            case \"tile1\":return tile1;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n",
"pxt.json": "{\n    \"name\": \"Frogger Clone 12-1-2023\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"images.g.jres\",\n        \"images.g.ts\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"target\": \"1.12.41\",\n        \"targetId\": \"arcade\"\n    },\n    \"supportedTargets\": [\n        \"arcade\"\n    ],\n    \"preferredEditor\": \"blocksprj\"\n}\n"
}
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
game.splash("Welcome to A Frogger Clone")
```

## Step 2

Now that we have a splash screen to greet players, let's add our Frogger!

 Go get a ``||variables:set mySprite to||`` block from ``||sprites:Sprites||``. 
 Add this below the ``||game:splash "___"||`` block.
 
 Click on the grey image in the block to add the provided sprite 
 or to open the Image Editor, and draw an image for your sprite. 
 You can also use one of the provided frog sprites in **My Assets**.

 ```blocks
game.splash("Welcome to A Frogger Clone")
 let mySprite = sprites.create(assets.image`Frogger_Idle_Down`, SpriteKind.Player)
 ```

## Step 3

Pull out a ``||sprites:set mySprite stay in screen||`` block and add it to the bottom. 
Click the slider button to make it say **ON**.

```blocks
game.splash("Welcome to A Frogger Clone")
let mySprite = sprites.create(assets.image`Frogger_Idle_Down`, SpriteKind.Player)
mySprite.setStayInScreen(true)
```

## Step 4

Now let's make the sprite move! Find the ``||controller:ControllerButtonEvent||`` block
in ``||controller:Controller||``. Pull out a total of four for each direction on the gamepad.

In **MakeCode** sprites are 16x16 pixels, so we need to add 
or subract 16 pixels for each button pressed for our movement.

```blocks
game.splash("Welcome to A Frogger Clone")
let mySprite = sprites.create(assets.image`Frogger_Idle_Down`, SpriteKind.Player)
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

## Complete

That's it. You've got Frogger moving around. You're awesome!
