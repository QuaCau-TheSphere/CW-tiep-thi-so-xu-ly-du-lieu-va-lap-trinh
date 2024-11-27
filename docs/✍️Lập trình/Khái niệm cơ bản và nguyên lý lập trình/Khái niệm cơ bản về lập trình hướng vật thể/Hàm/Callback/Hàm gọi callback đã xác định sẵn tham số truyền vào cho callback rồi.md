---
share: true
created: 2023-10-30T14:29
updated: 2024-11-27T20:31
---
[Callback là những hàm được dùng như đối số của hàm khác](./Callback%20l%C3%A0%20nh%E1%BB%AFng%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20nh%C6%B0%20%C4%91%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20h%C3%A0m%20kh%C3%A1c.md). Ví dụ như ta hay thấy người ta viết thế này:
```js
function callback(x) {
  return x + 1;
}
hàmGọi(callback); 
```

Nhưng để code này chạy được được thì phải truyền đối số cho callback vào chứ? Nên đáng lẽ phải gán giá trị cho `x` rồi thì code mới chạy được chứ?
```js
function callback(x) {
  return x + 1;
}
const x = 123;
hàmGọi(callback(x)); 
```

Nhưng nếu viết như vậy thì `callback(123)` mới được dùng làm đối số của `hàmGọi()`. Giá trị được truyền vào `hàmGọi()` là `124`, chứ không phải là `callback`. Để được gọi là callback, [nó phải là hàm được dùng như đối số của hàm khác](./Callback%20l%C3%A0%20nh%E1%BB%AFng%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20nh%C6%B0%20%C4%91%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20h%C3%A0m%20kh%C3%A1c.md).

Thực ra nãy giờ ta chưa xét xem `hàmGọi()` có những gì trong đó. Nếu xét thì sẽ thấy nó đã định nghĩa sẵn giá trị sẽ được truyền vào hàm được gọi rồi:
```js
function hàmGọi(callback){
	const x = ...
	callback(x)
} 
```

Điều này cũng có nghĩa là callback bắt buộc phải có đúng thứ tự và kiểu biến được hàm gọi cho trước