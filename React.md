## JSX
```
{/* all HTML attributes and event references become camelCase (class => className, onclick => onClick) */}
{/* all elements must be closed (<br> => <br />) */}
ReactDOM.render(componentToRender, targetNode)
```

## HTML DOM (Document Object Model) - constructed as a tree of objects(or nodes)
Let's you access and change all the elements in an HTML document

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
