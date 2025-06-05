## File system module:
- import the fs:
```js
const fs = require('fs/promises');
```

- read the file has a call back function with `error` and `data`
```js
const fs = require("fs");

fs.readFile("file.txt", "utf8", (err, data) => {
  console.log(err, data);
});

```
- it will print `null and the content inside the file`
- if the file is not present in the folder then we will get the error
- if we write a log after the readfile funtion then that will be print before the `console.log(err, data);`
```js
const fs = require("fs");

fs.readFile("file.txt", "utf8", (err, data) => {
  console.log(err, data);
});
console.log("Finished reading file");
```
### Output:
```
Finished reading file
null this is a file
```
### Explaination:
- in the `fs.readFile` the file must called `file.txt` but the `call back function` will be called when the file content will be fully read.
- so the reading file and run the call back can take time so the node js differ the things and don't block the path it will let execute the next part and the print the call back after the file read complete, because node js work on `non blocking I/O model`

## readFileSync
- It will `intensionaly block the path` and until the file read complete it won't execute further
```js
const a = fs.readFileSync("file.txt");
console.log(a); // stream
console.log(a.toString()); // to see the content

console.log("Finished reading file");
```
### Output:
```
<Buffer 74 68 69 73 20 69 73 20 61 20 66 69 6c 65>
this is a file
Finished reading file
```

## Write file
- for write file we have something called `writeFile`
```js
fs.writeFile("file.txt", "This is a data", () => {
  console.log("Written to the file");
});
console.log("Finished writing file");
```



