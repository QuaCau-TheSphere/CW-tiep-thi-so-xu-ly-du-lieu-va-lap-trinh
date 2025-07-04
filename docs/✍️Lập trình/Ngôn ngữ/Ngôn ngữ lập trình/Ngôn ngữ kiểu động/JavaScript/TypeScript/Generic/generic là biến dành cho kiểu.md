---
share: true
created: 2023-10-24T18:26
updated: 2025-03-03T18:48
---
[generic là cách để giữ được tính chung chung mà vẫn không bị mất thông tin](./generic%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20gi%E1%BB%AF%20%C4%91%C6%B0%E1%BB%A3c%20t%C3%ADnh%20chung%20chung%20m%C3%A0%20v%E1%BA%ABn%20kh%C3%B4ng%20b%E1%BB%8B%20m%E1%BA%A5t%20th%C3%B4ng%20tin.md)
Biến (variable) thì để trong `( )`, còn biến kiểu (type variable) thì để trong `< >`

Ví dụ, đây là cách viết hàm như bình thường:
```js
function f(x)
```
Trước giờ nếu muốn khai báo kiểu cho cả hàm và biến thì phải viết thế này:
```ts
interface t { u }
function f(x: t): t
```
Nhưng cách viết này thì `u` bị giữ cố định trong code. Nó là hằng rồi chứ không phải là biến. Nếu muốn nó cũng là biến thì ngay trong hàm cũng phải khai báo `t` như thể nó là một biến.

Nếu có thể viết chỉ số dưới chân cả hai như vậy thì tiện:
```ts
fₜ(xₜ)
```

Nhưng vì không dùng unicode được nên viết như thế này:
```js
f(t)(x) 
```
Nhưng nếu vậy thì không phân biệt được cái nào thực sự là biến dành cho hàm, cái nào là biến dành cho kiểu. Để phân biệt thì ta dùng ngoặc nhọn:
```ts
f<t>(x) 
```
Rồi sau đó khai báo kiểu cho biến và hàm như bình thường:
```ts
f<t>(x: t): t
```
Đây chính là cú pháp của generic. Ví dụ:
```ts
function identity<Type>(arg: Type): Type { return arg;}
```

Cũng giống như ta có thể có nhiều biến trong hàm, ta cũng có thể có nhiều biến kiểu trong hàm:
```ts
f<t, u>(x, y) 
```
