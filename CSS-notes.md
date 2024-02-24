##### Table of Contents


# CSS Notes
[md reference](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links)


## Gradient:
```background: gradient-type(color1, color2);```

```background: gradient-type(90deg, color1 0%, color1 40%, color2 40%, color2 100%);```

This looks pretty cool :D
```
background: radial-gradient(
    closest-corner circle at 15% 15%,
    #ccc,
    #ccc 20%,
    #445 21%,
    #223 100%
);
```

## Variable:
To declare:
```--variable-name: value;```

To use:
```random-attribute: var(--variable-name, fallback-value);```

## Display:
- Block:
- Flex: [reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox)
  * display: flex;
  * flex-direction: row; (row-reverse, column, column-reverse)
  * flex-wrap: nowrap; (wrap, wrap-reverse)
  * flex-flow: row wrap; (shorthand for direction + wrap)
  * justify-content: flex-start; (space-evenly, space-around, space-between, center, etc.)
  * align-items: flex-start; (stretch, center, etc.)
  * align-content: flex-start; (stretch, center, etc.)

- Grid: 

## Using media query (@media)
Conditionally apply CSS
```
@media (min-width: 480px) and (max-width: 960px) {
}
```

## The universal selector (*) does not affect pseudo elements
```
html {
box-sizing: border-box;
}

*, ::before, ::after {
box-sizing: inherit;
}
```
## The root pseudo selector ```:root{}``` has a higher specificity than the html type selector
## Wildcard selectors (*, ^, $) for classes
- class name contains "string"
```
[class*="string"] {}
```
- class name starts with "string"
```
[class^="string"] {}
```
- class name ends with "string"
```
[class$="string"] {}
```

## Positions:
- Absolute: 
  - relative to its container
- Relative:
  - relative to its normal position
- Fixed:
  - relative to the viewport
- Sticky:
  - relative to the scroll position

