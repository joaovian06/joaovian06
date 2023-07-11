# Mixins: Arguments

Mixins also have the ability to take in a value.

An argument, or parameter, is a value passed to the mixin that will be used inside the mixin, such as `$visibility` in this example:

```sass
@mixin backface-visibility($visibility) {
backface-visibility: $visibility;
-webkit-backface-visibility: $visibility;
-moz-backface-visibility: $visibility;
-ms-backface-visibility: $visibility;
-o-backface-visibility: $visibility;
}
```

In fact, you should only ever use a mixin if it takes an argument. We will learn more about this in a later exercise.

The syntax to pass in a value is as follows:

```sass
@include backface-visibility(hidden);
```

In the code above, `hidden` is passed into the `backface-visibility` mixin, where it will be assigned as the value of its argument, `$visibility`.
