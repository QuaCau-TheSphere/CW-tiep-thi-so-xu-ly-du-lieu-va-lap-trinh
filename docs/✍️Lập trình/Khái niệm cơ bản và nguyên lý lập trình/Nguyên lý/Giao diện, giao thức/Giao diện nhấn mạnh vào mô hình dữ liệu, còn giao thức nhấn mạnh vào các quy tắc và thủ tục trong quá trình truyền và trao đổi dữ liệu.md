---
share: true
created: 2023-10-30T14:29
updated: 2025-09-12T14:41
title: Giao diện và giao thức đều là những thứ các bên cần tuân thủ để sự giao tiếp được diễn ra, nhưng giao diện nhấn mạnh vào mô hình dữ liệu, còn giao thức nhấn mạnh vào các quy tắc và thủ tục trong quá trình truyền và trao đổi dữ liệu
---
[Giao diện là cách để sử dụng vật thể mà không cần biết bên trong nó có gì](../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/M%C3%B4%20%C4%91un/Giao%20di%E1%BB%87n%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20s%E1%BB%AD%20d%E1%BB%A5ng%20v%E1%BA%ADt%20th%E1%BB%83%20m%C3%A0%20kh%C3%B4ng%20c%E1%BA%A7n%20bi%E1%BA%BFt%20b%C3%AAn%20trong%20n%C3%B3%20c%C3%B3%20g%C3%AC.md). Đây là một ví dụ về giao diện (interface):

```
interface Communicate
{
    string SendMessageAndGetResponse(string message);
}
```

[Giao thức là cách để các bên nhận và gửi dữ liệu hiểu nhau](../../../../%F0%9F%9B%9CM%E1%BA%A1ng%20m%C3%A1y%20t%C3%ADnh/Giao%20th%E1%BB%A9c/Giao%20th%E1%BB%A9c%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20c%C3%A1c%20b%C3%AAn%20nh%E1%BA%ADn%20v%C3%A0%20g%E1%BB%ADi%20d%E1%BB%AF%20li%E1%BB%87u%20hi%E1%BB%83u%20nhau.md). Đây là một ví dụ về giao thức (protocol):

> 1. Gửi "Hello"
> 2. Nếu bạn nhận được phản hồi "Hi" thì hãy gửi "How are you?" và phản hồi sẽ là trạng thái
> 3. Nếu bạn nhận được bất kỳ thông tin nào khác ngoài "Hi" từ tin nhắn ban đầu thì hệ thống không hoạt động bình thường và bạn phải gửi tin nhắn "Reboot" 
> 4. Sau đó bạn sẽ nhận được "Rebooted!" nếu thành công và bất kỳ thông tin nào khác nếu không thành công

You can explore the relationship between these concepts in [Six Degree of Wikipedia](https://www.sixdegreesofwikipedia.com/?source=Interface+(computing)&target=Communication+protocol):
- Interface to protocol: [![enter image description here](https://i.sstatic.net/pzNMapLf.png)](https://i.sstatic.net/pzNMapLf.png)
- Protocol to interface: [![enter image description here](https://i.sstatic.net/65pL4rSB.png)](https://i.sstatic.net/65pL4rSB.png)

Nguồn:: [What is the difference between a protocol and an interface in general? - Stack Overflow](https://stackoverflow.com/a/64219055)
