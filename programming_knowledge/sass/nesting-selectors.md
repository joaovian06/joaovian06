# Nesting Selectors

The first Sass construct we will learn about is nesting.

Nesting is the process of placing selectors inside the scope of another selector:

In programming, a variable’s scope is the context in which a variable is defined and available to use.

In Sass, it’s helpful to think of the scope of a selector as any of the code between its opening `{` and closing `}` curly brackets.

Selectors that are nested inside the scope of another selector are referred to as children. The former selector is referred to as the parent. This is just like the relationship observed in HTML elements.

```sass
.parent {
  color: blue;
  .child {
    font-size: 12px;
  }
}
```

In the example above `.child` is the child selector and `.parent` is the parent selector.

The above SCSS would compile to the following, equivalent CSS:

```css
.parent {
  color: blue;
}

.parent .child {
  font-size: 12px;
}
```

Nesting allows you to see the clear DOM relationship between two selectors while also removing the repetition observed in CSS.
