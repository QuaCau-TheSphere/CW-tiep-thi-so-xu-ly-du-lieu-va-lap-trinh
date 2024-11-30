---
share: true
created: 2023-10-30T14:29
updated: 2024-11-30T13:38
---
Vì nếu xử lý và cần trả về một vật thể có chứa DOM, thì việc phải dùng `return Response.json()` sẽ gây lỗi circular
[DOM là kết quả của việc phân tích cú pháp một tài liệu HTML cộng với](../DOM/DOM%20l%C3%A0%20k%E1%BA%BFt%20qu%E1%BA%A3%20c%E1%BB%A7a%20vi%E1%BB%87c%20ph%C3%A2n%20t%C3%ADch%20c%C3%BA%20ph%C3%A1p%20m%E1%BB%99t%20t%C3%A0i%20li%E1%BB%87u%20HTML%20c%E1%BB%99ng%20v%E1%BB%9Bi.md)
Nguồn:: [Tự ngẫm nghĩ, trải nghiệm](../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/T%E1%BB%B1%20ng%E1%BA%ABm%20ngh%C4%A9,%20tr%E1%BA%A3i%20nghi%E1%BB%87m.md)