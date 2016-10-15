# earthbound
Offers various implementations of Earthbound-related stuff

This repository is a collection of implementations that are related to the Earthbound (Mother 2) franchise.
## Installation
```bash
$ npm i -S earthbound
```
## Usage
This example renders Earthbound's battle backgrounds in your browser.
```js
import { BattleBackgrounds } from "earthbound";
const { BackgroundLayer, Engine } = BattleBackgrounds;
/* Create two layers */
const layer1 = new BackgroundLayer(153);
const layer2 = new BackgroundLayer(298);
/* Create animation engine  */
const engine = new Engine([layer1, layer2], {
	canvas: document.querySelector("#target-canvas");
});
engine.animate();
```