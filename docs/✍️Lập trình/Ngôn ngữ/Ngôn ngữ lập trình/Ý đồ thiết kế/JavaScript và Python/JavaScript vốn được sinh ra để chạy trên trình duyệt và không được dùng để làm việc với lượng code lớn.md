---
share: true
created: 2023-10-24T18:26
updated: 2024-12-18T21:33
---
Eric Lippert, một trong những implementers của JScript và ở trong hội đồng ECMA vào cuối thập kỷ 90, chia sẻ về lịch sử của JS như sau:
> Hãy nhớ lại mục đích thiết kế cơ bản của JS vào những năm 1990. **Làm cho con khỉ nhảy múa khi bạn rê chuột.** Chúng tôi coi inline expression script là bình thường, các khối script từ hai đến mười dòng là phổ biến, và cái ý nghĩ rằng sẽ có người viết *hàng trăm dòng* cho một trang thực sự rất bất thường. Tôi nhớ khi tôi lần đầu tiên xem một chương trình JS mười ngàn dòng, câu hỏi đầu tiên của tôi dành cho những người đang cần tôi giúp đỡ vì nó quá chậm so với phiên bản C++ của họ là một phiên bản của "bạn điên à?! 10 ngàn dòng code JS?! "

Nguồn:: [Why is Math.random() not designed to be cryptographically secure?](https://security.stackexchange.com/a/181623/94500)

[JavaScript cố gắng đoán ý định của người viết chứ không báo lỗi](./JavaScript%20c%E1%BB%91%20g%E1%BA%AFng%20%C4%91o%C3%A1n%20%C3%BD%20%C4%91%E1%BB%8Bnh%20c%E1%BB%A7a%20ng%C6%B0%E1%BB%9Di%20vi%E1%BA%BFt%20ch%E1%BB%A9%20kh%C3%B4ng%20b%C3%A1o%20l%E1%BB%97i.md)
Trong khi đó, [Python tập trung vào việc cung cấp một ngôn ngữ lập trình tổng quát, dễ đọc và dễ viết](./Python%20t%E1%BA%ADp%20trung%20v%C3%A0o%20vi%E1%BB%87c%20cung%20c%E1%BA%A5p%20m%E1%BB%99t%20ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh%20t%E1%BB%95ng%20qu%C3%A1t,%20d%E1%BB%85%20%C4%91%E1%BB%8Dc%20v%C3%A0%20d%E1%BB%85%20vi%E1%BA%BFt.md) 

Chính vì lý do này, nên khi rốt cuộc JS được dùng nhiều, người ta cần tạo thêm nhiều công cụ cho nó:
- [TypeScript cung cấp kiểu cho JavaScript](../../Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/TypeScript/TypeScript%20cung%20c%E1%BA%A5p%20ki%E1%BB%83u%20cho%20JavaScript.md) 
- [Node với Deno là những môi trường thực thi của JavaScript](../../Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20(runtime)/Node%20v%E1%BB%9Bi%20Deno%20l%C3%A0%20nh%E1%BB%AFng%20m%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20c%E1%BB%A7a%20JavaScript.md). Điều này dẫn tới việc [Những hàm của môi trường thực thi không chạy được trên trình duyệt](../../Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20(runtime)/Nh%E1%BB%AFng%20h%C3%A0m%20c%E1%BB%A7a%20m%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20kh%C3%B4ng%20ch%E1%BA%A1y%20%C4%91%C6%B0%E1%BB%A3c%20tr%C3%AAn%20tr%C3%ACnh%20duy%E1%BB%87t.md)

Xem thêm:: [Lịch sử phát triển của JavaScript](../../Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/L%E1%BB%8Bch%20s%E1%BB%AD%20ph%C3%A1t%20tri%E1%BB%83n%20c%E1%BB%A7a%20JavaScript.md)