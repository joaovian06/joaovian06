# The & Selector in Mixins

It’s time to tie in how the `&` selector plays into mixins.

Sass allows `&` selector usage inside of mixins. The flow works much like you think it would:

1. The `&` selector gets assigned the value of the parent at the point where the mixin is included.

2. If there is no parent selector, then the value is null and Sass will throw an error.

```scss
@mixin text-hover($color) {
  &:hover {
    color: $color;
  }
}
```

In the above, the value of the parent selector will be assigned based on the parent at the point where it is invoked.

```scss
.word {
  //SCSS:
  display: block;
  text-align: center;
  position: relative;
  top: 40%;
  @include text-hover(red);
}
```

The above will compile to the following CSS:

```css
.word {
  display: block;
  text-align: center;
  position: relative;
  top: 40%;
}
.word:hover {
  color: red;
}
```

Notice that the mixin inherited the parent selector `.word` because that was the parent at the point where the mixin was included.
