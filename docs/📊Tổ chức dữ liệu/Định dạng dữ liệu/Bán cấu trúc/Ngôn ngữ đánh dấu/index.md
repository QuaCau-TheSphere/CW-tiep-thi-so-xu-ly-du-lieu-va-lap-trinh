---
share: true
created: 2024-01-14T15:32
updated: 2024-08-25T21:02
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

