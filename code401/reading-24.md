# Intro to React

React is a js library built to simplify the creation of user interfaces and allow for the creation of single page application, reducing the number of times the client side must talk to the server side. One of the main points, is how the UI is divided into components.

JSX, Javascript XML, allows the coder to write html in js. It is not required for React, but they pair well together.
examples:
- `const element = <h1>Hello, world!</h1>;`
- ```
   const name = 'Josh Perez';
   const element = <h1>Hello, {name}</h1>;

   ReactDOM.render(
     element,
    document.getElementById('root')
   );
  ```

  - using string literals to set attributes
    - `const element = <div tabIndex="0"></div>;`
    - `const element = <img src={user.avatarUrl}></img>;`

- `ReactDOM.render()` is used to render an object to the page. The coder can use Jquery to find a node to attach it too.

- Once a react object has been rendered, it cannot be updated. If an element needs to be updated, it can only be replaced.
- Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
- a component can be made using a function 
```
   function Welcome(props) {
    return <h1>Hello, {props.name}</h1>;
   }
```
- or a class
```
     class Welcome extends React.Component {
        render() {
       return <h1>Hello, {this.props.name}</h1>;
        }
     }
```

- an interesting feature of React is that the coder can create custom components `const element = <Welcome name="Sara" />;`
- a custom component can be defined using a function
```
   function Welcome(props) {
     return <h1>Hello, {props.name}</h1>;
   }

   const element = <Welcome name="Sara" />;
   ReactDOM.render(
    element,
    document.getElementById('root')
    );
```

