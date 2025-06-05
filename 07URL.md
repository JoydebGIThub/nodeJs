## URL
- We can modify or create our URL as required:
```js
import url from "node:url";
const myURL = new URL("https://example.org");
myURL.pathname = "/a/b/c";
myURL.search = "?d=e";
myURL.hash = "#fgh";

console.log(myURL);
console.log(myURL.href); //https://example.org/a/b/c?d=e#fgh

```
