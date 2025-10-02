---
share: true
created: 2024-01-14T15:32
updated: 2025-10-02T14:50
title: Ngôn ngữ đánh dấu
---

| Tối ưu cho... →<br>Ngôn ngữ đánh dấu ↓ | ...cho con người đọc và viết | ...cho việc khai báo metadata | ...cho việc viết tập tin cấu hình | ...cho việc truyền dữ liệu |
| -------------------------------------- | ---------------------------- | ----------------------------- | --------------------------------- | -------------------------- |
| YAML                                   | ✔                            | ✔                             | ❌                                | ❌                         |
| XML                                    | ❌                           | ✔                             | ❌                                | ✔                          |
| TOML                                   | ✔                            | ❌                            | ✔                                 | ❌                         |
| JSON                                   | ❌                           | ❌                            | ❌                                | ✔                          |
| JSONC/JWCC                             | ❌                           | ❌                            | ✔                                 | ✔                          |

Những thứ mà không tối ưu cho con người đọc và viết thì nên để máy tự in ra. Chỉnh sửa trực tiếp dễ gây lỗi. Hoặc ít nhất là nên viết trong parser/validator để nó báo lỗi ngay cho mình.

[Chữ ML trong HTML, XML, YAML, TOML là viết tắt của markup language](./Ch%E1%BB%AF%20ML%20trong%20HTML,%20XML,%20YAML,%20TOML%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a%20markup%20language.md)
[The yaml document from hell](https://ruudvanasseldonk.com/2023/01/11/the-yaml-document-from-hell)

- [Chữ ML trong HTML, XML, YAML, TOML là viết tắt của markup language](./Ch%E1%BB%AF%20ML%20trong%20HTML,%20XML,%20YAML,%20TOML%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a%20markup%20language.md)
- [Ngôn ngữ đánh dấu mạnh có thể sử dụng cho dữ liệu có cấu trúc vì spec của nó có nói rõ dữ liệu nên được lưu thế nào](./Ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u%20m%E1%BA%A1nh%20c%C3%B3%20th%E1%BB%83%20s%E1%BB%AD%20d%E1%BB%A5ng%20cho%20d%E1%BB%AF%20li%E1%BB%87u%20c%C3%B3%20c%E1%BA%A5u%20tr%C3%BAc%20v%C3%AC%20spec%20c%E1%BB%A7a%20n%C3%B3%20c%C3%B3%20n%C3%B3i%20r%C3%B5%20d%E1%BB%AF%20li%E1%BB%87u%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20l%C6%B0u%20th%E1%BA%BF%20n%C3%A0o.md)
- [RDF có thể được biểu diễn bằng JSON-LD](./RDF%20c%C3%B3%20th%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20bi%E1%BB%83u%20di%E1%BB%85n%20b%E1%BA%B1ng%20JSON-LD.md)
- [XML là dạng dữ liệu bán cấu trúc](./XML%20l%C3%A0%20d%E1%BA%A1ng%20d%E1%BB%AF%20li%E1%BB%87u%20b%C3%A1n%20c%E1%BA%A5u%20tr%C3%BAc.md)
