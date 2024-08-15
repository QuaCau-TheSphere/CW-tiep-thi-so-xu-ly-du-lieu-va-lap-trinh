---
share: true
created: 2023-10-24T18:26
updated: 2024-08-13T20:51
---
| Phương thức mã hoá | Số đơn vị mã (code unit) cần để biểu diễn một ký tự bất kỳ | Số byte cần cho một đơn vị mã |
| ------------------ | ---------------------------------------------------------- | ----------------------------- |
| UTF-8              | 1-4                                                        | 1                             |
| UTF-16             | 1-2                                                        | 2                             |
| UTF-32             | 1                                                          | 3                             |

Nguồn:: [Tìm hiểu Unicode](https://viblo.asia/p/tim-hieu-unicode-PwRkgVOXeEd)
Ví dụ, chữ `à` có 2 code point:
- `U+0061` cho chữ `a`
- `U+0300` cho dấu huyền

Có thể kiểm tra điều này bằng lệnh 
```
"à".length //kết quả là 2 😲
```
Tuy nhiên, `a` cũng có thể có 1 code point là `U+00E0`.
[UTF là cách thức để chuyển đổi từ điểm mã sang hệ nhị phân](./UTF%20l%C3%A0%20c%C3%A1ch%20th%E1%BB%A9c%20%C4%91%E1%BB%83%20chuy%E1%BB%83n%20%C4%91%E1%BB%95i%20t%E1%BB%AB%20%C4%91i%E1%BB%83m%20m%C3%A3%20sang%20h%E1%BB%87%20nh%E1%BB%8B%20ph%C3%A2n.md)

Đây cũng là lý do mà [JSON bắt phải đóng ngoặc kép tất cả các key](../../Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/JSON/JSON%20kh%C3%B4ng%20cho%20ph%C3%A9p%20%C4%91%E1%BB%83%20d%C6%B0%20d%E1%BA%A5u%20ph%E1%BA%A9y,%20kh%C3%B4ng%20c%C3%B3%20comment,%20b%E1%BA%AFt%20bu%E1%BB%99c%20ph%E1%BA%A3i%20d%C3%B9ng%20ngo%E1%BA%B7c%20k%C3%A9p,%20key%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%C3%B3ng%20trong%20ngo%E1%BA%B7c%20k%C3%A9p.md)