---
share: true
created: 2023-10-24T18:26
updated: 2024-05-26T14:04
---
`a.js` (entry module):

```javascript
import { b } from "./b.js";

export const a = 2;
```

`b.js`:

```javascript
import { a } from "./a.js";

console.log(a); // ReferenceError: Cannot access 'a' before initialization
export const b = 1;
```

# Cách 1
```javascript
function a_js() {
  var b = b_js(); // unnecessary line
  return 2;
}

function b_js() {
  var a = a_js();
  console.log(a);
  return 1;
}
```
# Cách 2
`a.js`:
```javascript
import { logA, b } from "./b.js";

export const a = 2;

logA();
console.log(b);
```

`b.js`:
```javascript
import { a } from "./a.js";

export const b = 1;

export function logA() {
  console.log(a);
}
```

Nguồn:: [Does importing a module mean embedding the code of the module at the line of the import statement?](https://stackoverflow.com/q/76928950/3416774)

[Việc chia các lệnh trong kịch bản thành các hàm nhỏ hơn sẽ giúp dễ bắt lỗi hơn](../../Nguy%C3%AAn%20l%C3%BD/%C4%90%C6%A1n%20nhi%E1%BB%87m/Vi%E1%BB%87c%20chia%20c%C3%A1c%20l%E1%BB%87nh%20trong%20k%E1%BB%8Bch%20b%E1%BA%A3n%20th%C3%A0nh%20c%C3%A1c%20h%C3%A0m%20nh%E1%BB%8F%20h%C6%A1n%20s%E1%BA%BD%20gi%C3%BAp%20d%E1%BB%85%20b%E1%BA%AFt%20l%E1%BB%97i%20h%C6%A1n.md)
[Khi import một hàm thì cả file chứa hàm đó sẽ được chạy. Các import cũng sẽ chạy theo, dù là để import vào một hàm khác mình không import](../M%C3%B4%20%C4%91un/Khi%20import%20m%E1%BB%99t%20h%C3%A0m%20th%C3%AC%20c%E1%BA%A3%20file%20ch%E1%BB%A9a%20h%C3%A0m%20%C4%91%C3%B3%20s%E1%BA%BD%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BA%A1y.%20C%C3%A1c%20import%20c%C5%A9ng%20s%E1%BA%BD%20ch%E1%BA%A1y%20theo,%20d%C3%B9%20l%C3%A0%20%C4%91%E1%BB%83%20import%20v%C3%A0o%20m%E1%BB%99t%20h%C3%A0m%20kh%C3%A1c%20m%C3%ACnh%20kh%C3%B4ng%20import.md)