## JSX
```
{/* all HTML attributes and event references become camelCase (class => className, onclick => onClick) */}
{/* all elements must be closed (<br> => <br />) */}
{/* use curly braces {} to include JavaScript within JSX */}
ReactDOM.render(componentToRender, targetNode)
```
### Pass props to stateless functional components
You can pass props to child components
```
const ChildComponent = (props) => {
  ...
    {props.date}
  ...
}

class Parent extends React.Component {
  ...
    <ChildComponent date={Date()} />
  ...
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
