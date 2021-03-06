# One Hour Text Game Engine

A small wrapper for [xterm.js](https://xtermjs.org/) to make small terminal games using a trivial API. [Docs available here](https://mkalam-alami.github.io/ohtge/docs/).

## Example `game.js` file

```javascript
/// <reference path="node_modules/ohtge/lib/ohtge.d.ts" />

title("test.exe")
loop()

async function loop() {
    while (1) {
        write("Hello world")
        color("yellow")
        const a = await input("Say something?") // `input(string, callback)` syntax also supported
        color("white")
        write("You said " + a)
        write()
        await pause()
    }
}
```

![](https://raw.githubusercontent.com/mkalam-alami/ohtge/master/lib/ohtge-readme.gif)

## Simple setup

1. Download the [zip](https://github.com/mkalam-alami/ohtge/archive/master.zip)
2. Only keep the files you want (typically `dist/` + one of the examples)
3. Make a game!

## Setup from scratch

1. `npm install ohtge` *(Optional, only used as reference for IDE auto-completion)*
2. Insert the following HTML in your web page:

```html
<div class="ohtge-window cloaked">
    <div class="ohtge-title"></div>
    <div class="ohtge-terminal"></div>
</div>

<script src="https://cdn.jsdelivr.net/npm/ohtge"></script>
<script src="[ YOUR OWN GAME SCRIPT ]"></script>
```

3. Insert the following at the top of your own script (either JS or TS):

```javascript
/// <reference path="node_modules/ohtge/lib/ohtge.d.ts" />

write('Hello world!');
```

## Complete API

[![](https://i.imgur.com/mF5Yehw.png)](https://mkalam-alami.github.io/ohtge/docs/)

## Made with ohtge

* ["freeze.exe"](https://marwane.kalam-alami.net/1hgj/286/) (1HGJ 286 entry, 2020)
* ["prince.exe"](https://marwane.kalam-alami.net/jams/alakajam-k5/) (5th Kajam entry, 2018)
* ["monster.exe"](https://marwane.kalam-alami.net/1hgj/167/) (1HGJ 167 entry, 2018)
* ["Day Off Work"](https://marwane.kalam-alami.net/misc/dayoffwork/) (web port of a 1st Alakajam! entry, 2018)
