---
share: true
created: 2023-10-24T18:26
updated: 2024-01-09T16:12
---
Một cách đại khái, [interface](https://tuhocict.com/lesson/cai-tien-data-acceess-su-dung-interface/) là một giao kèo giữa bên sử dụng và bên thực thi class. Cụ thể hơn, [interface](https://tuhocict.com/giai-phap-winforms-3-interface-loose-coupling/) chứa các mô tả về phương thức và thuộc tính mà bên thực thi class phải xây dựng. Bên sử dụng thì không cần quan tâm đến cách thức xây dựng này.

Lấy một ví dụ khác. Giả sử đèn điện nhà bạn lắp toàn loại đui xoáy. Nếu bạn cần mua bóng đèn, có vô số loại khác nhau, từ đèn sợi đốt đến đèn huỳnh quang, từ hình vuông đến hình tròn. Nhưng chỉ cần nó là đui xoáy thì bạn đều có thể sử dụng được.

Khi so ra, đui xoáy ở đây chính là một dạng interface, là “giao kèo” giữa người sử dụng bóng đèn và người sản xuất bóng đèn. Người sản xuất chỉ cần đảm bảo “đui xoáy” cho bóng mình làm ra. Người sử dụng thì không cần quan tâm đến cách thức làm ra bóng đèn, miễn sao có đui xoáy là được.

Interface khi đó được bên sử dụng xem như một kiểu dữ liệu. Biến của kiểu dữ liệu này có thể tương thích với bất kỳ object nào tạo ra từ class thực thi giao diện tương ứng.

Nguồn:: [tuhocict](../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/tuhocict.md), [Bộ nguyên lý SOLID - lập trình viên tương lai cần biết | Tự học ICT](https://tuhocict.com/bo-nguyen-ly-solid-lap-trinh-vien-tuong-lai-can-biet/)

[Giao diện là cái khuôn của phương thức](../H%C3%A0m/Giao%20di%E1%BB%87n%20l%C3%A0%20c%C3%A1i%20khu%C3%B4n%20c%E1%BB%A7a%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c.md)
[API là giao diện của một chương trình](./API%20l%C3%A0%20giao%20di%E1%BB%87n%20c%E1%BB%A7a%20m%E1%BB%99t%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh.md) 
[Việc đóng gói (encapsulation) giúp ta không cần quan tâm vật thể lưu dữ liệu thế nào, mà chỉ cần quan tâm tới thuộc tính và phương thức của nó](../V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/Vi%E1%BB%87c%20%C4%91%C3%B3ng%20g%C3%B3i%20(encapsulation)%20gi%C3%BAp%20ta%20kh%C3%B4ng%20c%E1%BA%A7n%20quan%20t%C3%A2m%20v%E1%BA%ADt%20th%E1%BB%83%20l%C6%B0u%20d%E1%BB%AF%20li%E1%BB%87u%20th%E1%BA%BF%20n%C3%A0o,%20m%C3%A0%20ch%E1%BB%89%20c%E1%BA%A7n%20quan%20t%C3%A2m%20t%E1%BB%9Bi%20thu%E1%BB%99c%20t%C3%ADnh%20v%C3%A0%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20c%E1%BB%A7a%20n%C3%B3.md)