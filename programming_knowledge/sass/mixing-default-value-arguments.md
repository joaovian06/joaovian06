# Default Value Arguments

Mixin arguments can be assigned a default value in the mixin definition by using a special notation.

A default value is assigned to the argument if no value is passed in when the mixin is included. Defining a default value for each argument is optional.

The notation is as follows:

```sass
@mixin backface-visibility($visibility: hidden) {
   backface-visibility: $visibility;
  -webkit-backface-visibility: $visibility;
  -moz-backface-visibility: $visibility;
  -ms-backface-visibility: $visibility;
  -o-backface-visibility: $visibility;
}
```

In the example above, if no value is passed in when `backface-visibility` is included, `hidden` would be assigned to all properties.
