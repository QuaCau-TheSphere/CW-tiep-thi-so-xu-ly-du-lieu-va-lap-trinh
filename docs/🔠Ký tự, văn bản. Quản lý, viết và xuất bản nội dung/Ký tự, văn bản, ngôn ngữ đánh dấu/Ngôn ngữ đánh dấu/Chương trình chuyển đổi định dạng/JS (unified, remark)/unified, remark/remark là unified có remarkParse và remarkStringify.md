---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
Gọi `remark` thế này
```js
const file = await remark()
  .use(remarkPresetLintConsistent)
  .use(remarkPresetLintRecommended)
  .process('1) Hello, _Jupiter_ and *Neptune*!')
```

tương đương với gọi `unified` thế này:
```js
const file = await unified()
  .use(remarkParse)
  .use(remarkStringify)
  .use(remarkPresetLintConsistent)
  .use(remarkPresetLintRecommended)
  .process('1) Hello, _Jupiter_ and *Neptune*!')
```

Nguồn:: [Stack Overflow](../../../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [Why can remark work independently from unified?](https://stackoverflow.com/a/78913256/3416774)