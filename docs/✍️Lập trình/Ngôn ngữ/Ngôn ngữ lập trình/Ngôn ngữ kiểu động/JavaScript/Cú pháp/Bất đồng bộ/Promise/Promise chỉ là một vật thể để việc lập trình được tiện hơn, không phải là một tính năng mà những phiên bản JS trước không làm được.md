---
share: true
created: 2023-10-24T18:26
updated: 2025-03-03T18:48
---
[Lớp là một cái khuôn để tạo các vật thể cho nhanh](../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/L%E1%BB%9Bp%20l%C3%A0%20m%E1%BB%99t%20c%C3%A1i%20khu%C3%B4n%20%C4%91%E1%BB%83%20t%E1%BA%A1o%20c%C3%A1c%20v%E1%BA%ADt%20th%E1%BB%83%20cho%20nhanh.md). Thông thường để tạo một vật thể mới qua một lớp ta dùng thế này:
```js
const xeMáy = new Xe('2 bánh')
const ôTô   = new Xe('4 bánh')
const xeTải = new Xe('12 bánh')
//    ^ vật thể   ^ Lớp
```

Promise là một vật thể, và nó được tạo ra từ lớp `Promise`. Lớp này không nhận đối số là chuỗi như bình thường mà là cả một hàm:
```js
const promise = new Promise(hàmThựcThi)
//    ^ vật thể     ^ Lớp
```

Hàm này sẽ được thực thi ngay khi bạn khai báo mà không cần bạn phải gọi nó thực thi như thông thường:
```js
function hàmBìnhThường(){} // chỉ mới khai báo, chưa thực thi
hàmBìnhThường() // Tới lúc này mới thực thi

const promise = new Promise(hàmThựcThi) // hàmThựcThi() được thực thi ngay tại dòng này
```
[Hàm thực thi này được quy định là có 2 đối số. 2 đối số này đến lượt nó lại là 2 hàm khác](./L%E1%BB%9Bp%20Promise,%20resolve,%20reject/%C4%90%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20Promise%20l%C3%A0%20m%E1%BB%99t%20h%C3%A0m.%20N%C3%B3%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20l%C3%A0%20h%C3%A0m%20th%E1%BB%B1c%20thi%20(executor).md). Hàm đầu tiên có tên là `resolve` còn hàm sau thì có tên là `reject`:
```js
function hàmThựcThi(resolve, reject) {} 
```

[Vật thể promise có 2 thuộc tính là state và result, và 3 phương thức là then, catch, và finally](./V%E1%BA%ADt%20th%E1%BB%83%20promise,%20then,%20catch/V%E1%BA%ADt%20th%E1%BB%83%20promise%20c%C3%B3%202%20thu%E1%BB%99c%20t%C3%ADnh%20l%C3%A0%20state%20v%C3%A0%20result,%20v%C3%A0%203%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20l%C3%A0%20then,%20catch,%20v%C3%A0%20finally.md)
Vật thể `promise` sau khi được tạo ra từ lớp `Promise` sẽ có 3 phương thức: `then`, `catch`, `finally`. 

```js
fetch("https://jsonplaceholder.typicode.com/todos/1")
.then(res => res.json())
.then(d => console.log(d))
```


[Phương thức cho ta biết mình có thể làm gì với vật thể](../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c/Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20cho%20ta%20bi%E1%BA%BFt%20m%C3%ACnh%20c%C3%B3%20th%E1%BB%83%20l%C3%A0m%20g%C3%AC%20v%E1%BB%9Bi%20v%E1%BA%ADt%20th%E1%BB%83.md)
[Đường cú pháp là những loại cú pháp giúp việc đọc dễ dàng hơn. Muối cú pháp là những loại cú pháp giúp việc viết sai trở nên khó khăn hơn](../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Nguy%C3%AAn%20l%C3%BD/%C4%90%C6%B0%E1%BB%9Dng%20c%C3%BA%20ph%C3%A1p%20l%C3%A0%20nh%E1%BB%AFng%20lo%E1%BA%A1i%20c%C3%BA%20ph%C3%A1p%20gi%C3%BAp%20vi%E1%BB%87c%20%C4%91%E1%BB%8Dc%20d%E1%BB%85%20d%C3%A0ng%20h%C6%A1n.%20Mu%E1%BB%91i%20c%C3%BA%20ph%C3%A1p%20l%C3%A0%20nh%E1%BB%AFng%20lo%E1%BA%A1i%20c%C3%BA%20ph%C3%A1p%20gi%C3%BAp%20vi%E1%BB%87c%20vi%E1%BA%BFt%20sai%20tr%E1%BB%9F%20n%C3%AAn%20kh%C3%B3%20kh%C4%83n%20h%C6%A1n.md)