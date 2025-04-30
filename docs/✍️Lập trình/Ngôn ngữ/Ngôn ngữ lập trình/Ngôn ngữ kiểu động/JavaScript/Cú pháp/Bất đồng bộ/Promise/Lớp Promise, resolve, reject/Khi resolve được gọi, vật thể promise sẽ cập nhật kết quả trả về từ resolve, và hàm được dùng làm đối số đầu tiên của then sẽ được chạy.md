---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
Lúc tạo vật thể promise thì [đối số được dùng cho lớp Promise là một hàm được gọi là hàm thực thi](./%C4%90%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20Promise%20l%C3%A0%20m%E1%BB%99t%20h%C3%A0m.%20N%C3%B3%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20l%C3%A0%20h%C3%A0m%20th%E1%BB%B1c%20thi%20(executor).md):
```ts
function hàmThựcThi(biến1, biến2){}
const promise = new Promise(hàmThựcThi);
```

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

Đáng lẽ là bạn phải định nghĩa hàm giải quyết và hàm từ chối. Nhưng khi chúng được dùng làm biến cho hàm được dùng làm biến cho lớp `Promise` (tức là hàm thực thi), thì JS sẽ tự động [định nghĩa sẵn](./resolve,%20reject%20l%C3%A0%20hai%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20JS%20cung%20c%E1%BA%A5p%20s%E1%BA%B5n%20%C4%91%E1%BB%83%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20cho%20h%C3%A0m%20th%E1%BB%B1c%20thi.md) hai hàm này luôn, bạn không cần định nghĩa gì cả. Và thường người viết hay đặt tên cho hàm giải quyết là `resolve` và hàm từ chối là  `reject`. Cho nên bạn sẽ hay thấy code người ta viết tắt lại như này:

```js
const promise = new Promise((resolve, reject) => {
    // ...
    resolve(giáTrịTrongHàmGiảiQuyết)
    // ...
    reject(giáTrịTrongHàmTừChối)
});
```

Nhớ rằng, [Vật thể promise có 2 thuộc tính là state và result, và 3 phương thức là then, catch, và finally](../V%E1%BA%ADt%20th%E1%BB%83%20promise,%20then,%20catch/V%E1%BA%ADt%20th%E1%BB%83%20promise%20c%C3%B3%202%20thu%E1%BB%99c%20t%C3%ADnh%20l%C3%A0%20state%20v%C3%A0%20result,%20v%C3%A0%203%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20l%C3%A0%20then,%20catch,%20v%C3%A0%20finally.md). Khi `resolve()` được gọi:
- Thuộc tính `state` đang từ `pending` sẽ được gán giá trị mới là `fulfilled`
- Giá trị được truyền vào trong `resolve()` sẽ được gán vào thuộc tính `result` 
- Hàm được dùng làm đối số đầu tiên của `then()` sẽ chạy

Ngược lại, khi `reject()` được gọi:
- Thuộc tính `state` đang từ `pending` sẽ được gán giá trị mới là `rejected`
- Giá trị được truyền vào trong `reject()` sẽ được gán vào thuộc tính `result`  
- Hàm được dùng làm đối số thứ hai của `then()` sẽ chạy

Nguồn:: [Tự ngẫm nghĩ, trải nghiệm](../../../../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/T%E1%BB%B1%20ng%E1%BA%ABm%20ngh%C4%A9,%20tr%E1%BA%A3i%20nghi%E1%BB%87m.md)
