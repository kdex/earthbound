# earthbound
Offers various implementations of Earthbound-related stuff

This repository is a collection of implementations that are related to the Earthbound (Mother 2) franchise.

## Installation
```bash
$ npm install -S earthbound
```

## Usage
This example renders Earthbound's battle backgrounds in your browser.
```js
import { BattleBackgrounds } from "earthbound";
const { initialize, BackgroundLayer, Engine } = BattleBackgrounds;
(async () => {
    await initialize();
    /* Create two layers */
    let bgLayer1 = new BackgroundLayer(153);
    let bgLayer2 = new BackgroundLayer(298);
    /* Create animation engine  */
    let engine = new Engine([bgLayer1, bgLayer2], {
        canvas: document.querySelector("#target-canvas");
    });
    engine.animate();
})();
```
