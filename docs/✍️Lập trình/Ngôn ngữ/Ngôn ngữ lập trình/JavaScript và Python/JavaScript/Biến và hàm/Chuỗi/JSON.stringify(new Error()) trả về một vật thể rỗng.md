---
share: true
created: 2023-10-30T14:29
updated: 2024-05-05T20:40
---
```javascript
> JSON.stringify(error);
'{}'
```

From the document of [JSON.stringify()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify),

> For all the other Object instances (including Map, Set, WeakMap and WeakSet), only their enumerable properties will be serialized.

and `Error` object doesn't have any enumerable properties, that's why it prints an empty object.

**Background on enumerable properties**

In Javascript, an object can have two types of properties:

- enumerable properties
- non-enumerable properties

The exact distinction is a bit tricky, but basically:

- "normal" properties, such as the ones you create by assignment ( `myobj= {}; myobj.prop1 = 4711;`), are enumerable,
- "internal" properties, such as the `length` property of an array, are non-enumerable

In particular, an `Error` has _only_ non-enumerable properties.

For details, see for example [Enumerability and ownership of properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Enumerability_and_ownership_of_properties) on MDN.

Nguồn:: [Stack Overflow](../../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md),  [Is it not possible to stringify an Error using JSON.stringify?](https://stackoverflow.com/a/50738205/3416774)