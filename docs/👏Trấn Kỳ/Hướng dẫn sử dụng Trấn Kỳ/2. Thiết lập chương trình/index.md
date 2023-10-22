---
share: true
created: 2023-08-25T14:20
updated: 2023-10-21T23:42
---
Phần bạn cần chỉnh sửa nằm trong thư mục `A. Cấu hình`. Đây là một tệp ở định dạng YAML. Cấu trúc cơ bản của nó như sau:
```yaml
Khai báo:
  - Tên chiều: 
	Dữ liệu tự nhận dạng: 
    Ký tự để nhập trực tiếp:
      Từ:
      Nhãn:
    Tên gọi đầu ra:
      Từ: 
      Nhãn:  
Fibery:
Keep
```

> [!Attention] Lưu ý: Số khoảng trắng thụt đầu dòng cần phải chính xác
>  Bạn chỉ được dùng **dấu cách** để tạo khoảng trắng chứ không được dùng **tab**

# Các chiều đặc biệt
Nếu bạn khai báo một trong những chiều này thì cần lưu ý thêm:
## `Món đồ`
- Những món đồ cùng nhãn thì chỉ hiển thị một nhãn. Ví dụ: nếu câu nhập là `thịt 50k, cá 20k` thì nhãn sẽ là `đồ ăn`, không phải `đồ ăn, đồ ăn`
- Nếu trong câu nhập có nhiều món đồ cùng nhãn thì chỉ lấy một nhãn

## `Phương thức thanh toán`
Nếu trong câu nhập vào có nhiều phương thức thanh toán thì chỉ lấy cái cuối cùng, còn tất cả những cái phía trước chỉ là thông tin. Ví dụ, nếu câu nhập là `đáo hạn shinhan bằng vcb`

## `Số tiền`
- Số tiền sẽ là các số có đuôi là tr, k, đ, d. Nếu không có đơn vị thì sẽ không xem là số tiền
- Nếu có nhiều giá trị thì sẽ lấy tổng. Nếu muốn chọn một giá trị nào đó thì thêm dấu bằng phía trước nó (`＝`)

  Ví dụ:
  - `cá 50k thịt 40k` → `90000`.
  - `cá 50k thịt = 40k`→ `40000`
- Dấu thập phân là dấu chấm (`.`). Bạn có thể dùng dấu phẩy (`,`) để cách các con số để dễ đọc. Nó sẽ được bỏ đi. Ví dụ: 1.2tr, 3,400k, 123,456,700đ, 123,456,700d.


# Một số phím tắt thường dùng cho việc đọc hiểu code

| Phím tắt         | Chức năng                                                 |
| ---------------- | --------------------------------------------------------- |
| Alt + Z          | Word wrap                                                 |
| Ctrl + Shift + . | Mở danh sách các hàm và biến                              |
| F12              | Đến nhanh những nơi hàm hoặc biến được sử dụng            |
| Ctrl + Space     | Mở danh sách gợi ý điền nhanh                             |
| Ctrl + K Z       | Mở zen mode                                               |
| Ctrl + \         | Chia màn hình thành các editor (hay còn gọi là tab group) |
| Ctrl + 1, 2, 3   | Di chuyển giữa các editor                                 |
| F6               | Đổi panel                                                 |
| Ctrl + B         | Mở sidebar trái (VS Code gọi là primary sidebar)          |
| Ctrl + Shift + B | Mở sidebar phải (VS Code gọi là secondary sidebar)        |

Xem thêm:: [Hiểu về YAML](../../../%F0%9F%93%9C%20L%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Hi%E1%BB%83u%20v%E1%BB%81%20YAML.md#)
Xem thêm:: [Phím tắt trong VS Code](../../../%F0%9F%93%9C%20L%E1%BA%ADp%20tr%C3%ACnh/IDE%20(VS%20Code)/Ph%C3%ADm%20t%E1%BA%AFt%20trong%20VS%20Code.md#)
Xem thêm:: [Giao diện VS Code](../../../%F0%9F%93%9C%20L%E1%BA%ADp%20tr%C3%ACnh/IDE%20(VS%20Code)/Giao%20di%E1%BB%87n%20VS%20Code.md#)

