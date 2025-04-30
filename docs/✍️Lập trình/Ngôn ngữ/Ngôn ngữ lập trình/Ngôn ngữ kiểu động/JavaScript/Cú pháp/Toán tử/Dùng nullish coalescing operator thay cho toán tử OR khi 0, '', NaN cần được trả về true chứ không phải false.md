---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
title: Khi dùng `||` cho `0`, `''`, `NaN`  thì kết quả sẽ là `false`. Với `??`, chúng sẽ trả về `true`
alias: nullish coalescing operator
---
Nếu dùng toán tử OR (`||`) thì `0`, `''`, `NaN` sẽ trả về `false`:
```js
const baz = 0 || 42;
console.log(baz);
// Expected output: 42
```

Nhưng nếu dùng nullish coalescing operator (`??`),  thì `0`, `''`, `NaN` sẽ trả về `true`:
```js
const baz = 0 ?? 42;
console.log(baz);
// Expected output: 0
```

Nguồn:: [MDN](../../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/MDN.md), [Nullish coalescing operator (??) - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)