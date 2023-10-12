---
share: true
created: 2023-08-25T14:20
updated: 2023-09-27T16:17
---
Ví dụ, khi khai báo [[../../../../../👏Trấn Kỳ/Trấn Kỳ — Phân loại thu chi bằng tiếng Việt tự nhiên|Trấn Kỳ]] như sau:
```yaml
Khai báo:
  - Tên chiều: Món đồ    
    Dữ liệu tự nhận dạng:
      - Thức ăn:
          - bún bò
          - bún riêu
  - Tên chiều: Phương thức thanh toán
    Dữ liệu tự nhận dạng:
      - Tiền mặt
          - nợn trả
          - mèo trả
```
Thì là bạn đang khai báo một vật thể bình thường. Vật thể này chứa dữ liệu. Để chương trình lấy được dữ liệu cần có, nó áp các phương thức lên vật thể này.

Trong khi đó, khi chạy chương trình với câu nhập `bún bò cho con 50k nợn trả chợ` và ra được kết quả sau:
```yaml
Món đồ: 'bún bò'
Loại món đồ: 'Thức ăn'
Phương thức thanh toán: 'nợn trả'
Loại phương thức thanh toán: 'Tiền mặt'
Nơi mua: 'chợ'
Loại nơi mua: Offline
Người thụ hưởng: 'con'
Loại người thụ hưởng: 'Gia đình'
Số tiền: '50000'
Ghi chú: ''
```

Thì mặc dù đây cũng là một vật thể, nhưng sự phức tạp của nó không còn giống như vật thể ở trên. Nó chỉ được dùng để tra dữ liệu, giống như bạn tra từ điển. Bạn không có ý định thay đổi giá trị trong nó. Nên loại vật thể này được gọi là từ điển.

[[../../../Lịch sử phát triển và triết lý ngôn ngữ/Python tách bạch từ điển và vật thể, còn JS không làm vậy|Python tách bạch từ điển và vật thể, còn JS không làm vậy]]

