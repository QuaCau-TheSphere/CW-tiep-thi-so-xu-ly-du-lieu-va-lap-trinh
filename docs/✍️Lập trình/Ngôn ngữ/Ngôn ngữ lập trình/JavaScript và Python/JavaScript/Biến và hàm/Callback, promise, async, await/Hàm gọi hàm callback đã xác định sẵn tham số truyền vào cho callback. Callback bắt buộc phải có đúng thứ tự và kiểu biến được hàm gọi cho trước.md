---
share: true
created: 2023-10-30T14:29
updated: 2024-04-27T16:19
---
[Callback là những hàm được dùng như đối số của hàm khác](./Callback%20l%C3%A0%20nh%E1%BB%AFng%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20nh%C6%B0%20%C4%91%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20h%C3%A0m%20kh%C3%A1c.md). Khi dùng những hàm có callback, ta thắc mắc không biết tham số đã được truyền vào như thế nào? Ví dụ như:
```js
function callback (e) {
  console.log('clicked');
}

hàmNgoài(callback);
```

Ta thấy `callback()` là một hàm. Để nó hoạt động được thì phải truyền tham số vào. Nên đáng lẽ code trên phải là như vậy mới đúng chứ?

```js
function callback (e) {
  console.log('clicked');
}

const e = hàmNgoài();
callback(e)
```

Thực ra có thể nghĩ là `hàmNgoài()` đã được viết sẵn như vậy ở đâu đó:
```js
function hàmNgoài(callback){
	const e = ...
	callback(e)
} 
```