---
share: true
created: 2023-10-30T14:29
updated: 2024-06-02T16:43
---
Vì nếu xử lý và cần trả về một vật thể có chứ DOM, thì việc phải dùng `return Response.json()` sẽ gây lỗi circular

Nguồn:: [Tự ngẫm nghĩ, trải nghiệm](../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/T%E1%BB%B1%20ng%E1%BA%ABm%20ngh%C4%A9,%20tr%E1%BA%A3i%20nghi%E1%BB%87m.md)