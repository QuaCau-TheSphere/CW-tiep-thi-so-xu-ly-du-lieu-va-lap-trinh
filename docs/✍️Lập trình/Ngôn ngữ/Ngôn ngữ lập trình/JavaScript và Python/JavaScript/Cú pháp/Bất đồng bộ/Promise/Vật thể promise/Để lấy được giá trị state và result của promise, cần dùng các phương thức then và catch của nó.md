---
share: true
created: 2023-10-30T14:29
updated: 2024-11-24T15:19
---
Nhớ rằng, [resolve, reject là các hàm được ](../L%E1%BB%9Bp%20Promise/resolve,%20reject%20l%C3%A0%20hai%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20JS%20cung%20c%E1%BA%A5p%20s%E1%BA%B5n.%20Ch%C3%BAng%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20cho%20h%C3%A0m%20th%E1%BB%B1c%20thi.md)
Đối số đầu tiên của `then` là một hàm sẽ chạy khi promise được giải quyết và nhận kết quả từ hàm `resolve()`.
Đối số thứ hai của `then` là một hàm sẽ chạy khi promise bị từ chối và nhận kết quả.
The first argument of `.then` is a function that runs when the promise is resolved and receives the result.

The second argument of `.then` is a function that runs when the promise is rejected and receives the error.
[Vật thể promise có 2 thuộc tính là state và result, và 3 phương thức là then, catch, và finally](./V%E1%BA%ADt%20th%E1%BB%83%20promise%20c%C3%B3%202%20thu%E1%BB%99c%20t%C3%ADnh%20l%C3%A0%20state%20v%C3%A0%20result,%20v%C3%A0%203%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20l%C3%A0%20then,%20catch,%20v%C3%A0%20finally.md)
Nguồn:: [Promise](https://javascript.info/promise-basics)