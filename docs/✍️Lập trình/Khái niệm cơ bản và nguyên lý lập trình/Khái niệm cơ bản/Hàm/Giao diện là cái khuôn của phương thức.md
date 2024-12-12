---
share: true
created: 2023-10-24T18:26
updated: 2024-12-04T15:51
---
[Phương thức cho ta biết mình có thể làm gì với vật thể](../V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c/Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20cho%20ta%20bi%E1%BA%BFt%20m%C3%ACnh%20c%C3%B3%20th%E1%BB%83%20l%C3%A0m%20g%C3%AC%20v%E1%BB%9Bi%20v%E1%BA%ADt%20th%E1%BB%83.md). [Lớp là một cái khuôn để tạo các vật thể cho nhanh](../V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/L%E1%BB%9Bp%20l%C3%A0%20m%E1%BB%99t%20c%C3%A1i%20khu%C3%B4n%20%C4%91%E1%BB%83%20t%E1%BA%A1o%20c%C3%A1c%20v%E1%BA%ADt%20th%E1%BB%83%20cho%20nhanh.md). Giả sử ta có nhiều lớp khác nhau, và các vật thể được tạo ra từ các lớp này đều có cùng một số phương thức giống nhau. Lúc này, ta sẽ có một *tập hợp* các phương thức giống nhau cho tất cả các lớp. 

[Giao diện là cách để sử dụng vật thể mà không cần biết bên trong nó có gì](../M%C3%B4%20%C4%91un/Giao%20di%E1%BB%87n%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20s%E1%BB%AD%20d%E1%BB%A5ng%20v%E1%BA%ADt%20th%E1%BB%83%20m%C3%A0%20kh%C3%B4ng%20c%E1%BA%A7n%20bi%E1%BA%BFt%20b%C3%AAn%20trong%20n%C3%B3%20c%C3%B3%20g%C3%AC.md). Tập hợp này được gọi là *giao diện*, vì cũng giống như những nút bấm trên màn hình quy định những gì ta có thể làm được với chương trình mà không cần biết bên trong có gì, những thứ trong tập hợp này quy định những gì ta có thể làm được với vật thể mà không cần biết bên trong có gì. Cái đầu tiên được gọi là GUI, cái sau được gọi là [API](../M%C3%B4%20%C4%91un/API%20l%C3%A0%20giao%20di%E1%BB%87n%20c%E1%BB%A7a%20m%E1%BB%99t%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh.md).

Ta hay nghĩ phải có vật thể trước đã rồi mới biết mình có thể làm gì với nó. Nhưng thường việc nghĩ trước về những thứ mình có thể làm với nó rồi mới tạo nó ra sẽ hiệu quả hơn. Tức là đầu tiên ta sẽ định nghĩa giao diện, từ đó tạo ra các lớp triển khai giao diện đó, rồi mới tạo vật thể từ các lớp đó sau:
```ts
interface GiaoDiện {...}
class Lớp implements GiaoDiện {...}
const vậtThể = new Lớp()
```