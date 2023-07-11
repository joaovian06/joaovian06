# Maps & Lists

In addition to color, numbers, strings, booleans, and null, Sass also has two other data types, lists and maps.

- Lists can be separated by either spaces or commas. For example, the following list denotes font properties, such as:

```sass
1.5em Helvetica bold;
```

or

```sass
Helvetica, Arial, sans-serif;
```

Note: You can also surround a list with parentheses and create lists made up of lists.

- Maps are very similar to lists, but instead each object is a key-value pair. The typical map looks like:

```sass
(key1: value1, key2: value2);
```

Note: In a map, the value of a key can be a list or another map.
