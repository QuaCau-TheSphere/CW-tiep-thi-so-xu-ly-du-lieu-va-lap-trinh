---
share: true
created: 2023-10-30T14:29
updated: 2025-10-09T11:04
---
Có 2 cách (hoặc tác giả chưa biết thêm cách thứ 3 vì kiến thức hạn hẹp) để **implement** một ngôn ngữ hỗ trợ hướng đối tượng (OO supported). Đó là **class-base** & **prototype-base**. **Class-base** là cách **implement** (cài đặt) ngôn ngữ lập trình hướng đối tượng chặt chẽ, thể hiện được khía cạnh mạnh mẽ của **O**bject **O**riented (hướng đối tượng), các ngôn ngữ bậc trung như **C++**, **Java**, **C#**,... được cài đặt theo cách này. Tuy nhiên điểm yếu là khi bắt đầu code với các ngôn ngữ này thì nền tảng về lập trình, cũng như hiểu biết về hướng đối tượng, kỹ thuật lập trình là thứ không thể thiếu. Cài đặt dài dòng rườm ra mất thời gian của coder nhưng thứ tốt hơn được nhận lấy là code dễ quản lý, tìm lỗi, bảo trì. Nôm na là sẽ đánh đổi công sức của coder lấy về một source code tốt (hoặc ít nhất thì đó là mục tiêu lý tưởng).

Cách ngược lại là **protoype-base** thì giúp coder viết code nhanh và mượt hơn, không strict nhiều tính chất chặt chẽ, dễ tiếp cận với người mới. Mặt khác thì nhận sự hạn chế trong việc tuỳ biến các đối tượng. Đồng thời phải sinh ra thêm khái niệm mới để đảm bảo tính chất của **OO** về mặt tư tưởng. **Javascript** & **Python** là 2 ngôn ngữ điển hình cài đặt OOP theo prototype

Trích từ:: [OOP Implementation](https://viblo.asia/p/oop-implementation-V3m5Wm7QZO7)
[JavaScript là lập trình dựa trên prototype, Java là lập trình dựa trên lớp](../%C3%9D%20%C4%91%E1%BB%93%20thi%E1%BA%BFt%20k%E1%BA%BF/JavaScript%20v%C3%A0%20Python/JavaScript%20l%C3%A0%20l%E1%BA%ADp%20tr%C3%ACnh%20d%E1%BB%B1a%20tr%C3%AAn%20prototype,%20Java%20l%C3%A0%20l%E1%BA%ADp%20tr%C3%ACnh%20d%E1%BB%B1a%20tr%C3%AAn%20l%E1%BB%9Bp.md)