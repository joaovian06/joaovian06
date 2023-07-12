# String Interpolation

In Sass, string interpolation is the process of placing a variable string in the middle of two other strings.

In a mixin context, interpolation is handy when you want to make use of variables in selectors or file names. The notation is as follows:

```scss
@mixin photo-content($file) {
  content: url(#{$file}.jpg); //string interpolation
  object-fit: cover;
}

//....

.photo {
  @include photo-content("titanosaur");
  width: 60%;
  margin: 0px auto;
}
```

String interpolation would enable the following CSS:

```css
.photo {
  content: url(titanosaur.jpg);
  width: 60%;
  margin: 0px auto;
}
```
