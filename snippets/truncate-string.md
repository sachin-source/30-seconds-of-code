---
title: Truncate string
type: snippet
tags: [string]
cover: bamboo-lamp
dateModified: 2020-10-21T21:17:45+03:00
---

Truncates a string up to a specified length.

- Determine if `String.prototype.length` is greater than `num`.
- Return the string truncated to the desired length, with `'...'` appended to the end or the original string.

```js
const truncateString = (str, num) =>
  str.length > num ? str.slice(0, num > 3 ? num - 3 : num) + '...' : str;
```

```js
truncateString('boomerang', 7); // 'boom...'
```
