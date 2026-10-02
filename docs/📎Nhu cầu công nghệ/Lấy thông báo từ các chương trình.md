---
share: true
created: 2023-10-30T14:29
updated: 2026-10-02T20:20
---
## Yêu cầu chức năng
Phải có:
- Dùng được với những nền tảng không cấp API

Có thì tốt:
- Phân loại độ khẩn cấp, quan trọng
- Có log 
- Nhắc hẹn
- Trả lời tự động những thứ bot có thể trả lời được
- Bấm vào là mở ra được nơi chat 
- Có bản web 

## Phân tích
Dù nền tảng không cho API thì vẫn phải đưa nội dung tin nhắn qua 2 kênh sau:
- Trong giao diện tin nhắn 
- Lên trung tâm thông báo của trình duyệt, hệ điều hành

Ta có thể lấy dữ liệu gián tiếp tại những kênh đó.

## Giải pháp
### Cách 1: chuyển tiếp thông báo nhận được sang một nơi khác
Nhược điểm là chỉ dùng được cho Android.

Các bước cài đặt:
1. Cài [Tasker](../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi/Android/Tasker.md) trên điện thoại Android. Cấp hết các quyền cần thiết
2. Triển khai [chương trình này](https://github.com/QuaCau-TheSphere/sound/) lên một máy phục vụ (server). Do nó được viết bằng Deno nên dùng Deno Deploy thì hợp nhất. Xem [demo](https://anxin.quacau.deno.net/)
3. Import [profile Tasker này](https://taskernet.com/shares/?user=AS35m8lzsj4d9AypQpFbngaGm31G9aDGS2iHxuemGuaJEbTFdhTS9XhDmhTOWhnwKalKBPQ5&id=Profile%3AWebhook+Momo), rồi thiết lập theo video sau:
  ![Chỉnh URL để lấy thông báo các chương trình.mp4](../attachments/Ch%E1%BB%89nh%20URL%20%C4%91%E1%BB%83%20l%E1%BA%A5y%20th%C3%B4ng%20b%C3%A1o%20c%C3%A1c%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh.mp4)

<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=sG37APnlmGI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Cách 2: tạo một trình duyệt riêng chỉ để quản lý các nền tảng chat
Nhược điểm là chỉ dùng được cho nền tảng nào có phiên bản dành cho web