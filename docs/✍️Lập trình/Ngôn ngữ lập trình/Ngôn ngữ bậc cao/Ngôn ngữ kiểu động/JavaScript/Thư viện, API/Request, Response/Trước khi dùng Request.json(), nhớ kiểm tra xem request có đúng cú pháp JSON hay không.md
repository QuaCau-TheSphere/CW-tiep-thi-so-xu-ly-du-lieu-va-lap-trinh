---
share: true
created: 2023-10-30T14:29
updated: 2026-07-24T21:47
---
Khái niệm:: [JSON](JSON.md)
[Serialize là cách duy nhất để truyền dữ liệu từ máy phục vụ tới máy khách và ngược lại](../../../../../../Web/Framework%20(Preact,%20Fresh)/Server/Route,%20handler/Serialize%20l%C3%A0%20c%C3%A1ch%20duy%20nh%E1%BA%A5t%20%C4%91%E1%BB%83%20truy%E1%BB%81n%20d%E1%BB%AF%20li%E1%BB%87u%20t%E1%BB%AB%20m%C3%A1y%20ph%E1%BB%A5c%20v%E1%BB%A5%20t%E1%BB%9Bi%20m%C3%A1y%20kh%C3%A1ch%20v%C3%A0%20ng%C6%B0%E1%BB%A3c%20l%E1%BA%A1i.md). Cách serialize thông dụng là dùng `JSON.serialize()`. Nhưng sẽ có những lúc body không được tạo ra bằng cách đó, mà được tạo ra bằng việc nối chuỗi:
```
{"a": %x, "b": %y}
```

Nếu các biến `%x`, `%y` có thể chứa các ký tự có trong JSON mà không được escape trước, thì body không đúng cú pháp JSON, dẫn đến việc `req.json()` lúc chạy được lúc không. Nhưng ta lại không nghĩ là vấn đề nằm ở việc request body không đúng cú pháp, vì cứ đinh ninh là nó được `serialize()` đúng cách.

Có thể dùng [Zod để bắt lỗi kiểu do người dùng gửi](../../TypeScript/Th%C6%B0%20vi%E1%BB%87n,%20plugin/TS%20ch%E1%BB%89%20c%C3%B3%20th%E1%BB%83%20b%E1%BA%AFt%20l%E1%BB%97i%20ki%E1%BB%83u%20d%E1%BB%AF%20li%E1%BB%87u%20trong%20l%C3%BAc%20vi%E1%BA%BFt%20code.%20Zod%20gi%C3%BAp%20b%E1%BA%AFt%20l%E1%BB%97i%20ki%E1%BB%83u%20do%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng%20g%E1%BB%ADi.md)

Nguồn:: [Tự ngẫm nghĩ, trải nghiệm](../../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/T%E1%BB%B1%20ng%E1%BA%ABm%20ngh%C4%A9,%20tr%E1%BA%A3i%20nghi%E1%BB%87m.md)
