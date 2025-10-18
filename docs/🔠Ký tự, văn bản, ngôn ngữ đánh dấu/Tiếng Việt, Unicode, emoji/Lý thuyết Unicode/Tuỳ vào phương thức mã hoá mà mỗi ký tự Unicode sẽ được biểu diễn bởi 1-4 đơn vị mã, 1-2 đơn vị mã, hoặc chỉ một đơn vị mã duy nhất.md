---
share: true
created: 2023-10-24T18:26
updated: 2025-10-12T15:34
---
| Phương thức mã hoá | Số đơn vị mã (code unit) cần để biểu diễn một ký tự bất kỳ | Số byte cần cho một đơn vị mã |
| ------------------ | ---------------------------------------------------------- | ----------------------------- |
| UTF-8              | 1-4                                                        | 1                             |
| UTF-16             | 1-2                                                        | 2                             |
| UTF-32             | 1                                                          | 3                             |

Nguồn:: [Tìm hiểu Unicode](https://viblo.asia/p/tim-hieu-unicode-PwRkgVOXeEd)
Ví dụ, chữ `à` có 2 điểm mã:
- `U+0061` cho chữ `a`
- `U+0300` cho dấu huyền

Có thể kiểm tra điều này bằng lệnh 
```
"à".length //kết quả là 2 😲
```
Tuy nhiên, `à` cũng có thể có 1 điểm mã là `U+00E0`.
[UTF là cách thức để chuyển đổi từ điểm mã sang hệ nhị phân](./%C4%90i%E1%BB%83m%20m%C3%A3/UTF%20l%C3%A0%20c%C3%A1ch%20th%E1%BB%A9c%20%C4%91%E1%BB%83%20chuy%E1%BB%83n%20%C4%91%E1%BB%95i%20t%E1%BB%AB%20%C4%91i%E1%BB%83m%20m%C3%A3%20sang%20h%E1%BB%87%20nh%E1%BB%8B%20ph%C3%A2n.md). [Mỗi điểm mã được biểu diễn dưới dạng U+XXYYYY](./%C4%90i%E1%BB%83m%20m%C3%A3/M%E1%BB%97i%20%C4%91i%E1%BB%83m%20m%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20bi%E1%BB%83u%20di%E1%BB%85n%20d%C6%B0%E1%BB%9Bi%20d%E1%BA%A1ng%20U+XXYYYY.md)

```js
const message = "Một thông điệp";
const encoder = new TextEncoder();
const encoded = encoder.encode(message);
console.log(encoded)
// Uint8Array(20) [
//   77, 225, 187, 153, 116,  32,
//  116, 104, 195, 180, 110, 103,
//   32, 196, 145, 105, 225, 187,
//  135, 112
// ]

const decoder = new TextDecoder(); 
const u8arr = new Uint8Array(encoded);
const decoded = decoder.decode(u8arr)
console.log(decoded);
// Một thông điệp
```

Đây cũng là lý do mà [JSON bắt phải đóng ngoặc kép tất cả các thuộc tính](../../../%F0%9F%97%84%EF%B8%8FT%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%8Bnh%20d%E1%BA%A1ng%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%8Bnh%20d%E1%BA%A1ng%20v%C4%83n%20b%E1%BA%A3n/JSON/JSON%20kh%C3%B4ng%20cho%20ph%C3%A9p%20%C4%91%E1%BB%83%20d%C6%B0%20d%E1%BA%A5u%20ph%E1%BA%A9y,%20kh%C3%B4ng%20c%C3%B3%20comment,%20thu%E1%BB%99c%20t%C3%ADnh%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%C3%B3ng%20trong%20ngo%E1%BA%B7c%20k%C3%A9p.md), để khỏi phải quan tâm xem "ký tự" là gì.