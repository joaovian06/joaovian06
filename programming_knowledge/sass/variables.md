# Variables In Sass

Variables in SCSS allow you to assign an identifier of your choice to a specific value.

Why is that useful? Unlike in CSS, if you need to tweak a value, you’ll only have to update it in one place and the change will be reflected in multiple rules.

In Sass, `$` is used to define and reference a variable:

```sass
$translucent-white: rgba(255,255,255,0.3);
```

Note: It’s important to stick to one naming convention for variables when you first build out your codebase. This will help you reference them easily in the future.
