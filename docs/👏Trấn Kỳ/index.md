---
share: true
created: 2023-09-05T16:17
updated: 2023-10-13T22:26
title: Trấn Kỳ — Phân loại thu chi bằng tiếng Việt tự nhiên
alias: Trấn Kỳ
description: Phân loại câu nhập bằng tiếng Việt tự nhiên
filename: index
---
Thu chi chồng chất nhưng không biết phải tính thế nào? Dùng app thì giới hạn chức năng hoặc tính phí, không app thì không biết tính sao?

Nay đã có Trấn Kỳ. Chương trình này xuất phát từ nhu cầu của một cá nhân đau đầu khi quản lý mạng lưới kinh doanh của mình, hiện tại đã hoàn thiện và trở thành công cụ đắc lực để phân loại thu chi cá nhân.

Hiện tại có rất nhiều ứng dụng quản lý thu chi, mình tin mỗi người sẽ tìm được những tính năng phù hợp với nhu cầu của bản thân. Vậy câu hỏi đặt ra là: "Bạn cần gì?" 

Nếu bạn là người cần phân loại tất cả các chi tiêu của mình một cách rõ ràng (việc nhắm hờ mỗi tháng chi chừng bao nhiêu tiền là không đủ với bạn), và bạn cần một chương trình:
- [x] Dùng được trên điện thoại khi không có mạng
- [x] Cho phép bạn khai báo dữ liệu theo thói quen và cách phân loại của chính mình
- [x] Tự động phân loại, gắn nhãn thông tin chứ không bắt bạn phải tự xử lý
- [x] Tích hợp được vào hệ thống vận hành hiện tại của bạn: Obsidian, Notion, Fibery, Google Sheet, v.v. 
- [x] Không có bất cứ quảng cáo mời mọc hoặc theo dõi dữ liệu nào

Thì chương trình này dành cho bạn.
![[../assets/attachments/Hemi Head_med.png|Hemi Head_med.png]]
# Tính năng
## Phân loại thông tin
Ví dụ, với câu nhập đầu vào là:
```
thăn bò 30k lườn gà 20k (giảm giá) cho Parid ở coopmart vợ trả 
```

Kết quả đầu ra sẽ là:

| Tên                         | Giá trị          |
| --------------------------- | ---------------- |
| Món đồ                      | thăn bò, lườn gà |
| Loại món đồ                 | Lương thực       |
| Phương thức thanh toán      | vợ trả           |
| Loại phương thức thanh toán | Tiền mặt         |
| Nơi mua                     | CoopMart         |
| Loại nơi mua                | Siêu thị         |
| Người thụ hưởng             | Parid            |
| Loại người thụ hưởng        | Gia đình         |
| Số tiền                     | 50000            |
| Ghi chú                     | giảm giá         |

Chương trình có thể tự động bắt được các giá trị trên nhờ vào [[2.1 Thiết lập cấu hình|cấu hình bạn đã thiết lập]] từ trước. Ở ví dụ này, bạn đã thiết lập:
- `thăn bò`, `lườn gà` thuộc nhãn `Lương thực` trong chiều `Món đồ`
- `vợ trả` thuộc nhãn `Tiền mặt` trong chiều `Phương thức thanh toán`

Chi tiết cụ thể như sau:

| Từ khoá từ câu nhập  | Nhãn phân loại  | Chiều dữ liệu            |
| -------------------- | --------------- | ------------------------ |
| `thăn bò`, `lườn gà` | `Lương thực`    | `Món đồ`                 |
| `vợ trả`             | `Tiền mặt`      | `Phương thức thanh toán` |
| `coopmart`           | `Siêu thị`      | `Nơi mua`                |
| `Parid`              | `Gia đình`      | `Người thụ hưởng`        |
| `20k`, `30k`         | Không thiết lập | `Số tiền`                |
| `giảm giá`           | Không thiết lập | `Ghi chú`                |

## Giá trị mặc định
Sẽ có những lúc bạn muốn chương trình tự hiểu là nếu bạn không điền từ khoá gì trong chiều `Phương thức thanh toán` thì mặc định đó là `tiền mặt`.

## Tiếp nhận từ khoá chưa được khai báo một cách trực tiếp
Sẽ có những lúc bạn muốn một từ khoá nào đó chưa kịp khai báo trong cấu hình xuất ra ở kết quả. Bạn có thể thiết lập các ký tự để chương trình hiểu là dữ liệu đó nên được cho vào mục nào.

Ví dụ, bạn mới gặp `Iris` và muốn tặng `dưa hấu` cho bạn ấy. Bạn chưa kịp khai báo tên của `Iris` vào cấu hình. Bạn có thể thiết lập ký tự `@` dành cho chiều `Người thụ hưởng`. Khi đó, bạn có thể dùng câu nhập:
```
tặng dưa hấu cho @Iris 50k
```

Lúc này chương trình sẽ tự hiểu `Iris` là `Người thụ hưởng`.

Nếu sau đó không xuất hiện dấu `@` lần nữa thì từ khoá sẽ dừng khi gặp dấu cách đầu tiên. Nếu từ khoá chứa nhiều dấu cách thì bạn thêm một dấu `@` nữa ở ngay cuối. Ví dụ:
```
tặng dưa hấu cho @chị Iris@ 50k
```

Bạn có thể khai báo ký tự đứng trước khác với ký tự đứng sau. Thường gặp nhất là khi bạn cần có một ghi chú nào đó. Ví dụ:
```
tặng dưa hấu cho @chị Iris@ 50k (sau đó mới biết chị Iris dị ứng dưa hấu)
```

## Viết tắt 
Sẽ có những lúc bạn muốn viết tắt `as` là `ăn sáng`, `st` là `siêu thị` cho nhanh. Nhưng bạn còn có thể dùng nó cho những câu nhập dài, và có thể thiết lập một hệ thống viết tắt cho những khoảng chi cố định hằng ngày, hằng tuần, hằng tháng.

Ví dụ:
- `as` → `ăn sáng`
- `st` → `siêu thị`
- `xăng` → `xăng 50k`
- `trọ` → `tiền trọ 3tr chuyển khoản (vay qua nhóm Tình Thân)`

## Hiểu từ ghép
Ví dụ, nếu lúc thiết lập cấu hình bạn có khai báo ba từ khoá `bún`, `bò`, và `bún bò`, và trong câu nhập có chữ `bún bò` thì chương trình sẽ hiểu đây là một từ chứ không nhận diện nhầm là có hai từ `bún` và `bò`.

## Một từ khoá có thể thuộc về nhiều nhãn phân loại
Ví dụ, từ khoá `ăn trưa với` vừa có thể thuộc nhãn `Mối quan hệ`, vừa có thể thuộc nhãn `Thực phẩm`

## Xuất, nhập dữ liệu với các chương trình khác
![[../assets/attachments/Keep to FIbery.png|Keep to FIbery.png]]
Hiện tại đã có sẵn phần bổ trợ (add-on) để nhập dữ liệu từ Google Keep và xuất dữ liệu sang Fibery. Bạn có thể tự viết những phần bổ trợ khác cho phù hợp với bạn.

Google Keep là một phần mềm ghi chú rất phổ biến với mọi người. Nó:
- Có trên iOS, Android và web
- Mở rất nhanh và có thể mở trong tình trạng không có mạng
- Đồng bộ hoá giữa tất cả các thiết bị
- Hoàn toàn miễn phí
- Cho phép nhiều người cùng chỉnh sửa một ghi chú

Việc có thể nhập liệu từ Google Keep sẽ giúp cho bạn có thể nhập những khoảng chi tiêu chung, phù hợp cho gia đình, nhóm bạn, tổ chức.

# Các tính năng hỗ trợ khác (a.k.a. yêu cầu phi chức năng) 
- **Viết cho người Việt** nên:
	- xử lý được từ ghép và [[../📜 Lập trình/Regex, Unicode, tiếng Việt, emoji/Regex/Tiếng Việt có 2 cách đặt dấu|các cách đặt dấu khác nhau]]
	- tên biến, tên hàm hoàn toàn bằng tiếng Việt
- **Viết cho người cần sử dụng trên các webapp khác** như Fibery, Google Sheet nên:
	- chỉ sử dụng JavaScript thuần 
	- đảm bảo regex không chạy lâu
	- có sẵn build script để chuyển từ TypeScript sang JavaScript
- **Viết cho người không muốn bị ràng buộc vào một nền tảng nào** nên sẽ có mã nguồn mở
- **Viết cho người phải tự học lập trình** nên:
	- có rất nhiều ghi chú, hướng dẫn để bạn hiểu code, hiểu được cái cách một lập trình viên kiến trúc nên một chương trình thế nào 
	- cố gắng tuân thủ [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/)
	- script kiểm thử

![Giao diện khởi động](https://i.imgur.com/njIioJD.png)

# Không chỉ mỗi phân loại thu chi
Thật ra, chương trình này không hẳn nên được đặt tên là "Phân loại thu chi", vì bạn còn có thể dùng nó để phân loại nhiều thứ khác. Ví dụ:
- **Ý tưởng**: `Kĩ thuật viết văn %topic_Writing @tác_giả_a`
- **Mối quan hệ**: `Gặp @ông_A bàn về việc X, có đi ăn ở !nhà_hàng_Y 200k ck vcb`
- **Công việc**: `Công việc A cần giao cho @bạn_B liên hệ với @@đối_tác_C tại !quán_D với chi phí dự kiến 300k ck vcb và nhận output &&item_X`
- **Cảm xúc**: `xem phim:Inception thấy chấn động`

Bạn muốn đọc gì tiếp theo?

[Lý do viết Trấn Kỳ](https://obsidian.quảcầu.cc/%F0%9F%93%90%20D%E1%BB%B1%20%C3%A1n/3%20Th%C3%A0nh%20ph%E1%BA%A9m/Tr%E1%BA%A5n%20K%E1%BB%B3/L%C3%BD%20do%20vi%E1%BA%BFt%20Tr%E1%BA%A5n%20K%E1%BB%B3/?utm_source=CW+%C2%BB+X%E1%BB%AD+l%C3%BD+d%E1%BB%AF+li%E1%BB%87u+v%C3%A0+l%E1%BA%ADp+tr%C3%ACnh&utm_medium=Gi%E1%BB%9Bi+thi%E1%BB%87u+Tr%E1%BA%A5n+K%E1%BB%B3&utm_campaign=Giai+%C4%91o%E1%BA%A1n+1&utm_term=%C4%90%E1%BB%8Dc+b%C3%A0i+vi%E1%BA%BFt+tr%C3%AAn+web){ .md-button .md-button--primary } [[./Hướng dẫn sử dụng Trấn Kỳ/index|Hướng dẫn sử dụng Trấn Kỳ]]{ .md-button .md-button--primary }
