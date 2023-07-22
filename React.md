Use ```ReactDOMServer.renderToString(<App />)``` to render a React component on the server instead of client
## JSX
<a href="https://www.freecodecamp.org/news/what-is-state-in-react-explained-with-examples/">State Explanation</a>
<br />
<a href="https://stackoverflow.com/questions/27991366/what-is-the-difference-between-state-and-props-in-react" target="_blank">State vs. Props</a>
<br />
<a href="https://stackoverflow.com/questions/36097965/when-to-use-es6-class-based-react-components-vs-functional-es6-react-components" target="_blank">
Function or Class Components?</a>
```
use 'ctrl + /' as shortcut to add comment
{/* try to minimize statefulness */}
{/* all HTML attributes and event references become camelCase (class => className, onclick => onClick) */}
{/* all elements must be closed (<br> => <br />) */}
{/* use curly braces {} to include JavaScript within JSX */}
ReactDOM.render(componentToRender, targetContainerNode)
React.createElement(type, props, ...children) // this is what JSX is converted to when compiled
```
### React Notes
- <i>Unidirectional data flow</i> (state flows in one direction down the component tree)
- Separate state logic from UI logic (maybe you only need one stateful component?)
- 

### React Lifecycle
- place API calls in componentDidMount()
- add event listeners for the document and window object in componentDidMount()
  - click is the event
  - onClick is the event listener
  - handleClick is the event handler
  - document.addEventListner("click", this.handleClick);
- remove event listeners in componentWillUnmount()
- .
- use shouldComponentUpdate(nextProps, nextState) -> bool to determine if component should update based on next props and state


### Event Listener
[why handleClick instead of handleClick()](https://stackoverflow.com/questions/64943885/why-does-a-react-jsx-element-event-handler-not-use-parentheses-similar-to-a-html)
```
handleClick(e) {}

... onclick={this.handleClick} ...
=== equivalent to
element.addEventListener("click", this.handleClick)
```

### Create Stateful Components
```
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: "Leo"
    }
    this.handleClick = this.handleClick.bind(this);      // explicitly bind this to the handleClick method
  }

  
  // never modify state directly; always use this.setState(); accepts object or function as the argument
  // To fix asynchronus state updates, use a second form of setState() that accepts a callback function rather than an object.
  // That function will receive the previous state as the first argument, and the props at the time the update is applied as the second argument:

  handleClick() {
    this.setState((prevState, props) => ({        // or this.setState(function(prevState, props) {return {...}})
      name: "Leo Ren",
      count: preState.count + 1;
    }));
  }
  
  render() {
    const name = this.state.name;
    return (
      <div>
        <button onClick={this.handleClick}>Click Me!</button>
        <h1>{ name }</h1>
      </div>
    );
  }
}
```

### Pass props to stateless functional components 
- (props: type of object that stores the value of attributes of a HTML tag)
- You can pass props to child components
```
const ChildComponent = (props) => {
  ...
    { props.date }
    // use { this.props.date } if ChildComponent is a class component
  ...
}

class Parent extends React.Component {
  ...
    <ChildComponent date={Date()} />    // pass a date prop
  ...
}

ChildComponent.defaultProps = {         // create default props
  date: Date()
}

ChildComponent.propTypes = {            // type checking for props (TypeScript?)
  handleClick: Proptypes.func.isRequired
}
```

### create stateless functional components
```
{/* function names in CapitalCamelCase */}
const ChildComponent = function () {
  return (
    <div />
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <ChildComponent />
      </div>
    );
  }
}
```

---
## HTML DOM (Document Object Model) - constructed as a tree of objects(or nodes)
Lets you access and change all the elements in an HTML document

### Events
[DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)

### Methods
```
document.getElementById()
document.getElementByClassName()
document.createElement()

document.getElementById(id).onclick = function(){code}
```
### Properties
```
.innerHTML = new html content
.attribute
.style.property
```

---
## Random
[function scope](https://stackoverflow.com/questions/33040703/proper-use-of-const-for-defining-functions)
- using const before a function declaration makes it a function expression
- this means the function is not hoisted to the top and now has block scope instead of full lexical scope
  
[Understand Callbacks and Event Listeners](https://dev.to/i3uckwheat/understanding-callbacks-2o9e)
- callbacks are functions passed into other functions as arguments
- so declaring callbacks are the same syntax as declaring regular functions,
- the parameters in the callbacks (like e or prevState) are passed into another function (like .addEventListener) as arguments
- (so in the implementation of .addEventListener, the callback is called/executed with event as the argument)
- (we need to know what the callback is using as the arguments so we can write the callback with the correct parameter names)
```
++a is equivalent to a += 1
be careful with a++
```

```
// evaluate string as math expression?
function addbits(s) {
    return (s.replace(/\s/g, '').match(/[+\-]?([0-9\.]+)/g) || [])
        .reduce((sum, value) => parseFloat(sum) + parseFloat(value));
}
```

### Conditionals in JSX
```
// can't use if/else in the return statement because can't use if/else in JSX,
// however, the ternary operator can be used in JSX
{ condition && <div>...</div>}
{ condition ? expressionIfTrue : expressionIfFalse; }

```

### Inline Styles
```
// HTML
<div style="color: yellow; font-size: 16px">
// React
<div style={{color: "yellow", fontSize: "16px"}}>
```

