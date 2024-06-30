---
share: true
created: 2023-08-25T14:20
updated: 2024-02-04T16:31
title: 2. Thiết lập chương trình
---
Để Trấn Kỳ có thể phân loại tự động được, bạn cần phải thiết lập cấu hình. Các cấu hình được khai báo nằm trong thư mục `A. Cấu hình`. Chúng ở định dạng YAML. Cấu trúc cơ bản của nó như sau:
```yaml
Khai báo:
  - Tên chiều: 
    Dữ liệu tự nhận dạng: 
	Giá trị mặc định: 
    Ký tự để nhập trực tiếp:
      Từ:
      Nhãn:
    Tên gọi đầu ra:
      Từ: 
      Nhãn:  
Viết tắt:
Fibery:
Keep
```
Ví dụ:
```yaml
Khai báo:
  - Tên chiều: Món đồ
    Dữ liệu tự nhận dạng: 
      - Lương thực: lương thực, ăn sáng, ăn trưa, ăn chiều, ăn tối, cơm sáng, cơm trưa, cơm tối, bánh mì, rau, đồ hộp, cơm bụi, nước, bình nước
      - Xe: xăng, nhớt xe, sửa xe, gửi xe, grab, thuê xe, xe đò, tài xế
  - Tên chiều: Phương thức thanh toán
    Dữ liệu tự nhận dạng: 
      - Tài khoản ngân hàng: agri, vcb
      - Ví điện tử: momo, zalopay
      - Tiền mặt: tiền mặt
    Giá trị mặc định: tiền mặt
  - Tên chiều: Người thụ hưởng
    Dữ liệu tự nhận dạng: 
      - Tài khoản ngân hàng: agri, vcb
      - Ví điện tử: momo, zalopay
      - Tiền mặt: tiền mặt
    Giá trị mặc định: tiền mặt
  - Tên chiều: Người thụ hưởng
    Dữ liệu tự nhận dạng:
      - Gia đình: bản thân, vợ, con
      - Nhà vợ: ba vợ, má vợ, chị dâu, em dâu
    Giá trị mặc định: Bản thân
    Ký tự để nhập trực tiếp:
      Từ: "@" 
      Nhãn: "@@"  
  - Tên chiều: Số tiền
  - Tên chiều: Ghi chú
    Ký tự để nhập trực tiếp:
      Từ: "(", ")"

Viết tắt: 
  - ăn sáng: as, ss
  - chuyển khoản: ck
  - cà phê: cafe, cf
```
> [!Attention] Lỗi sai thường gặp khi viết YAML
> - Dùng tab để thụt đầu dòng
> - Số dấu cách ở đầu mỗi dòng không chính xác
> - Không để các ký tự đặc biệt vào dấu ngoặc kép
Nếu bạn cần dùng các ký tự này: `{`, `}`, `[`, `]`, `&`, `*`, `#`, `?`, `|`, `-`, `<`, `>`, `＝`, `!`, `%`, `@`, `:`, `` ` ``, `,` thì cần để vào dấu ngoặc kép.
>  
> Để đảm bảo việc viết cú pháp đúng bạn có thể dùng [YAML Viewer](https://codebeautify.org/yaml-viewer-online)

## Các chiều đặc biệt
Nếu bạn khai báo một trong những chiều này thì cần lưu ý thêm:
### `Món đồ`
- Những món đồ cùng nhãn thì chỉ hiển thị một nhãn. Ví dụ: nếu câu nhập là `thịt 50k, cá 20k` thì nhãn sẽ là `Lương thực`, không phải `Lương thực, Lương thực`
- Nếu trong câu nhập có nhiều món đồ cùng nhãn thì chỉ lấy một nhãn

### `Phương thức thanh toán`
Nếu trong câu nhập có nhiều phương thức thanh toán thì chỉ lấy cái cuối cùng, còn tất cả những cái phía trước chỉ là thông tin. Ví dụ, nếu câu nhập là `đáo hạn shinhan` thì `shinhan` sẽ là `Phương thức thanh toán`. Nhưng nếu câu nhập là `đáo hạn shinhan bằng vcb` thì `vcb` sẽ là `Phương thức thanh toán`.

### `Số tiền`
- Số tiền sẽ là các số có đuôi là tr, k, đ, d. Nếu không có đơn vị thì sẽ không xem là số tiền
- Nếu có nhiều giá trị thì sẽ lấy tổng. Nếu muốn chọn một giá trị nào đó thì thêm dấu bằng phía trước nó (`＝`). Ví dụ:
	  - `cá 50k thịt 40k` → `90000`.
	  - `cá 50k thịt = 40k`→ `40000`

- Dấu thập phân là dấu chấm (`.`). Bạn có thể dùng dấu phẩy (`,`) để cách các con số để dễ đọc. Nó sẽ được bỏ đi. Ví dụ: 1.2tr, 3,400k, 123,456,700đ, 123,456,700d.


## Một số phím tắt thường dùng cho việc đọc hiểu code

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

Xem thêm:: [YAML được sinh ra để con người đọc và viết metadata một cách dễ dàng](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/YAML/YAML%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20%C4%91%E1%BB%83%20con%20ng%C6%B0%E1%BB%9Di%20%C4%91%E1%BB%8Dc%20v%C3%A0%20vi%E1%BA%BFt%20metadata%20m%E1%BB%99t%20c%C3%A1ch%20d%E1%BB%85%20d%C3%A0ng.md)
Xem thêm:: [Phím tắt trong VS Code](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/C%C3%B4ng%20c%E1%BB%A5/IDE%20(VS%20Code)/Ph%C3%ADm%20t%E1%BA%AFt%20trong%20VS%20Code.md)
Xem thêm:: [Giao diện VS Code](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/C%C3%B4ng%20c%E1%BB%A5/IDE%20(VS%20Code)/Giao%20di%E1%BB%87n%20VS%20Code.md)

