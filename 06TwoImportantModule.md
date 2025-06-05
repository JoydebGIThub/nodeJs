## CommonJS modules:
```js
const circle = require('./circle.js');
```
- moduleSecond.js
```js
function simple() {
  console.log("Simple");
}
module.exports = simple;
```
- moduleFirst.js
```js
const simple = require("./moduleSecond");
simple();
```

## ECMAScript modules:
```js
import {addTwo} from `./addTwo.mjs`
```
- for use this module in js we need to use the `.mjs` extension so that node js will understand that we are going to use the ECMAScript modules
- if the file extension has `.mjs` then we cann't use **module.export** to import it
- To use the ES6 we need to add `"type":"module"` in package.json
```js
export function simple() {
  console.log("ECMAScript simple");
}

```
```js
import { simple } from "./moduleThird.mjs";
simple();
```
### If we try to call  simple without the {} then we will get an error
- To resolve that we need an default export in the other file then we can call that default by any name no need to mention the same funtion name which we export
```js
export function simple() {
  console.log("ECMAScript simple");
}

export default function simple2() {
  console.log("ECMAScript simple default");
}

```

```js
import simple63 from "./moduleThird.mjs";
simple63();
```
#### Output:
```
ECMAScript simple default
```
- We also import all the function in the by using *
```js
import * as aj from "./moduleThird.mjs";
```

