**REACT JS:**
MVC(Model View Control);
- NodeJS is Framework and ReactJS is library...
V in MVC is ReactJS
- React implements a virtual DOM that is basically a DOM tree representation in JavaScript. 

**prerequisites:**
html,css,classes in javascript, NodeJS

- Object, class, methods
-class has constructors(initialize the objects) and functions(reusable code)

`class Class_name {  
}
var var_name = new Class_name {  
}`

**ES6 also supports inheritance:**

`child_name extends parent_name`

- In javascript the value of `this` keyword is dependednt on how it is called and it does nt always represent the object reference of current object(unlike other programming languages.

-If the script is in strict mode, this refers to undefined, so `console.log()` will return an error.

- to embed any javascript object into `JSX` we need to write it in curly braces

- Attributes in JSX: these are different from traditional html attributes and follow camelCase naming convention...
ex. class=>className, this is because some attributes in html are keywords in JSX and can cause ambiguity...

- ECMA(European Computer Manufacturers Association) Script is standard for Scripts like javaScript...


<img src="https://user-images.githubusercontent.com/121226686/210417703-1c22408b-88e9-4aad-be09-d5982e99d7a6.png" width="500" height="250" />

- bABEL COMPILER USES `POLYFILL TECHNIQUE` AND backward compiles the new JS6 program. It is also known as transplier. 
*(a transpiler as the transpiler converts source code into another source code at the same abstraction level, whereas the compiler converts code into a lower level code generally. )*

- **ReactDOM :** import ReactDOM from `react-dom`
- <img src="https://user-images.githubusercontent.com/121226686/210418930-364731b0-fc99-478a-a58f-e5d25c877c3c.png" width="500" height="100" />


`ReactDOM.render(element, container, callback)`
`ReactDOM.findDOMNode(component)`
`ReactDOM.unmountComponentAtNode(container)`--->used to unmount already rendered component
`ReactDOM.hydrate(element, container, callback)`---> same as render but used in serverside rendering 
`ReactDOM.createPortal(child, container)`
- npm (node package manager)
- 

-We use `call, bind and apply` methods to set the `this` keyword independent of how the function is called. This is especially useful for the callbacks 
-functions can act as objects in javascript
`ex. function greeting() {
  console.log('Hello World');
}greeting.lang = 'English';// Prints 'English'
console.log(greeting.lang);`

-The difference between `call()` and `bind()` is that the `call()` sets the this keyword and executes the function immediately and it does not create a new copy of the function, 
while the `bind()` creates a copy of that function and sets the this keyword.
`apply()` function will act like call() but accepts array as a parameter and not comma seperated values

- Every browser has JavaScript Engine which is embedded into browsers, for example, *Chrome has a V8 engine and Mozilla Firefox has SpiderMonkey.*

-

`function greeting(lang) {
  console.log(${lang}: I am ${this.name}
);}const john = {
  name: 'John'
};const jane = {
 name: 'Jane'
};`
`const greetingJohn = greeting.bind(john, 'en');`
`greetingJohn();const greetingJane = greeting.bind(jane, 'es');`
`greetingJane();*/`

`function.call(thisArg, arg1, agr2, ...)` 

component based front end library.
it can be used to create SPA single page application and MPA Multipage apps

-UI to improve the speed of apps
- It uses virtual DOM(Document Object Model)
- Tree data structure
- saves elements(components) of react as nodes. This makes easy to target and modify the node and not the entire object. It also helps in avoiding the full page rerendering and renders only what is required to be rendered. This makes *ReactJS* a lot faster than other front end SPA frameworks/libraries.
-  **{ The process without react
  The browser parses the HTML to find the node with this id.
It removes the child element of this specific element.
Updates the element(DOM) with the ‘updated value’.
Recalculates the CSS for the parent and child nodes.
Update the layout.
Finally, traverse the tree and paint it on the screen(browser) display.
}**
**With ReactJS in work
{
it maintains a lightweight copy of actual DOM with elements as it's nodes
everytime some update comes it creates the copy of original DOM and compares with the pre-updateDOM this is called 'diffing' process
Then react sends all this changes to real DOM in batches rather than one by one 
This reduces re-rendering of actual DOM from n times to just one time as all the changes are already known while 'diffing'
THE PROCESS OF BATCH TRANSFERRING IS KNOWN AS `RECONCILATION`

}**
{Code splitting is left for later read when you get time}

**this is from the handwritten notes**
- JavaScript virtual DOM is faster than the traditional use
- npm install create-react-app is a tool for better developing environment and no need to build all from scratch
- install nodejs, npm, react

- react will mount the app in *index.html* by default..this `div` has `id="root"`

- src has App.js, App.css, index.js
App.js renders everything on the react page

- package.json and package-lock.json

-React Features: JSX is javascript extension with the html
it is also known as XML like syntax

- React app has multiple components which are added in App.js---> which further renders it on index.html

- It has one way data binding --> better performance no additional requirements

- The changes are re-rendered in virtual DOM and the origial page only renders the components which are actually changed

- Simple to use and learn

- ADV: easy to develop, faster than others, reusable components, It is SEO(Search Engine Optimisation) friendly, 

- Dis: pace deflects learning, poor documentation,
 need help of other tools for connections, JSX is a barrier,

- ReactJS is used for developing web based apps and ReactNative is used to develop mobile apps UI

- We can give the attributes in return() html components as 
String literals ex. `<h1 name="nm"></h1>`
an be given as expressions `using {}: ex.<h1 Style=mystyle}`>abc</h1>`

- Types of React Component: functional component, Class COmponent

- class component: need to extend from React.component

`import eact, {Component} from 'react';
class Abc extends Component{
render(){
return({
<div>
</div>

});
}
}`
 
`export default app;`


- functional components: also known as stateless components

`function Abc(){
return (
<div>
</div>
);
}`
- React State: It holds synchronous variables

-updated structure according to the user action on the page displayed...methods available for state getInitialState() and setState() . setState re-renders the page

-props: these are arguments passed to the function , in react these are the arguments passed into html tag as input arguments


### ------------------------------------------------------



**this is from the videos of react**
functional component:
`const Abc =()=>{
return(
html page to return or JSX syntax
)
}`

get the data in child using parent 

`const Abc({song}){
return (JSX)
}

const AbcParent(){
return(
songs.map((s)=>
<Abc song={s}/>)
);
}`

- props and state

-props are readonly values passed from parent to child
-state changes the value of the declared state inside the react component
- react hooks are used to catch the values according to requirement

useState,useHistory, useLocation

are some of the hooks

`import {useState} from 'react';
const [count,setCount] = useState(0);`
*here the value of count is state and inside the react component and can be modified using the useState's setState(count+1) or any other desired logic*

**create-react-app**
`npm i create-react-app
npx create-react-app myapp
npm start`

`ReatctDOM.render(<React.StricMode><App/><React.StricMode>
, document.getElementById('root'));`

*yarn and npm are both package managers. yarn is better than the npm*
-

- Folder Structure

1.public
a.favicon.ico
b.index.html
c.manifest.json
2.src
a.components
b.App.js
c.index.js
d.
3.package.json

### ---------------------------------------------------

New component= new js file inside components folder in src....import that folder into the app.js

>- per component we will have one css and one js file
>- clean code seperation is attained with create-react-app

- if we want to get the info from a text box we need to do the two way binding and write a function to catch the changing value. This can be achieved using `onChange` event of the textbox
- `onChange` will pass an event to the function and the calue inside the textbox can be retrieved by using the  `event.target.value`

`const MyComponent=()=>
{
const changedValue=(event)=>
{Console.log(event.target.value");
}`

`return(
<input type="text" name="myip" onChange={changedValue}> Name</input>)
}`

-Routing in the react app

*Router (react-router-dom)(react-router)
Switch
Route*

Auto import extension
auto rename tag extension
react-router : 
react-router-dom : BrowserRouter, Link, Route, Switch


***Add from here next
write a functional components in component folder in src
do not forget to keep the first letter capital and follow camelcasing
also export default *Appname*

`<BrowserRouter>
<link to="/home"> Home <Link>
<Switch>
<Route path="/home" component={Home}/>

</Switch>
</BrowserRouter>`

- Rest API <---->dbs
```npm i express multer cors crypto-js mysql2```

- create dbs, tbl, serveer, middleware axios, react
-While writing express always follow steps :
**import** - crypto-js,express,body-parser(now it is integrated with the express package)

**middleware** - bodyparser, routes middleware (or) folder of routes,  
**start server**

- create database connection seperate
- keep the routers seperate
- jwt??????
### -------------------------------------------------






### ---------------------------------------------------




