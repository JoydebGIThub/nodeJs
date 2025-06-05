## Import in nodejs:
- create a 2nd js and declare an `object` inside the js
```js
joydeb = {
  name: "Joydeb",
  favNum: 3,
  developer: true,
};
module.exports = joydeb
```
- import the 2nd js in index.js and export the 2nd.js every thing using `module.exports`
```js
const lov = require("./second");
console.log("Hello world", lov);
```
- This type of code system is called `common js module`

## Module wrapper function
- All the modules in node js automatially wrap in a function
- when a module run in a nodejs before everything the node js wrap the module inside the function
```js
(function(exports, require, module, __filename, __dirname){
joydeb = {
  name: "Joydeb",
  favNum: 3,
  developer: true,
};
module.exports = joydeb;
})
```

- we can also check all the parameters details:
```js
console.log(exports, require, module, __filename, __dirname);
```


