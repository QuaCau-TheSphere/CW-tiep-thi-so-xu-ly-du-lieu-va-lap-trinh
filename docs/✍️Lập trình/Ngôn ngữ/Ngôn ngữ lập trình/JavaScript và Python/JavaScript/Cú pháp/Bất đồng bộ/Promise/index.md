---
share: true
created: 2023-10-30T14:29
updated: 2024-11-25T16:41
title: Promise
---
- \-: 
    - [Promise chỉ là một vật thể để việc lập trình được tiện hơn, không phải là một tính năng mà những phiên bản JS trước không làm được](./Promise%20ch%E1%BB%89%20l%C3%A0%20m%E1%BB%99t%20v%E1%BA%ADt%20th%E1%BB%83%20%C4%91%E1%BB%83%20vi%E1%BB%87c%20l%E1%BA%ADp%20tr%C3%ACnh%20%C4%91%C6%B0%E1%BB%A3c%20ti%E1%BB%87n%20h%C6%A1n,%20kh%C3%B4ng%20ph%E1%BA%A3i%20l%C3%A0%20m%E1%BB%99t%20t%C3%ADnh%20n%C4%83ng%20m%C3%A0%20nh%E1%BB%AFng%20phi%C3%AAn%20b%E1%BA%A3n%20JS%20tr%C6%B0%E1%BB%9Bc%20kh%C3%B4ng%20l%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c.md)
    - [Promise được sinh ra là để không phải dùng if lồng quá nhiều](./Promise%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20l%C3%A0%20%C4%91%E1%BB%83%20kh%C3%B4ng%20ph%E1%BA%A3i%20d%C3%B9ng%20if%20l%E1%BB%93ng%20qu%C3%A1%20nhi%E1%BB%81u.md)
    - [Promise](index.md)
    - [Thực chất promise không giải quyết được chuyện lồng, vì promise cũng lồng vào nhau như if thôi. Thứ nó giải quyết là việc các giá trị trả về từ promise trông như không lồng vào nhau gì cả](./Th%E1%BB%B1c%20ch%E1%BA%A5t%20promise%20kh%C3%B4ng%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20%C4%91%C6%B0%E1%BB%A3c%20chuy%E1%BB%87n%20l%E1%BB%93ng,%20v%C3%AC%20promise%20c%C5%A9ng%20l%E1%BB%93ng%20v%C3%A0o%20nhau%20nh%C6%B0%20if%20th%C3%B4i.%20Th%E1%BB%A9%20n%C3%B3%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20l%C3%A0%20vi%E1%BB%87c%20c%C3%A1c%20gi%C3%A1%20tr%E1%BB%8B%20tr%E1%BA%A3%20v%E1%BB%81%20t%E1%BB%AB%20promise%20tr%C3%B4ng%20nh%C6%B0%20kh%C3%B4ng%20l%E1%BB%93ng%20v%C3%A0o%20nhau%20g%C3%AC%20c%E1%BA%A3.md)

- Lớp Promise: 
    - [resolve, reject là hai hàm được JS cung cấp sẵn. Chúng được dùng làm đối số cho hàm thực thi](./L%E1%BB%9Bp%20Promise/resolve,%20reject%20l%C3%A0%20hai%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20JS%20cung%20c%E1%BA%A5p%20s%E1%BA%B5n.%20Ch%C3%BAng%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20l%C3%A0m%20%C4%91%E1%BB%91i%20s%E1%BB%91%20cho%20h%C3%A0m%20th%E1%BB%B1c%20thi.md)
    - [Đối số của Promise là một hàm. Nó được gọi là hàm thực thi (executor)](./L%E1%BB%9Bp%20Promise/%C4%90%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20Promise%20l%C3%A0%20m%E1%BB%99t%20h%C3%A0m.%20N%C3%B3%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20l%C3%A0%20h%C3%A0m%20th%E1%BB%B1c%20thi%20(executor).md)

- Vật thể promise: 
    - [Vật thể promise có 2 thuộc tính là state và result, và 3 phương thức là then, catch, và finally](./V%E1%BA%ADt%20th%E1%BB%83%20promise/V%E1%BA%ADt%20th%E1%BB%83%20promise%20c%C3%B3%202%20thu%E1%BB%99c%20t%C3%ADnh%20l%C3%A0%20state%20v%C3%A0%20result,%20v%C3%A0%203%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20l%C3%A0%20then,%20catch,%20v%C3%A0%20finally.md)
    - [Hàm cần gọi phải ở trong then](./V%E1%BA%ADt%20th%E1%BB%83%20promise/H%C3%A0m%20c%E1%BA%A7n%20g%E1%BB%8Di%20ph%E1%BA%A3i%20%E1%BB%9F%20trong%20then.md)
    - [Để lấy được giá trị state và result của promise, cần dùng các phương thức then và catch của nó](./V%E1%BA%ADt%20th%E1%BB%83%20promise/%C4%90%E1%BB%83%20l%E1%BA%A5y%20%C4%91%C6%B0%E1%BB%A3c%20gi%C3%A1%20tr%E1%BB%8B%20state%20v%C3%A0%20result%20c%E1%BB%A7a%20promise,%20c%E1%BA%A7n%20d%C3%B9ng%20c%C3%A1c%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20then%20v%C3%A0%20catch%20c%E1%BB%A7a%20n%C3%B3.md)

