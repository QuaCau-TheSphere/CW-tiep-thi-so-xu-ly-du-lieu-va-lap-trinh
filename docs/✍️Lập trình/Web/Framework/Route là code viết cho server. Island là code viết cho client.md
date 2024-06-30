---
share: true
created: 2023-10-30T14:29
updated: 2024-05-13T22:20
---
[Các hàm được môi trường thực thi cung cấp không hoạt động được ở island](./Island,%20state/C%C3%A1c%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20m%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20cung%20c%E1%BA%A5p%20kh%C3%B4ng%20ho%E1%BA%A1t%20%C4%91%E1%BB%99ng%20%C4%91%C6%B0%E1%BB%A3c%20%E1%BB%9F%20island.md)
If all your JavaScript only runs in the client, then you don't have the problem of how do I share signals from the server to the client, simply because there is no js code running on the server. Same is true if everything is running on the server. When all code only ever runs in the same runtime, you avoid the whole "how do I share stuff with the other runtime" which is a pretty complex problem.

Regarding why sharing signals doesn't work per import statement across runtimes: It's the same problem as when you open your website in Chrome, trigger some signal update and then open the same site in Firefox. Despite you having updated the signal in Chrome, it won't be updated in Firefox, simply because they both run in their own runtime and have no clue update each other

Every other framework which renders parts on the server and parts of it on the client has this problem. Doesn't matter if they are built around the island concept or something else
Nguồn:: [Discord](https://discord.com/channels/684898665143206084/991511118524715139/1238477389663834152)

[Route không bao giờ được gửi đến client. Island được chạy ở cả server và client](./Route,%20handler/Route%20kh%C3%B4ng%20bao%20gi%E1%BB%9D%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%ADi%20%C4%91%E1%BA%BFn%20client.%20Island%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BA%A1y%20%E1%BB%9F%20c%E1%BA%A3%20server%20v%C3%A0%20client.md)
[Render phía máy chủ nhanh và SEO tốt. Render phía người dùng phù hợp cho những ứng dụng cần tương tác nhiều](../Render%20ph%C3%ADa%20m%C3%A1y%20ch%E1%BB%A7%20nhanh%20v%C3%A0%20SEO%20t%E1%BB%91t.%20Render%20ph%C3%ADa%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng%20ph%C3%B9%20h%E1%BB%A3p%20cho%20nh%E1%BB%AFng%20%E1%BB%A9ng%20d%E1%BB%A5ng%20c%E1%BA%A7n%20t%C6%B0%C6%A1ng%20t%C3%A1c%20nhi%E1%BB%81u.md)
