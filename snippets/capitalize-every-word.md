---
title: Capitalize every word
type: snippet
tags: [string,regexp]
cover: laptop-plants
dateModified: 2020-10-22T20:23:47+03:00
---

Capitalizes the first letter of every word in a string.

- Use `String.prototype.replace()` to match the first character of each word and `String.prototype.toUpperCase()` to capitalize it.

```js
const capitalizeEveryWord = str =>
  str.replace(/\b[a-z]/g, char => char.toUpperCase());
```

```js
capitalizeEveryWord('hello world!'); // 'Hello World!'
```
