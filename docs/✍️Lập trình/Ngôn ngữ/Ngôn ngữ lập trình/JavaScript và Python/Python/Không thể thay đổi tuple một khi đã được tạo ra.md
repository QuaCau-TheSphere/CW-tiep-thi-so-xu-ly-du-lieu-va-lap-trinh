---
share: true
created: 2023-09-22T21:50
updated: 2024-04-26T21:34
---
Qua các nội dung của bài này và bài học trước đó ([list trong Python](https://tuhocict.com/kieu-danh-sach-list-trong-python/)) bạn có thể thấy có rất nhiều điểm tương tự giữa tuple và list. Tuy nhiên, tuple và list có những điểm phân biệt rất rõ ràng. Sự khác biệt này quyết định giá trị sử dụng của từng kiểu dữ liệu.

Thứ nhất, list là kiểu dữ liệu _khả biến_ (mutable) trong khi tuple là kiểu dữ liệu _bất biến_ (immutable). Nghĩa là, một khi đã được tạo ra trong bộ nhớ, list có thể thay đổi còn tuple không thể thay đổi. Các thao tác biến đổi trên tuple sẽ đều tạo ra object mới chứ không thay đổi object sẵn có.

Từ khía cạnh nào đó có thể hình dung tuple là phiên bản chỉ đọc thu gọn của list.

Với đặc thù trên, list thường dùng làm kho dữ liệu cho chương trình. Ví dụ, bạn có thể đọc dữ liệu từ file vào list, thực hiện các biến đổi trên list và lưu trở lại file. Dữ liệu lưu trong list được xử lý linh hoạt uyển chuyển hơn. Bạn không thể sử dụng tuple cho mục đích này.

Trong khi đó, tuple được sử dụng để truyền dữ liệu trong chương trình. Ví dụ, nếu một hàm cần trả lại nhiều kết quả, nó có thể trả về một tuple. Kết quả trả về ở dạng tuple nhẹ, nhanh và an toàn hơn. Ở đây mặc dù có thể dùng list nhưng không khuyến khích.

Mặc dù list cho phép lưu trữ dữ liệu thuộc nhiều kiểu khác nhau, người ta thường dùng list để lưu dữ liệu có cùng kiểu. Trong khi đó, tuple thường được dùng để lưu trữ kết quả thuộc các kiểu khác biệt để truyền qua lại trong chương trình.

Ví dụ, nếu khách hàng có các thông tin về họ tên, email, số điện thoại, địa chỉ. Danh sách khách hàng (tập hợp bản ghi) nên được lưu trong list. Nếu cần truyền thông tin về một khách hàng (dữ liệu 1 bản ghi, ví dụ, trả về từ hàm) thì nên dùng tuple chứa các thông tin của khách hàng đó.

Nguồn:: [tuhocict](../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/tuhocict.md), [Kiểu dữ liệu tuple trong Python | Tự học ICT](https://tuhocict.com/kieu-du-lieu-tuple-trong-python/)
[Tuple là mảng nhưng không thay đổi được số lượng phần tử](./Tuple%20l%C3%A0%20m%E1%BA%A3ng%20nh%C6%B0ng%20kh%C3%B4ng%20thay%20%C4%91%E1%BB%95i%20%C4%91%C6%B0%E1%BB%A3c%20s%E1%BB%91%20l%C6%B0%E1%BB%A3ng%20ph%E1%BA%A7n%20t%E1%BB%AD.md)