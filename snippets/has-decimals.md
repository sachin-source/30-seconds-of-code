---
title: Number has decimal digits
type: snippet
tags: [math]
author: chalarangelo
cover: man-cup-laptop
dateModified: 2022-05-13T05:00:00-04:00
---

Checks if a number has any decimals digits

- Use the modulo (`%`) operator to check if the number is divisible by `1` and return the result.

```js
const hasDecimals = num => num % 1 !== 0;
```

```js
hasDecimals(1); // false
hasDecimals(1.001); // true
```
