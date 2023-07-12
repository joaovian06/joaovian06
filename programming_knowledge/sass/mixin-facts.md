# Mixin Facts

In general, here are 5 important facts about arguments and mixins:

- Mixins can take multiple arguments.
- Sass allows you to explicitly define each argument in your '@include' statement.
- When values are explicitly specified you can send them out of order.
- If a mixin definition has a combination of arguments with and without a default value, you should define the ones with no default value first.
- Mixins can be nested.

Here are some concrete examples of the rules:

```sass
@mixin dashed-border($width, $color: #FFF) {
    border: {
        color: $color;
        width: $width;
        style: dashed;
    }
}

span { //only passes non-default argument
    @include dashed-border(3px);
}

p { //passes both arguments
    @include dashed-border(3px, green);
}

div { //passes out of order but explicitly defined
    @include dashed-border(color: purple, width: 5px);
}
```

In the example above, the color of the border of 'span' elements would be white, the border of 'paragraph' elements would be green, while the 'div' elements would have a thicker purple border.
