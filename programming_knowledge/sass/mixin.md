# What is a Mixin?

In addition to variables and nesting, Sass has multiple constructs that reduce repetition.

In Sass, a mixin lets you make groups of CSS declarations that you want to reuse throughout your site.

The notation for creating a mixin is as follows:

```sass
@mixin backface-visibility {
backface-visibility: hidden;
-webkit-backface-visibility: hidden;
-moz-backface-visibility: hidden;
-ms-backface-visibility: hidden;
-o-backface-visibility: hidden;
}
```

Note: Mixin names and all other Sass identifiers use hyphens and underscores interchangeably. The following code:

```scss
.notecard {
  .front,
  .back {
    width: 100%;
    height: 100%;
    position: absolute;

    @include backface-visibility;
  }
}
```

is equivalent to the following CSS:

```css
.notecard .front,
.notecard .back {
  width: 100%;
  height: 100%;
  position: absolute;

  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  -moz-backface-visibility: hidden;
  -ms-backface-visibility: hidden;
  -o-backface-visibility: hidden;
}
```
