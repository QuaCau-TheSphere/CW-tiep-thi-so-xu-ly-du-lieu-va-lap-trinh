---
share: true
created: 2023-10-30T14:29
updated: 2025-01-01T12:14
---
Các hệ mã khối, giống như tên gọi, thực hiện tính toán trên từng khối bit có kích thước cố định, thông thường là 64 hoặc 128 bit. Vì vậy khi đầu vào bản rõ có độ dài không là bội số của khối, ta cần phải thực hiện thao tác đệm (padding) sao cho số bit của đầu vào phải là bội số của khối.

Các hệ mã khối nổi tiếng đó là [DES](https://en.wikipedia.org/wiki/Data_Encryption_Standard) có kích thước khối là 64 (tức là mỗi lần mã hóa một khối bản rõ 64 bits và cho ra khối bản mã 64 bít) và kích thước khóa là 56 bits; [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) có kích thước khối là 128 bit, và kích thước khóa là 128, 192 hoặc 256bit.

Thông thường block cipher chậm hơn so với stream cipher, nhưng làm việc tốt với những khối dữ liệu đã biết trước kích thước, ví dụ mã hóa file, mã hóa tin nhắn trên các giao thức như là HTTP ...
Nguồn:: [Giới Thiệu Về Các Hệ Mã Hóa](https://viblo.asia/p/gioi-thieu-ve-cac-he-ma-hoa-OEqGj6rNG9bL)

[Cách máy tính hiểu ký tự khác với cách con người hiểu ký tự. Tốt nhất là nên dùng điểm mã khi nói về ký tự máy tính](../../%F0%9F%94%A0K%C3%BD%20t%E1%BB%B1,%20v%C4%83n%20b%E1%BA%A3n,%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/Ti%E1%BA%BFng%20Vi%E1%BB%87t,%20Unicode,%20emoji/L%C3%BD%20thuy%E1%BA%BFt%20Unicode/%C4%90i%E1%BB%83m%20m%C3%A3/C%C3%A1ch%20m%C3%A1y%20t%C3%ADnh%20hi%E1%BB%83u%20k%C3%BD%20t%E1%BB%B1%20kh%C3%A1c%20v%E1%BB%9Bi%20c%C3%A1ch%20con%20ng%C6%B0%E1%BB%9Di%20hi%E1%BB%83u%20k%C3%BD%20t%E1%BB%B1.%20T%E1%BB%91t%20nh%E1%BA%A5t%20l%C3%A0%20n%C3%AAn%20d%C3%B9ng%20%C4%91i%E1%BB%83m%20m%C3%A3%20khi%20n%C3%B3i%20v%E1%BB%81%20k%C3%BD%20t%E1%BB%B1%20m%C3%A1y%20t%C3%ADnh.md)