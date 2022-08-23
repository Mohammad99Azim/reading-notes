# React

### Hello World

```
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<h1>Hello, world!</h1>);
```

It displays a heading saying “Hello, world!” on the page.


### JSX

``const element = <h1>Hello, world!</h1>;``

This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.




### Rendering Elements

An element describes what you want to see on the screen:

``const element = <h1>Hello, world</h1>;``

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

**Rendering an Element into the DOM**

Let’s say there is a <div> somewhere in your HTML file:

  ``<div id="root"></div>``
  
  
 We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element, first pass the DOM element to ReactDOM.createRoot(), then pass the React element to root.render():

```
const root = ReactDOM.createRoot(
  document.getElementById('root')
);
const element = <h1>Hello, world</h1>;
root.render(element);
 ```

 ### Components and Props
  
  **Function and Class Components**
  
The simplest way to define a component is to write a JavaScript function:
 ```
  function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
 ```
  
  This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element.
  
  We call such components “function components” because they are literally JavaScript functions.
  
  
  You can also use an ES6 class to define a component:
  
  ```
  class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
  ```
  
  The above two components are equivalent from React’s point of view.
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
