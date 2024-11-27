---
share: true
created: 2024-11-27T15:04
updated: 2024-11-27T20:33
---
[Kết quả của promise chỉ có thể được lấy ở trong then](./K%E1%BA%BFt%20qu%E1%BA%A3%20c%E1%BB%A7a%20promise%20ch%E1%BB%89%20c%C3%B3%20th%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20l%E1%BA%A5y%20%E1%BB%9F%20trong%20then.md)
[resolve, reject là hai hàm được JS cung cấp sẵn để làm đối số cho hàm thực thi](../L%E1%BB%9Bp%20Promise,%20resolve,%20reject/resolve,%20reject%20l%C3%A0%20hai%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20JS%20cung%20c%E1%BA%A5p%20s%E1%BA%B5n%20%C4%91%E1%BB%83%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20cho%20h%C3%A0m%20th%E1%BB%B1c%20thi.md).
[Khi resolve được gọi, vật thể promise sẽ cập nhật kết quả trả về từ resolve, và hàm được dùng làm đối số đầu tiên của then sẽ được chạy](../L%E1%BB%9Bp%20Promise,%20resolve,%20reject/Khi%20resolve%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di,%20v%E1%BA%ADt%20th%E1%BB%83%20promise%20s%E1%BA%BD%20c%E1%BA%ADp%20nh%E1%BA%ADt%20k%E1%BA%BFt%20qu%E1%BA%A3%20tr%E1%BA%A3%20v%E1%BB%81%20t%E1%BB%AB%20resolve,%20v%C3%A0%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20%C4%91%E1%BA%A7u%20ti%C3%AAn%20c%E1%BB%A7a%20then%20s%E1%BA%BD%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BA%A1y.md)

- Thuộc tính `state` đang từ `pending` sẽ được gán giá trị mới là `fulfilled`
- Giá trị được truyền vào trong `resolve()` sẽ được gán vào thuộc tính `result` 
- Hàm được dùng làm đối số đầu tiên của `then()` sẽ chạy

Ngược lại, khi `reject()` được gọi:
- Thuộc tính `state` đang từ `pending` sẽ được gán giá trị mới là `rejected`
- Giá trị được truyền vào trong `reject()` sẽ được gán vào thuộc tính `result`  
- Hàm được dùng làm đối số thứ hai của `then()` sẽ chạy
