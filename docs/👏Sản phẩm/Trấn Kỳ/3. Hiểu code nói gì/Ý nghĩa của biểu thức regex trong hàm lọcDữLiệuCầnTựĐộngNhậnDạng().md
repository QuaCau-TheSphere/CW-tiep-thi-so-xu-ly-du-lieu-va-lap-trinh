---
share: true
created: 2023-09-19T23:42
updated: 2024-08-14T21:30
---
Biểu thức regex chỉ nhận những từ phía trước không có ký tự nào. Như vậy thì người dùng ghi `cát` thì script sẽ không tưởng lầm là có `cá`, ghi `đáo` thì sẽ không tưởng lầm là có `áo`.
 
 Đoạn ghi chú ngay sau đây dành cho người đã có hiểu biết về regex:
 - Ý tưởng ban đầu: dùng `\\b + từ + \\b`
 - Khó khăn của việc bắt regex tiếng Việt: `\b` không hỗ trợ cho Unicode. Để bắt Unicode đúng thì có thể thay bằng `\P{L}`, vốn tương đương với `\W`. Điều này đòi hỏi ở câu nhập phải thêm 2 khoảng trắng ở 2 bên. Xem thêm: [Tiếng Việt có 2 cách đặt dấu thanh, căn cứ vào thẩm mỹ hoặc vào ngữ âm](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Regex.%20Unicode,%20ti%E1%BA%BFng%20Vi%E1%BB%87t,%20emoji/Regex/Ti%E1%BA%BFng%20Vi%E1%BB%87t%20c%C3%B3%202%20c%C3%A1ch%20%C4%91%E1%BA%B7t%20d%E1%BA%A5u%20thanh,%20c%C4%83n%20c%E1%BB%A9%20v%C3%A0o%20th%E1%BA%A9m%20m%E1%BB%B9%20ho%E1%BA%B7c%20v%C3%A0o%20ng%E1%BB%AF%20%C3%A2m.md), [Ký tự unicode nếu dùng  ngay sau thì không được](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Regex.%20Unicode,%20ti%E1%BA%BFng%20Vi%E1%BB%87t,%20emoji/Regex/Kh%C3%B4ng%20d%C3%B9ng%20b%20ngay%20sau%20k%C3%BD%20t%E1%BB%B1%20unicode%20%C4%91%C6%B0%E1%BB%A3c.md)
 - Khó khăn của Fibery: `\P{L}` chạy rất lâu, mà Fibery chỉ cho thời gian chạy tối đa là 1000ms
 - Khó khăn của bài toán: không dùng `' ' + từ + ' '` được vì ngoài dấu cách ra còn có thể có nhiều dấu câu khác
- Sau một hồi loay hoay thì dùng phương pháp này:
```js
const khôngPhảiKýTựChữNào = `(\b|[^aAàÀảẢãÃáÁạẠăĂằẰẳẲẵẴắẮặẶâÂầẦẩẨẫẪấẤậẬbBcCdDđĐeEèÈẻẺẽẼéÉẹẸêÊềỀểỂễỄếẾệỆfFgGhHiIìÌỉỈĩĨíÍịỊjJkKlLmMnNoOòÒỏỎõÕóÓọỌôÔồỒổỔỗỖốỐộỘơƠờỜởỞỡỠớỚợỢpPqQrRsStTuUùÙủỦũŨúÚụỤưƯừỪửỬữỮứỨựỰvVwWxXyYỳỲỷỶỹỸýÝỵỴzZ0123456789-_])`
const regex = new RegExp(khôngPhảiKýTựChữNào + từ + khôngPhảiKýTựChữNào, `giu`);
```
- Sau đó khi cần dùng tới hàm `replace()` khi thay từ viết tắt thì chuyển lại sang dạng nhìn trước không có và nhìn sau không có (negative lookahead and negative lookbehind):
```js
const ANY_CHAR = '[aAàÀảẢãÃáÁạẠăĂằẰẳẲẵẴắẮặẶâÂầẦẩẨẫẪấẤậẬbBcCdDđĐeEèÈẻẺẽẼéÉẹẸêÊềỀểỂễỄếẾệỆfFgGhHiIìÌỉỈĩĨíÍịỊjJkKlLmMnNoOòÒỏỎõÕóÓọỌôÔồỒổỔỗỖốỐộỘơƠờỜởỞỡỠớỚợỢpPqQrRsStTuUùÙủỦũŨúÚụỤưƯừỪửỬữỮứỨựỰvVwWxXyYỳỲỷỶỹỸýÝỵỴzZ0123456789-_]'
const regex = new RegExp('(?<!' + ANY_CHAR + ')' + từ + '(?!' + ANY_CHAR + ')')
```
