# Nesting Properties

Congrats, you’ve written your first nested selectors!

In SCSS, nesting is not limited only to selectors. You can also nest common CSS properties if you append a `:` colon suffix after the name of the property.

For example, the following SCSS code:

```sass
.parent {
  font : {
    family: Roboto, sans-serif;
    size: 12px;
    decoration: none;
  }
}
```

will compile to the following CSS:

```css
.parent {
  font-family: Roboto, sans-serif;
  font-size: 12px;
  font-decoration: none;
}
```
