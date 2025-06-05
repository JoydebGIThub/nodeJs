## The difference of frontend and backend
|Client            | Server        |
|------------------|---------------|
|user              |A server is a computer or software that provides `services, data, or resources` to other computers, known as clients, over a network. This architecture is called the client-server model.|
|User is send the request to the server| Server will process it and then provide it to the client|
|It's called as frontend | It's called as backend|
|Request can view the response in there system | In server site there is a whole team who will maintain the server |

## Node Js
- Node js will fit in the `backend` and It will use the JS for backend also.
- In the place of node js there can be **php, django, Flask, Rails** but when we use node js we only need to use the `js`.
- In 2009 Ryan Dahl was use the **V8 engine of chrome**(which is responsible for running the js) in c++ and create a executable `node.exe`. We can run that anywhere like in our computer and the server.
- So node js is a javaScript which will executed on server.
- It's an `runtime environment` for JS which is run on server.

## Install the nodejs and VS code.
- We can change the theme of VS code (JellyFish Theme)

### Code:
```js
console.log("Hello world");
```

```terminal
node index.js
node index
```
## Non-blocking io model
- In js `single thread can manage multiple connection`, it is possible for `non-blocking io model`.
- When we `run the node js on server` then a particular thread can handle multiple connection `simultaneously`.
- If a client request come and that time you communication with another server or you run some process that is i/o bound and it is waiting for input output or any data from the database then also it will not block the thread, it will just waiting for a call back funtion, and an event will be fire when the I/O call end.
- So, by this multiple connection can be handle simultaneously through node js
- If we compare it with a multithreaded application, then node js will be faster if the request is so much I/O blocking then it will be faster.
- For that node js is used for `real time chat applications`, `video calling applications`.

## NPM
- Check the version
```terminal
node --version
npm --version
```
- npm -> node package manager
- It will help us to install packages

### NPM comments
- Initialize a js as `node project`
  - 1st: initialize the project by `npm init`
    - Give the package name.
    - Chose the `version`
    - give a description
    - entry point
    - then skip until author
    - give the name of the author
    - License entre
    - Then yes
    - Then a package.json will be created (all the details about the project)

- Want to install the project express or angular cli (packages for node js)
  - install the package `npm install express --save`
  - after the installation done the `package.json` also updated
  - a dependencies `express` will be added
  - also a `node modules` folder will be added
  - **Important**: When we distribute the application then we don't give the `node modules` folder also when we push the application to the `git hub` we don't push the `node modules` folder because the folder is heavy
  - **node modules** has all the dependency downloaded from the internet came here and then we can use it.
 
- Want to install the node modul globally in the system
  - we use `npm i -g nodemon`
  - after install use it `nodemon index.js`
  - So, after it if we change something in the file `index.js` and save it will automatically show the result in the terminal
  - It will be helpfull when we work on `http server`
 
- Install the angular cli
  - install it `npm i @angular/cli`
 
### Dev Dependency:
- Some dependency we want to use only when development like `nodemon`
  - We can open a terminal and run `npm install --save-dev nodemon`
  - after that it will add as a `devDependencies`
  - we also uninstall `nodemon` just run `npm uninstall nodemon`

## Package-lock.json
- Whole dependency tree is present here
- So when we add any dependency then that dependencies can have dependencies that all was install and store in the node modules and the dependencies are mentioned in the `package-lock.json`.
- In `package.json` has the dependency i added and in `package-lock.json` has all the dependecies as tree like structures








