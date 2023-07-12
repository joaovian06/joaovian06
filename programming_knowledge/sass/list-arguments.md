# List Arguments

Sass allows you to pass in multiple arguments in a list or a map format.

For example, take the multiple properties needed to create the college-ruled stripes in the back of our notecard.

```scss
@mixin stripes(
  $direction,
  $width-percent,
  $stripe-color,
  $stripe-background: #fff
) {
  background: repeating-linear-gradient(
    $direction,
    $stripe-background,
    $stripe-background ($width-percent - 1),
    $stripe-color 1%,
    $stripe-background $width-percent
  );
}
```

In this scenario, it makes sense to create a map with these properties in case we ever want to update or reference them.

```scss
$college-ruled-style: (
  direction: to bottom,
  width-percent: 15%,
  stripe-color: blue,
  stripe-background: white,
);
```

When we include our mixin, we can then pass in these arguments in a map with the following `...` notation:

```scss
.definition {
  width: 100%;
  height: 100%;
  @include stripes($college-ruled-style...);
}
```

Note: Remember to always prioritize readability over writing less code. This approach is only useful if you find it adds clarity to your codebase.
