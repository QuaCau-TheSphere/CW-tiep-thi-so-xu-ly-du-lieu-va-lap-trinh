---
share: true
created: 2023-10-30T14:29
updated: 2024-11-25T16:47
---
```ts
function hàmThựcThi(biến1, biến2){
    // Những hàm bất đồng bộ thì để vào đây
}
const promise = new Promise(hàmThựcThi);
```

Đối số của `hàmThựcThi`, đến lượt nó, cũng là 2 hàm khác nhau, được gọi lần lượt là hàm giải quyết và hàm từ chối:
```js
function hàmGiảiQuyết(giáTrịTrongHàmGiảiQuyết){}
function hàmTừChối(giáTrịTrongHàmTừChối){}
function hàmThựcThi(hàmGiảiQuyết, hàmTừChối){}
```

Thông thường, bạn phải định nghĩa `hàmGiảiQuyết` và `hàmTừChối`. Nhưng nếu bạn 

Nếu chạy thông thường thì bạn chỉ cần `return` lấy kết quả trong `hàmThựcThi` là được. Nhưng nhớ rằng ở đây ta đang truyền nó vào `Promise`. Mà đây là một lớp được JS viết ra sẵn, không phải là do bạn viết ra. Khi JS viết ra, nó không viết dòng nào để nhận kết quả của `hàmThựcThi`. Tức là việc bạn có `return` trong đó không có tác dụng gì (ngoài trừ việc làm nó kết thúc sớm).

Thứ JS thiết kế ở `Promise`, là khi chạy `hàmThựcThi` thì `hàmGiảiQuyết` được gọi trước hay là `hàmTừChối` được gọi trước. Nếu `hàmGiảiQuyết` được gọi trước, thì `giáTrịTrongHàmGiảiQuyết` sẽ được gán vào thuộc tính `result` của vật thể `promise`, đồng thời chuyển giá trị của thuộc tính `state` của nó từ `pending` sang `fulfilled`. Ngược lại, nếu `hàmTừChối` được gọi trước, thì `giáTrịTrongHàmTừChối` sẽ được gán vào thuộc tính `result` của vật thể `promise`, đồng thời chuyển giá trị của thuộc tính `state` của nó từ `pending` sang `rejected`. 

[resolve, reject là hai hàm được JS cung cấp sẵn. Chúng được dùng làm đối số cho hàm thực thi](./resolve,%20reject%20l%C3%A0%20hai%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20JS%20cung%20c%E1%BA%A5p%20s%E1%BA%B5n.%20Ch%C3%BAng%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20cho%20h%C3%A0m%20th%E1%BB%B1c%20thi.md)

[Để lấy được giá trị state và result của promise, cần dùng các phương thức then và catch của nó](../V%E1%BA%ADt%20th%E1%BB%83%20promise/%C4%90%E1%BB%83%20l%E1%BA%A5y%20%C4%91%C6%B0%E1%BB%A3c%20gi%C3%A1%20tr%E1%BB%8B%20state%20v%C3%A0%20result%20c%E1%BB%A7a%20promise,%20c%E1%BA%A7n%20d%C3%B9ng%20c%C3%A1c%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20then%20v%C3%A0%20catch%20c%E1%BB%A7a%20n%C3%B3.md)

Tham khảo:
- [Promise](https://javascript.info/promise-basics)