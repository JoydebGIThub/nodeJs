## Path module
- import path
```js
const path= require('path')
```
- print the base name from a url
```js
const a = path.basename("C:\\temp\\myfile.html");
console.log(a);
```

- print the directory name from a url
```js
const a2 = path.dirname("C:\\temp\\myfile.html");
console.log(a2);
```

- get the current file extention
```js
const a3 = path.extname(__filename);
console.log(a3);
```




