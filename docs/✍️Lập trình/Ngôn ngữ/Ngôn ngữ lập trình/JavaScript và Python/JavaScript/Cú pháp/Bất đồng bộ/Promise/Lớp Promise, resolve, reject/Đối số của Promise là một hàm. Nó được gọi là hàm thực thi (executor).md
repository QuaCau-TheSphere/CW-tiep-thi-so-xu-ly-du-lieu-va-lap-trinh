---
share: true
created: 2023-10-30T14:29
updated: 2024-11-27T15:25
alias: Hàm thực thi là hàm được dùng làm đối số cho lớp Promise
description: Tất cả các lệnh nào chạy tốn thời gian sẽ được đưa vào trong hàm thực thi
---
[Lớp là một cái khuôn để tạo các vật thể cho nhanh](../../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20l%E1%BA%ADp%20tr%C3%ACnh%20h%C6%B0%E1%BB%9Bng%20v%E1%BA%ADt%20th%E1%BB%83/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/L%E1%BB%9Bp%20l%C3%A0%20m%E1%BB%99t%20c%C3%A1i%20khu%C3%B4n%20%C4%91%E1%BB%83%20t%E1%BA%A1o%20c%C3%A1c%20v%E1%BA%ADt%20th%E1%BB%83%20cho%20nhanh.md). Thông thường để tạo một vật thể mới qua một lớp ta dùng thế này:
```js
const xeMáy = new Xe('2 bánh')
const ôTô   = new Xe('4 bánh')
const xeTải = new Xe('12 bánh')
//    ^ vật thể   ^ Lớp
```

Promise là một vật thể, và nó được tạo ra từ lớp `Promise`. Lớp này không nhận đối số là chuỗi như bình thường mà là cả một hàm. Nó được đặt tên là hàm thực thi:
```ts
function hàmThựcThi(biến1, biến2){}
const promise = new Promise(hàmThựcThi);
```

Tất cả các lệnh nào chạy tốn thời gian sẽ được đưa vào trong hàm thực thi. Nên việc chạy hàm thực thi cũng sẽ tốn thời gian.

Đối số của hàm thực thi, đến lượt nó, cũng là 2 hàm khác nhau, được gọi lần lượt là hàm giải quyết và hàm từ chối:
```js
function hàmThựcThi(hàmGiảiQuyết, hàmTừChối){
    // ...
    hàmGiảiQuyết(giáTrịTrongHàmGiảiQuyết)
    // ...
    hàmTừChối(giáTrịTrongHàmTừChối)
}
const promise = new Promise(hàmThựcThi);
```

Khi [engine](../../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi/Code%20gi%E1%BB%91ng%20nh%C6%B0%20c%C3%A1c%20n%E1%BB%91t%20nh%E1%BA%A1c,%20engine%20gi%E1%BB%91ng%20nh%C6%B0%20nh%E1%BA%A1c%20c%C3%B4ng,%20c%C3%B2n%20runtime%20gi%E1%BB%91ng%20nh%C6%B0%20nh%E1%BA%A1c%20c%E1%BB%A5.md) của JS đọc tới dòng này:
```js
const promise = new Promise(hàmThựcThi);
```
thì sẽ có 2 chuyện được xảy ra:
- Vật thể `promise` sẽ có 2 thuộc tính là `state` và `result`. `state` sẽ được gán sẵn giá trị là `pending`
- `hàmThựcThi` sẽ được chạy

Sau đó, tuỳ thuộc vào việc hàm giải quyết được gọi trước hay hàm từ chối được gọi trước mà giá trị của vật thể `promise` sẽ thay đổi tiếp. Nếu hàm giải quyết được gọi trước, thì thuộc tính `state` của vật thể đang từ `pending` sẽ được gán giá trị mới là `fulfilled`. Ngược lại, nếu hàm từ chối được gọi trước, thì thuộc tính `state` của nó sẽ được gán giá trị mới là `rejected`. Ở cả hai trường hợp, giá trị được truyền vào trong hàm sẽ được gán vào thuộc tính `result` của vật thể `promise`.

Đáng lẽ là bạn phải định nghĩa hàm giải quyết và hàm từ chối. Nhưng khi chúng được dùng làm biến cho hàm được dùng làm biến cho lớp `Promise` (tức là hàm thực thi), thì JS sẽ tự động [định nghĩa sẵn](./resolve,%20reject%20l%C3%A0%20hai%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20JS%20cung%20c%E1%BA%A5p%20s%E1%BA%B5n%20%C4%91%E1%BB%83%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20cho%20h%C3%A0m%20th%E1%BB%B1c%20thi.md) hai hàm này luôn, bạn không cần định nghĩa gì cả. Và thường người viết hay đặt tên cho hàm giải quyết là `resolve` và hàm từ chối là  `reject`. Cho nên bạn sẽ hay thấy code người ta viết tắt lại như này:
```js
const promise = new Promise((resolve, reject) => {
    // ...
    resolve(giáTrịTrongHàmGiảiQuyết)
    // ...
    reject(giáTrịTrongHàmTừChối)
});
```

Nếu chạy thông thường thì bạn chỉ cần `return` lấy kết quả trong hàm thực thi là được. Nhưng nhớ rằng ở đây ta đang truyền nó vào `Promise`. Mà đây là một lớp được JS viết ra sẵn, không phải là do bạn viết ra. Khi JS viết ra, nó không viết dòng nào để nhận kết quả của hàm thực thi. Tức là việc bạn có `return` trong đó không có tác dụng gì, ngoài trừ việc làm nó kết thúc sớm. Nếu nó kết thúc trước khi hàm giải quyết hoặc hàm từ chối được gọi thì vật thể `promise` sẽ ở trạng thái `pending` mãi mãi. Nếu nó có lỗi thì mặc định là đang gọi hàm từ chối.

[Để lấy được giá trị state và result của promise, cần dùng các phương thức then và catch](../V%E1%BA%ADt%20th%E1%BB%83%20promise,%20then,%20catch/%C4%90%E1%BB%83%20l%E1%BA%A5y%20%C4%91%C6%B0%E1%BB%A3c%20gi%C3%A1%20tr%E1%BB%8B%20state%20v%C3%A0%20result%20c%E1%BB%A7a%20promise,%20c%E1%BA%A7n%20d%C3%B9ng%20c%C3%A1c%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20then%20v%C3%A0%20catch.md)

Tham khảo:
- [Promise](https://javascript.info/promise-basics)