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

- [Chữ ML trong HTML, XML, YAML, TOML là viết tắt của markup language](./Ch%E1%BB%AF%20ML%20trong%20HTML,%20XML,%20YAML,%20TOML%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a%20markup%20language.md)
- [JSON hữu ích trong việc truyền dữ liệu vì nó hướng đến việc trở thành phần giao của các ngôn ngữ, chứ không phải phần hợp của chúng](./JSON/JSON%20h%E1%BB%AFu%20%C3%ADch%20trong%20vi%E1%BB%87c%20truy%E1%BB%81n%20d%E1%BB%AF%20li%E1%BB%87u%20v%C3%AC%20n%C3%B3%20h%C6%B0%E1%BB%9Bng%20%C4%91%E1%BA%BFn%20vi%E1%BB%87c%20tr%E1%BB%9F%20th%C3%A0nh%20ph%E1%BA%A7n%20giao%20c%E1%BB%A7a%20c%C3%A1c%20ng%C3%B4n%20ng%E1%BB%AF,%20ch%E1%BB%A9%20kh%C3%B4ng%20ph%E1%BA%A3i%20ph%E1%BA%A7n%20h%E1%BB%A3p%20c%E1%BB%A7a%20ch%C3%BAng.md)
- [JSON không cho phép để dư dấu phẩy, không có comment, bắt buộc phải dùng ngoặc kép, key phải được đóng trong ngoặc kép](./JSON/JSON%20kh%C3%B4ng%20cho%20ph%C3%A9p%20%C4%91%E1%BB%83%20d%C6%B0%20d%E1%BA%A5u%20ph%E1%BA%A9y,%20kh%C3%B4ng%20c%C3%B3%20comment,%20b%E1%BA%AFt%20bu%E1%BB%99c%20ph%E1%BA%A3i%20d%C3%B9ng%20ngo%E1%BA%B7c%20k%C3%A9p,%20key%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%C3%B3ng%20trong%20ngo%E1%BA%B7c%20k%C3%A9p.md)
- [JSON là cách để biểu diễn vật thể ra chữ, chứ tự nó không phải là vật thể](./JSON/JSON%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20bi%E1%BB%83u%20di%E1%BB%85n%20v%E1%BA%ADt%20th%E1%BB%83%20ra%20ch%E1%BB%AF,%20ch%E1%BB%A9%20t%E1%BB%B1%20n%C3%B3%20kh%C3%B4ng%20ph%E1%BA%A3i%20l%C3%A0%20v%E1%BA%ADt%20th%E1%BB%83.md)
- [JSON Schema dùng để đảm bảo file JSON được viết đúng](./JSON/JSON%20Schema%20d%C3%B9ng%20%C4%91%E1%BB%83%20%C4%91%E1%BA%A3m%20b%E1%BA%A3o%20file%20JSON%20%C4%91%C6%B0%E1%BB%A3c%20vi%E1%BA%BFt%20%C4%91%C3%BAng.md)
- [Chuyển từ YAML sang JSON](./YAML/Chuy%E1%BB%83n%20t%E1%BB%AB%20YAML%20sang%20JSON.md)
- [YAML thì để con người dễ đọc, còn JSON là để máy dễ đọc](./YAML/YAML%20th%C3%AC%20%C4%91%E1%BB%83%20con%20ng%C6%B0%E1%BB%9Di%20d%E1%BB%85%20%C4%91%E1%BB%8Dc,%20c%C3%B2n%20JSON%20l%C3%A0%20%C4%91%E1%BB%83%20m%C3%A1y%20d%E1%BB%85%20%C4%91%E1%BB%8Dc.md)
- [YAML được sinh ra để con người đọc và viết metadata một cách dễ dàng](./YAML/YAML%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20%C4%91%E1%BB%83%20con%20ng%C6%B0%E1%BB%9Di%20%C4%91%E1%BB%8Dc%20v%C3%A0%20vi%E1%BA%BFt%20metadata%20m%E1%BB%99t%20c%C3%A1ch%20d%E1%BB%85%20d%C3%A0ng.md)
