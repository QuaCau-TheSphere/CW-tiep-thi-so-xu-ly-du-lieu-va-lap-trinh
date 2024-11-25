---
share: true
created: 2023-10-30T14:29
updated: 2024-11-25T14:51
title: Promise
---
[Lớp là một cái khuôn để tạo các vật thể cho nhanh](../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20l%E1%BA%ADp%20tr%C3%ACnh%20h%C6%B0%E1%BB%9Bng%20v%E1%BA%ADt%20th%E1%BB%83/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/L%E1%BB%9Bp%20l%C3%A0%20m%E1%BB%99t%20c%C3%A1i%20khu%C3%B4n%20%C4%91%E1%BB%83%20t%E1%BA%A1o%20c%C3%A1c%20v%E1%BA%ADt%20th%E1%BB%83%20cho%20nhanh.md). Ví dụ, ta có thể tạo ra các vật thể `xeMáy`, `ôTô`, `xeTải` bằng lớp `Xe` thế này:
```js
const xeMáy = new Xe('2 bánh')
const ôTô   = new Xe('4 bánh')
const xeTải = new Xe('12 bánh')
//    ^ vật thể   ^ Lớp
```

JS cung cấp nhiều loại lớp có sẵn. Một trong những lớp đó là `Promise`. Lớp này không nhận đối số là chuỗi như bình thường mà là cả một hàm:
```js
const promise = new Promise(hàmThựcThi)
//    ^ vật thể     ^ Lớp
```

Hàm này sẽ được thực thi ngay khi bạn khai báo mà không cần bạn phải gọi nó thực thi như thông thường:
```js
function hàmBìnhThường(){
    ...
} // Khi viết xong hàm này thì nó mói chỉ được khai báo, chứ chưa được thực thi
hàmBìnhThường() // Phải tới dòng này thì nó mới được thực thi

const promise = new Promise(hàmThựcThi(){
    ...
}) // Ở đây ta vừa khai báo vừa thực thi hàmThựcThi luôn
```
[Hàm thực thi này được quy định là có 2 đối số. 2 đối số này đến lượt nó lại là 2 hàm khác](./L%E1%BB%9Bp%20Promise/%C4%90%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20Promise%20l%C3%A0%20m%E1%BB%99t%20h%C3%A0m.%20N%C3%B3%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20l%C3%A0%20h%C3%A0m%20th%E1%BB%B1c%20thi%20(executor).md). Hàm đầu tiên có tên là `resolve` còn hàm sau thì có tên là `reject`:
```js
function hàmThựcThi(resolve, reject) {} 
```

[Vật thể promise có 2 thuộc tính là state và result, và 3 phương thức là then, catch, và finally](./V%E1%BA%ADt%20th%E1%BB%83%20promise/V%E1%BA%ADt%20th%E1%BB%83%20promise%20c%C3%B3%202%20thu%E1%BB%99c%20t%C3%ADnh%20l%C3%A0%20state%20v%C3%A0%20result,%20v%C3%A0%203%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20l%C3%A0%20then,%20catch,%20v%C3%A0%20finally.md)
Vật thể `promise` sau khi được tạo ra từ lớp `Promise` sẽ có 3 phương thức: `then`, `catch`, `finally`. 

```js
fetch("https://jsonplaceholder.typicode.com/todos/1")
.then(res => res.json())
.then(d => console.log(d))
```


[Phương thức cho ta biết mình có thể làm gì với vật thể](../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20l%E1%BA%ADp%20tr%C3%ACnh%20h%C6%B0%E1%BB%9Bng%20v%E1%BA%ADt%20th%E1%BB%83/H%C3%A0m/Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c/Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20cho%20ta%20bi%E1%BA%BFt%20m%C3%ACnh%20c%C3%B3%20th%E1%BB%83%20l%C3%A0m%20g%C3%AC%20v%E1%BB%9Bi%20v%E1%BA%ADt%20th%E1%BB%83.md)