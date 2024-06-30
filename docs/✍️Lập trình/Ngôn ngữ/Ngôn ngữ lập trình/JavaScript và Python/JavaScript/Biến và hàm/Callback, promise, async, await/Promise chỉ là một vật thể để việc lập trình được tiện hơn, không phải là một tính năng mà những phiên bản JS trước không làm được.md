---
share: true
created: 2023-10-24T18:26
updated: 2024-04-27T16:19
---
[Lớp là một cái khuôn để tạo các vật thể cho nhanh](../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20l%E1%BA%ADp%20tr%C3%ACnh%20h%C6%B0%E1%BB%9Bng%20v%E1%BA%ADt%20th%E1%BB%83/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/L%E1%BB%9Bp%20l%C3%A0%20m%E1%BB%99t%20c%C3%A1i%20khu%C3%B4n%20%C4%91%E1%BB%83%20t%E1%BA%A1o%20c%C3%A1c%20v%E1%BA%ADt%20th%E1%BB%83%20cho%20nhanh.md). Thông thường để tạo một vật thể mới qua một lớp ta dùng thế này:
```js
const xeMáy = new Xe('2 bánh')
const ôTô   = new Xe('4 bánh')
const xeTải = new Xe('12 bánh')
//    ^ vật thể   ^ Lớp
```

Promise là một vật thể, và nó được tạo ra từ lớp `Promise`. Lớp này không nhận đối số là chuỗi như bình thường mà là cả một hàm:
```js
const promise = new Promise(hàm)
//    ^ vật thể     ^ Lớp
```

Hàm này được quy định có 2 đối số có tên là `resolve` và `reject`:
```js
function hàm(resolve, reject) {} 
```

Vật thể `promise` sau khi được tạo ra từ lớp `Promise` sẽ có 3 phương thức: `then`, `catch`, `finally`. 


```js
fetch("https://jsonplaceholder.typicode.com/todos/1")
.then(res => res.json())
.then(d => console.log(d))
```
Nguồn::

