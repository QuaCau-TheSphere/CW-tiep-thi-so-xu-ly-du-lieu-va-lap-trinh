---
share: true
created: 2023-10-30T14:29
updated: 2024-04-13T01:00
---

```js
import { signal } from "@preact/signals";

const count = signal(0);

// Read a signal’s value by accessing .value:
console.log(count.value);   // 0

// Update a signal’s value:
count.value += 1;

// The signal's value has changed:
console.log(count.value);  // 1
```
Nguồn:: [Signals – Preact Guide](https://preactjs.com/guide/v10/signals/)