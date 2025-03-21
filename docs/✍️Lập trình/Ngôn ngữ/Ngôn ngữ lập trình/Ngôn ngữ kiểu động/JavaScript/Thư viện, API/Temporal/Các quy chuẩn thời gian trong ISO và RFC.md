---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
description: Viết 2020-12-09T16:09:53+00:00 đáp ứng cả ISO 8601 và RFC 3339
---
Viết `2020-12-09T16:09:53+00:00` đáp ứng cả ISO 8601 và RFC 3339

| Mô tả                             | Ví dụ                       | ISO 8601 | RFC 3339 |
| --------------------------------- | --------------------------- | -------- | ------- |
| Chuẩn                             | `2020-12-09T16:09:53+00:00` | ✔        | ✔       |
| Dùng khoảng cách giữa ngày và giờ | `2020-12-09 16:09:53+00:00` | ❌       | ✔       |
| Dấu âm trong time offset          | `2020-12-09T16:09:53-00:00` | ❌       | ✔       |
| Bỏ dấu ngang và hai chấm          | `20201209T160953Z`          | ✔        | ❌      |

Nguồn:: [Stack Overflow](../../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [datetime - What's the difference between ISO 8601 and RFC 3339 Date Formats? - Stack Overflow](https://stackoverflow.com/a/65221179/3416774)

[Giờ UTC là giờ luôn giống nhau ở bất cứ nơi đâu. Nó là phiên bản sau của giờ GMT](./Gi%E1%BB%9D%20UTC%20l%C3%A0%20gi%E1%BB%9D%20lu%C3%B4n%20gi%E1%BB%91ng%20nhau%20%E1%BB%9F%20b%E1%BA%A5t%20c%E1%BB%A9%20n%C6%A1i%20%C4%91%C3%A2u.%20N%C3%B3%20l%C3%A0%20phi%C3%AAn%20b%E1%BA%A3n%20sau%20c%E1%BB%A7a%20gi%E1%BB%9D%20GMT.md)
[RFC 9557](https://datatracker.ietf.org/doc/html/rfc9557) là cái mới nhất. [Cả ISO 8601 và RFC 3339 đều là tập con của nó](https://tc39.es/proposal-temporal/docs/plaindate.html#static-methods).