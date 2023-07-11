# The & Selector in Nesting

In the next set of exercises, you’ll use new Sass concepts to fix and add styles to the notecard on the right so that it flips when you hover over it!

Recall that, in CSS, a pseudo-element is used to style parts of an element, for example:

- Styling the content `::before` or `::after` the content of an element.

- Using a pseudo class such as `:hover` to set the properties of an element when the user’s mouse is touching the area of the element.

In Sass, the parent selector, `&`, is used to specify exactly where a parent selector should be inserted. It also helps write pseudo-classes in a much less repetitive way.

For example, the following Sass:

```sass
.notecard{
  &:hover{
      @include transform (rotatey(-180deg));
    }
  }
```

will compile to the following CSS:

```css
.notecard:hover {
  transform: rotatey(-180deg);
}
```
