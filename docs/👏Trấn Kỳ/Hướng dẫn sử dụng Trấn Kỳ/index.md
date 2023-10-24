---
share: true
created: 2023-08-25T14:20
updated: 2023-10-24T16:03
title: Hướng dẫn sử dụng Trấn Kỳ
filename: index
---
# 1. Cài đặt và sử dụng nhanh
[1.1 Cài đặt PowerShell, Deno, Python, Git, VS Code](./1.%20C%C3%A0i%20%C4%91%E1%BA%B7t%20v%C3%A0%20s%E1%BB%AD%20d%E1%BB%A5ng%20nhanh/1.1%20C%C3%A0i%20%C4%91%E1%BA%B7t%20PowerShell,%20Deno,%20Python,%20Git,%20VS%20Code.md#)
[1.2 Lấy code](./1.%20C%C3%A0i%20%C4%91%E1%BA%B7t%20v%C3%A0%20s%E1%BB%AD%20d%E1%BB%A5ng%20nhanh/1.2%20L%E1%BA%A5y%20code.md#)

# 2. Thiết lập chương trình
[2. Thiết lập chương trình](./2.%20Thi%E1%BA%BFt%20l%E1%BA%ADp%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh/index.md#)
[Hiểu về YAML](../../%F0%9F%93%9C%20L%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Hi%E1%BB%83u%20v%E1%BB%81%20YAML.md#)
[Sử dụng main.ts](./2.%20Thi%E1%BA%BFt%20l%E1%BA%ADp%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh/S%E1%BB%AD%20d%E1%BB%A5ng%20main.ts.md#)
[Sử dụng tranky.py](./2.%20Thi%E1%BA%BFt%20l%E1%BA%ADp%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh/S%E1%BB%AD%20d%E1%BB%A5ng%20tranky.py.md#)
[Thiết lập trên Fibery](./2.%20Thi%E1%BA%BFt%20l%E1%BA%ADp%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh/Thi%E1%BA%BFt%20l%E1%BA%ADp%20tr%C3%AAn%20Fibery.md#)
[Sử dụng Docker](./2.%20Thi%E1%BA%BFt%20l%E1%BA%ADp%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh/S%E1%BB%AD%20d%E1%BB%A5ng%20Docker.md#)
[Chạy chương trình định kỳ](./2.%20Thi%E1%BA%BFt%20l%E1%BA%ADp%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh/Ch%E1%BA%A1y%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh%20%C4%91%E1%BB%8Bnh%20k%E1%BB%B3.md#)
# 3. Hiểu code nói gì
Phần này sẽ cố gắng cung cấp các khái niệm thiết yếu trong việc giúp bạn xây dựng mental model cho code, để bạn hiểu được cái cách một lập trình viên kiến trúc nên một chương trình thế nào. Những thứ sẽ hay được sử dụng:
- Các phép so sánh, ẩn dụ, 
- Các sắp đặt để tạo sự tương phản (juxtaposition) giữa các định nghĩa, ý tưởng 
- Ý đồ thiết kế (design choice) chương trình 

[3.1 Mô hình xử lý dữ liệu](./3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/3.1%20M%C3%B4%20h%C3%ACnh%20x%E1%BB%AD%20l%C3%BD%20d%E1%BB%AF%20li%E1%BB%87u.md#)
[Chiều, từ và nhãn](./3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/Chi%E1%BB%81u,%20t%E1%BB%AB%20v%C3%A0%20nh%C3%A3n.md#)
[Hướng dẫn debug](./3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/H%C6%B0%E1%BB%9Bng%20d%E1%BA%ABn%20debug.md#)
[Ý nghĩa của biểu thức regex trong hàm lọcSốTiền()](./3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/%C3%9D%20ngh%C4%A9a%20c%E1%BB%A7a%20bi%E1%BB%83u%20th%E1%BB%A9c%20regex%20trong%20h%C3%A0m%20l%E1%BB%8DcS%E1%BB%91Ti%E1%BB%81n().md#)
[Ý nghĩa của biểu thức regex trong hàm lọcDữLiệuCầnTựĐộngNhậnDạng()](./3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/%C3%9D%20ngh%C4%A9a%20c%E1%BB%A7a%20bi%E1%BB%83u%20th%E1%BB%A9c%20regex%20trong%20h%C3%A0m%20l%E1%BB%8DcD%E1%BB%AFLi%E1%BB%87uC%E1%BA%A7nT%E1%BB%B1%C4%90%E1%BB%99ngNh%E1%BA%ADnD%E1%BA%A1ng().md#)

> [!NOTE] Hỗ trợ trực tiếp
> Nếu bạn cần sự hỗ trợ trực tiếp, bạn có thể tham gia [các buổi hướng dẫn sử dụng Trấn Kỳ](https://obsidian.quảcầu.cc/%F0%9F%93%90%20d%E1%BB%B1%20%C3%A1n/3%20th%C3%A0nh%20ph%E1%BA%A9m/c%C3%A1c%20bu%E1%BB%95i%20%C4%91%C3%A1p%20%E1%BB%A9ng%20nhu%20c%E1%BA%A7u%20h%E1%BB%8Dc%20c%C3%A1ch%20s%E1%BB%AD%20d%E1%BB%A5ng%20c%C3%B4ng%20c%E1%BB%A5%20v%C3%A0%20t%C6%B0%20duy%20l%E1%BA%ADp%20tr%C3%ACnh%20cho%20nhu%20c%E1%BA%A7u%20c%C3%A1%20nh%C3%A2n%20ho%E1%BA%B7c%20nghi%C3%AAn%20c%E1%BB%A9u/c%C3%A1c%20bu%E1%BB%95i%20h%C6%B0%E1%BB%9Bng%20d%E1%BA%ABn%20s%E1%BB%AD%20d%E1%BB%A5ng%20tr%E1%BA%A5n%20k%E1%BB%B3/?utm_source=CW+X%E1%BB%AD+l%C3%BD+d%E1%BB%AF+li%E1%BB%87u+v%C3%A0+l%E1%BA%ADp+tr%C3%ACnh+%C2%BB+H%C6%B0%E1%BB%9Bng+d%E1%BA%ABn+s%E1%BB%AD+d%E1%BB%A5ng+Tr%E1%BA%A5n+K%E1%BB%B3&utm_medium=Gi%E1%BB%9Bi+thi%E1%BB%87u&utm_campaign=Tr%E1%BA%A5n+K%E1%BB%B3). Chúng là một phần của [các buổi đáp ứng nhu cầu học cách sử dụng công cụ và hiểu tư duy lập trình cho nhu cầu cá nhân hoặc nghiên cứu](https://obsidian.quảcầu.cc/%F0%9F%93%90%20d%E1%BB%B1%20%C3%A1n/3%20th%C3%A0nh%20ph%E1%BA%A9m/c%C3%A1c%20bu%E1%BB%95i%20%C4%91%C3%A1p%20%E1%BB%A9ng%20nhu%20c%E1%BA%A7u%20h%E1%BB%8Dc%20c%C3%A1ch%20s%E1%BB%AD%20d%E1%BB%A5ng%20c%C3%B4ng%20c%E1%BB%A5%20v%C3%A0%20t%C6%B0%20duy%20l%E1%BA%ADp%20tr%C3%ACnh%20cho%20nhu%20c%E1%BA%A7u%20c%C3%A1%20nh%C3%A2n%20ho%E1%BA%B7c%20nghi%C3%AAn%20c%E1%BB%A9u/?utm_source=CW+X%E1%BB%AD+l%C3%BD+d%E1%BB%AF+li%E1%BB%87u+v%C3%A0+l%E1%BA%ADp+tr%C3%ACnh+%C2%BB+H%C6%B0%E1%BB%9Bng+d%E1%BA%ABn+s%E1%BB%AD+d%E1%BB%A5ng+Tr%E1%BA%A5n+K%E1%BB%B3&utm_medium=Gi%E1%BB%9Bi+thi%E1%BB%87u&utm_campaign=Tr%E1%BA%A5n+K%E1%BB%B3).
