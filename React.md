## JSX
[State Explanation](https://www.freecodecamp.org/news/what-is-state-in-react-explained-with-examples/)
```
use 'ctrl + /' as shortcut to add comment
{/* try to minimize statefulness */}
{/* all HTML attributes and event references become camelCase (class => className, onclick => onClick) */}
{/* all elements must be closed (<br> => <br />) */}
{/* use curly braces {} to include JavaScript within JSX */}
ReactDOM.render(componentToRender, targetContainerNode)
React.createElement(type, props, ...children)
```
### Create a Controlled Input

```
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
  // To fix asynchronus state updates, use a second form of setState() that accepts a function rather than an object.
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


## HTML DOM (Document Object Model) - constructed as a tree of objects(or nodes)
Lets you access and change all the elements in an HTML document

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

## Random
```
++a is equivalent to a += 1
be careful with a++
```

