---
title: Add an event to multiple elements
type: snippet
tags: [browser,javascript,event]
cover: button
dateModified: 2023-05-07T10:06:26+05:30
---

Adds an event(s) to one or more HTML elements based on their query selector

- Use `EventTarget.addEventListener()` to add event listener to the elements with  `Array.prototype.forEach()` to loop and iterate through all the elements.
- Supports single as well as multiple query selectors
- supports single as well as multiple events

```js
const addListenertoMultipleElements = (querySelectors, types, listener, options, capture) => {
  const querySelectorsArr = [].concat(querySelectors);
  const typesArr = [].concat(types);

querySelectorsArr.forEach(querySelector => {
    types.forEach(type =>
      document.querySelectorAll(querySelector).forEach(element => element.addEventListener(type, listener, options, capture))
    );
  })
};
```

```js
addListenertoMultipleElements(
  '.my-element', // use array for multiple querySelectors. ex : ['p', '.my-element']
  ['click', 'mousedown'], // use as string argument incase of single event. ex : 'click' 
  () => { console.log('hello!') }
);
```
