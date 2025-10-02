---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
alias:
  - markdown, URL, domain xử lý
---
|                             | Cho dùng dấu cách | Ký tự `%` | Các ký tự phi ASCII |
| --------------------------- | ----------------- | --------- | ------------------- |
| Markdown                    | ❌                |           | ✔                   |
| YAML                        | ❌                |           | ✔                   |
| URL                         | ✔                 | ❌        | ✔                   |
| Domain                      | ✔                 |           | ✔                   |
| Thuộc tính `src` trong HMTL | ✔                 |           | ✔                   |
| Query                       | ❌                |           | ✔                   |
| Windows path                | ✔                 | ✔         | ✔                   |
| Linux path                  | ✔                 |           | ✔                   |
| Mac path                    | ✔                 |           | ✔                   |
| Docker                      | ❌                |           | ❌                    |

Nên tránh dùng ký tự `%` trong tên tập tin, nhất là nếu sau này sẽ biến thành web. Vì dấu này chính là dấu để encode, nên không như những ký tự khác, khi decode sẽ gặp lỗi
[What is the difference between decodeURIComponent and decodeURI?](https://stackoverflow.com/q/747641/3416774)
[Sự khác biệt giữa Windows và Android, Mac trong tên file](./S%E1%BB%B1%20kh%C3%A1c%20bi%E1%BB%87t%20gi%E1%BB%AFa%20Windows%20v%C3%A0%20Android,%20Mac%20trong%20t%C3%AAn%20file.md)

[Các ký tự ASCII có 1 điểm mã](../../%F0%9F%94%A0K%C3%BD%20t%E1%BB%B1,%20v%C4%83n%20b%E1%BA%A3n,%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/Ti%E1%BA%BFng%20Vi%E1%BB%87t,%20Unicode,%20emoji/L%C3%BD%20thuy%E1%BA%BFt%20Unicode/%C4%90i%E1%BB%83m%20m%C3%A3/C%C3%A1c%20k%C3%BD%20t%E1%BB%B1%20ASCII%20c%C3%B3%201%20%C4%91i%E1%BB%83m%20m%C3%A3.md)