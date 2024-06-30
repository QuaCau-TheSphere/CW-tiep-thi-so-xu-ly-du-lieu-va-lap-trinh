---
share: true
created: 2023-09-17T18:30
updated: 2024-05-26T14:29
---
VD:

Nếu:
- có một mảng được khai báo ở ngoài hàm `main()`, 
- trong hàm mảng đó được thêm thành phần, 
- có một vòng lặp nào đó **ở file khác** gọi `main()`

thì hàm sẽ bị chồng dữ liệu với những dữ liệu ở lần gọi cũ
[Để tránh phụ thuộc lòng vòng (circular dependency) có thể dùng hàm](../H%C3%A0m/%C4%90%E1%BB%83%20tr%C3%A1nh%20ph%E1%BB%A5%20thu%E1%BB%99c%20l%C3%B2ng%20v%C3%B2ng%20(circular%20dependency)%20c%C3%B3%20th%E1%BB%83%20d%C3%B9ng%20h%C3%A0m.md)
[Nên tách bạch file util cho client và util cho server](./N%C3%AAn%20t%C3%A1ch%20b%E1%BA%A1ch%20file%20util%20cho%20client%20v%C3%A0%20util%20cho%20server.md) 