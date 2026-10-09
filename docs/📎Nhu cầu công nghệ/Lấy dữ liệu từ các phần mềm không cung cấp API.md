---
share: true
created: 2023-10-30T14:29
updated: 2026-10-09T16:35
---
## Phân tích
Dù phần mềm không cho API thì vẫn phải đưa dữ liệu đến giao diện người dùng. Ngoài ra, một số loại phần mềm như phần mềm chat cũng cần đưa dữ liệu đến trung tâm thông báo của trình duyệt, hệ điều hành. Ta có thể lấy dữ liệu gián tiếp tại những kênh đó.

Lấy được trong giao diện người dùng thì là tốt nhất. Về bản chất thì cũng như cào web thôi, chỉ là thay vì cào web thì giờ là cào app. Nhưng khác biệt ở chỗ với web thì ta truy cập qua trình duyệt, còn với app thì hệ điều hành trực tiếp chạy. Nên tùy vào hệ điều hành mà có làm được hay không. Trên điện thoại chắc chỉ có Android mới làm được, mà cũng không chắc là làm tốt. Nếu nền tảng cung cấp phiên bản web thì chắc sẽ dễ hơn. Còn không thì thử giả lập xem có được không.

## Giải pháp đề xuất
### Cách 1: chuyển tiếp thông báo nhận được sang một nơi khác
Cách dưới đây chỉ dùng được cho Android.

Các bước cài đặt:
1. Cài [Tasker](../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi/Android/Tasker.md) trên điện thoại Android. Cấp hết các quyền cần thiết
2. Triển khai [chương trình này](https://github.com/QuaCau-TheSphere/sound/) lên một máy phục vụ (server). Do nó được viết bằng Deno nên dùng Deno Deploy thì hợp nhất. Xem [demo](https://anxin.quacau.deno.net/)
3. Import [profile Tasker này](https://taskernet.com/shares/?user=AS35m8lzsj4d9AypQpFbngaGm31G9aDGS2iHxuemGuaJEbTFdhTS9XhDmhTOWhnwKalKBPQ5&id=Profile%3AWebhook+Momo), rồi thiết lập theo video sau:
  ![Chỉnh URL để lấy thông báo các chương trình.mp4](../attachments/Ch%E1%BB%89nh%20URL%20%C4%91%E1%BB%83%20l%E1%BA%A5y%20th%C3%B4ng%20b%C3%A1o%20c%C3%A1c%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh.mp4)

<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=sG37APnlmGI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Cách 2: tạo một trình duyệt riêng chỉ để quản lý các nền tảng chat
Nhược điểm là chỉ dùng được cho nền tảng nào có phiên bản dành cho web

Nếu bạn muốn hoàn thiện chương trình này thì hãy cho biết những thứ bạn có thể đóng góp.