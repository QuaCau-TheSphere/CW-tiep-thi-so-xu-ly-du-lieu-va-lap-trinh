---
share: true
created: 2023-10-30T14:29
updated: 2024-12-07T15:45
description: 2020-12-09T16:09:53+00:00 đáp ứng cả ISO và RFC
---
| Mô tả                             | Ví dụ                       | ISO 8601 | RFC3339 |
| --------------------------------- | --------------------------- | -------- | ------- |
| Chuẩn                             | `2020-12-09T16:09:53+00:00` | ✔        | ✔       |
| Dùng khoảng cách giữa ngày và giờ | `2020-12-09 16:09:53+00:00` | ❌       | ✔       |
| Dấu âm trong time offset          | `2020-12-09T16:09:53-00:00` | ❌       | ✔       |
| Bỏ dấu ngang và hai chấm          | `20201209T160953Z`          | ✔        | ❌      |

Nên dùng RFC3339. Nó mới được cập nhật thành [RFC 9557](https://datatracker.ietf.org/doc/html/rfc9557)
Nguồn:: [Stack Overflow](../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [datetime - What's the difference between ISO 8601 and RFC 3339 Date Formats? - Stack Overflow](https://stackoverflow.com/a/65221179/3416774)