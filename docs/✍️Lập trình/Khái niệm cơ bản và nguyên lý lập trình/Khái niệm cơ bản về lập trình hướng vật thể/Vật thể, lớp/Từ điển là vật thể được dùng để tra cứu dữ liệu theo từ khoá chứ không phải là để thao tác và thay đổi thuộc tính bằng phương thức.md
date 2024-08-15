---
share: true
title: Nếu tất cả thuộc tính của vật thể đều đơn giản, và vật thể được dùng để tra cứu dữ liệu theo từ khoá chứ không phải là để thao tác và thay đổi thuộc tính bằng phương thức, thì nó được gọi là từ điển
created: 2023-08-25T14:20
updated: 2024-07-26T13:53
---
Ví dụ, khi khai báo [Trấn Kỳ](Tr%E1%BA%A5n%20K%E1%BB%B3%20%E2%80%94%20Ph%C3%A2n%20lo%E1%BA%A1i%20thu%20chi%20b%E1%BA%B1ng%20ti%E1%BA%BFng%20Vi%E1%BB%87t%20t%E1%BB%B1%20nhi%C3%AAn.md) như sau:
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

[Python tách bạch từ điển và vật thể ngay từ đầu, còn JS mãi về sau mới có từ điển](../../../Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/JavaScript%20v%C3%A0%20Python/Kh%C3%A1c%20bi%E1%BB%87t%20gi%E1%BB%AFa%20JS%20v%C3%A0%20Python/V%E1%BB%81%20m%E1%BA%B7t%20tri%E1%BA%BFt%20l%C3%BD/Python%20t%C3%A1ch%20b%E1%BA%A1ch%20t%E1%BB%AB%20%C4%91i%E1%BB%83n%20v%C3%A0%20v%E1%BA%ADt%20th%E1%BB%83%20ngay%20t%E1%BB%AB%20%C4%91%E1%BA%A7u,%20c%C3%B2n%20JS%20m%C3%A3i%20v%E1%BB%81%20sau%20m%E1%BB%9Bi%20c%C3%B3%20t%E1%BB%AB%20%C4%91i%E1%BB%83n.md)

