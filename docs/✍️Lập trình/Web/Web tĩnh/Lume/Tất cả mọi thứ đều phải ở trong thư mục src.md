---
share: true
created: 2023-10-30T14:29
updated: 2024-08-11T13:23
---
Mặc định `src` nằm ở `.`. Để thay đổi thì thêm cái này trong `_config.ts`:
```js
const site = lume({
  src: "./src",
});
```
[Tất cả các đường dẫn đều bắt đầu từ src](./T%E1%BA%A5t%20c%E1%BA%A3%20c%C3%A1c%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20%C4%91%E1%BB%81u%20b%E1%BA%AFt%20%C4%91%E1%BA%A7u%20t%E1%BB%AB%20src.md)
Nguồn:: [The \_config file - Lume](https://lume.land/docs/configuration/config-file/#src)