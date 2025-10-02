---
share: true
created: 2023-09-22T14:54
updated: 2025-10-02T15:38
title: Lý thuyết Unicode
---
- \-: 
    - [Không gian mã là không gian chứa tất cả các điểm mã của Unicode](./Kh%C3%B4ng%20gian%20m%C3%A3%20l%C3%A0%20kh%C3%B4ng%20gian%20ch%E1%BB%A9a%20t%E1%BA%A5t%20c%E1%BA%A3%20c%C3%A1c%20%C4%91i%E1%BB%83m%20m%C3%A3%20c%E1%BB%A7a%20Unicode.md)
    - [Kể cả khi viết nội dung bằng ngôn ngữ khác thì số ký tự ASCII vẫn nhiều hơn nhiều so với số ký tự phi ASCII](./K%E1%BB%83%20c%E1%BA%A3%20khi%20vi%E1%BA%BFt%20n%E1%BB%99i%20dung%20b%E1%BA%B1ng%20ng%C3%B4n%20ng%E1%BB%AF%20kh%C3%A1c%20th%C3%AC%20s%E1%BB%91%20k%C3%BD%20t%E1%BB%B1%20ASCII%20v%E1%BA%ABn%20nhi%E1%BB%81u%20h%C6%A1n%20nhi%E1%BB%81u%20so%20v%E1%BB%9Bi%20s%E1%BB%91%20k%C3%BD%20t%E1%BB%B1%20phi%20ASCII.md)
    - [Lý thuyết Unicode](index.md)
    - [Những số bắt đầu bằng 0x là những số hex](./Nh%E1%BB%AFng%20s%E1%BB%91%20b%E1%BA%AFt%20%C4%91%E1%BA%A7u%20b%E1%BA%B1ng%200x%20l%C3%A0%20nh%E1%BB%AFng%20s%E1%BB%91%20hex.md)
    - [Tuỳ vào phương thức mã hoá mà mỗi ký tự Unicode sẽ được biểu diễn bởi 1-4 đơn vị mã, 1-2 đơn vị mã, hoặc chỉ một đơn vị mã duy nhất](./Tu%E1%BB%B3%20v%C3%A0o%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20m%C3%A3%20ho%C3%A1%20m%C3%A0%20m%E1%BB%97i%20k%C3%BD%20t%E1%BB%B1%20Unicode%20s%E1%BA%BD%20%C4%91%C6%B0%E1%BB%A3c%20bi%E1%BB%83u%20di%E1%BB%85n%20b%E1%BB%9Fi%201-4%20%C4%91%C6%A1n%20v%E1%BB%8B%20m%C3%A3,%201-2%20%C4%91%C6%A1n%20v%E1%BB%8B%20m%C3%A3,%20ho%E1%BA%B7c%20ch%E1%BB%89%20m%E1%BB%99t%20%C4%91%C6%A1n%20v%E1%BB%8B%20m%C3%A3%20duy%20nh%E1%BA%A5t.md)
    - [Điểm mã liên quan đến việc con người đánh số thứ tự của ký tự thế nào. Đơn vị mã liên quan đến việc máy tính dùng phương thức nào để biết tìm ký tự đó ở đâu](./%C4%90i%E1%BB%83m%20m%C3%A3%20li%C3%AAn%20quan%20%C4%91%E1%BA%BFn%20vi%E1%BB%87c%20con%20ng%C6%B0%E1%BB%9Di%20%C4%91%C3%A1nh%20s%E1%BB%91%20th%E1%BB%A9%20t%E1%BB%B1%20c%E1%BB%A7a%20k%C3%BD%20t%E1%BB%B1%20th%E1%BA%BF%20n%C3%A0o.%20%C4%90%C6%A1n%20v%E1%BB%8B%20m%C3%A3%20li%C3%AAn%20quan%20%C4%91%E1%BA%BFn%20vi%E1%BB%87c%20m%C3%A1y%20t%C3%ADnh%20d%C3%B9ng%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20n%C3%A0o%20%C4%91%E1%BB%83%20bi%E1%BA%BFt%20t%C3%ACm%20k%C3%BD%20t%E1%BB%B1%20%C4%91%C3%B3%20%E1%BB%9F%20%C4%91%C3%A2u.md)

- Điểm mã: 
    - [Các ký tự ASCII có 1 điểm mã](./%C4%90i%E1%BB%83m%20m%C3%A3/C%C3%A1c%20k%C3%BD%20t%E1%BB%B1%20ASCII%20c%C3%B3%201%20%C4%91i%E1%BB%83m%20m%C3%A3.md)
    - [Cách máy tính hiểu ký tự khác với cách con người hiểu ký tự. Tốt nhất là nên dùng điểm mã khi nói về ký tự máy tính](./%C4%90i%E1%BB%83m%20m%C3%A3/C%C3%A1ch%20m%C3%A1y%20t%C3%ADnh%20hi%E1%BB%83u%20k%C3%BD%20t%E1%BB%B1%20kh%C3%A1c%20v%E1%BB%9Bi%20c%C3%A1ch%20con%20ng%C6%B0%E1%BB%9Di%20hi%E1%BB%83u%20k%C3%BD%20t%E1%BB%B1.%20T%E1%BB%91t%20nh%E1%BA%A5t%20l%C3%A0%20n%C3%AAn%20d%C3%B9ng%20%C4%91i%E1%BB%83m%20m%C3%A3%20khi%20n%C3%B3i%20v%E1%BB%81%20k%C3%BD%20t%E1%BB%B1%20m%C3%A1y%20t%C3%ADnh.md)
    - [Mỗi điểm mã được biểu diễn dưới dạng U+XXYYYY](./%C4%90i%E1%BB%83m%20m%C3%A3/M%E1%BB%97i%20%C4%91i%E1%BB%83m%20m%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20bi%E1%BB%83u%20di%E1%BB%85n%20d%C6%B0%E1%BB%9Bi%20d%E1%BA%A1ng%20U+XXYYYY.md)
    - [Unicode chia thành 17 plane, mỗi plane chứa 65,536 (= 16⁴) điểm mã](./%C4%90i%E1%BB%83m%20m%C3%A3/Unicode%20chia%20th%C3%A0nh%2017%20plane,%20m%E1%BB%97i%20plane%20ch%E1%BB%A9a%2065,536%20(=%2016%E2%81%B4)%20%C4%91i%E1%BB%83m%20m%C3%A3.md)
    - [UTF là cách thức để chuyển đổi từ điểm mã sang hệ nhị phân](./%C4%90i%E1%BB%83m%20m%C3%A3/UTF%20l%C3%A0%20c%C3%A1ch%20th%E1%BB%A9c%20%C4%91%E1%BB%83%20chuy%E1%BB%83n%20%C4%91%E1%BB%95i%20t%E1%BB%AB%20%C4%91i%E1%BB%83m%20m%C3%A3%20sang%20h%E1%BB%87%20nh%E1%BB%8B%20ph%C3%A2n.md)
    - [Điểm mã không phải là cách để máy tính lưu ký tự](./%C4%90i%E1%BB%83m%20m%C3%A3/%C4%90i%E1%BB%83m%20m%C3%A3%20kh%C3%B4ng%20ph%E1%BA%A3i%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20m%C3%A1y%20t%C3%ADnh%20l%C6%B0u%20k%C3%BD%20t%E1%BB%B1.md)



<iframe width="560" height="315" src="https://www.youtube.com/embed/gd5uJ7Nlvvo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
![Accidental Emoji Expert: Tom Scott at An Evening of Unnecessary Detail](https://youtu.be/5OPkGQoPeHk?si=Y2mZenbD8oXLf8fA) 
