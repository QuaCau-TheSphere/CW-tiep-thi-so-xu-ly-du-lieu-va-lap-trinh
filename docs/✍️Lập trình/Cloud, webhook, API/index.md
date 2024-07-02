---
share: true
created: 2023-11-30T22:51
updated: 2024-04-26T12:33
title: Cloud, webhook, API
---

- \-: 
    - [API đưa thông tin là thụ động. Webhook đưa thông tin chủ động](./API%20%C4%91%C6%B0a%20th%C3%B4ng%20tin%20l%C3%A0%20th%E1%BB%A5%20%C4%91%E1%BB%99ng.%20Webhook%20%C4%91%C6%B0a%20th%C3%B4ng%20tin%20ch%E1%BB%A7%20%C4%91%E1%BB%99ng.md)
    - [Cloud bản chất là đi thuê local của người khác](./Cloud%20b%E1%BA%A3n%20ch%E1%BA%A5t%20l%C3%A0%20%C4%91i%20thu%C3%AA%20local%20c%E1%BB%A7a%20ng%C6%B0%E1%BB%9Di%20kh%C3%A1c.md)
    - [Endpoint](./Endpoint.md)
    - [Node là một vật thể có ID riêng. Edge là vật thể liên kết giữa các node. Field là thuộc tính của vật thể](./Node%20l%C3%A0%20m%E1%BB%99t%20v%E1%BA%ADt%20th%E1%BB%83%20c%C3%B3%20ID%20ri%C3%AAng.%20Edge%20l%C3%A0%20v%E1%BA%ADt%20th%E1%BB%83%20li%C3%AAn%20k%E1%BA%BFt%20gi%E1%BB%AFa%20c%C3%A1c%20node.%20Field%20l%C3%A0%20thu%E1%BB%99c%20t%C3%ADnh%20c%E1%BB%A7a%20v%E1%BA%ADt%20th%E1%BB%83.md)
    - [Node với edge được gọi chung là endpoint](Node%20v%E1%BB%9Bi%20edge%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20chung%20l%C3%A0%20endpoint.md)
    - [Web service là những API dùng trên HTTP](./Web%20service%20l%C3%A0%20nh%E1%BB%AFng%20API%20d%C3%B9ng%20tr%C3%AAn%20HTTP.md)

- Facebook API: 
    - [Các API thường dùng cho PHP](./Facebook%20API/C%C3%A1c%20API%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng%20cho%20PHP.md)
    - [Facebook API](./Facebook%20API/index.md)
    - [Fb hạn chế rất nhiều API để tránh việc làm nhái page](./Facebook%20API/Fb%20h%E1%BA%A1n%20ch%E1%BA%BF%20r%E1%BA%A5t%20nhi%E1%BB%81u%20API%20%C4%91%E1%BB%83%20tr%C3%A1nh%20vi%E1%BB%87c%20l%C3%A0m%20nh%C3%A1i%20page.md)
    - [me-accounts liệt kê tất cả các page mình quản lý](./Facebook%20API/me-accounts%20li%E1%BB%87t%20k%C3%AA%20t%E1%BA%A5t%20c%E1%BA%A3%20c%C3%A1c%20page%20m%C3%ACnh%20qu%E1%BA%A3n%20l%C3%BD.md)

- Fibery: 
    - [Non-ASCII or non-English characters in field or database names will be transliterated to English](./Fibery/Non-ASCII%20or%20non-English%20characters%20in%20field%20or%20database%20names%20will%20be%20transliterated%20to%20English.md)

- Google API: 
    - [Build service object](./Google%20API/Build%20service%20object.md)

- OAuth, access token: 
    - [Auth không phải là xác thực](./OAuth,%20access%20token/Auth%20kh%C3%B4ng%20ph%E1%BA%A3i%20l%C3%A0%20x%C3%A1c%20th%E1%BB%B1c.md)
    - [Authorization sinh ra access token để client sử dụng](./OAuth,%20access%20token/Authorization%20sinh%20ra%20access%20token%20%C4%91%E1%BB%83%20client%20s%E1%BB%AD%20d%E1%BB%A5ng.md)
    - [Client gửi access token đến authorization server để được truy cập](./OAuth,%20access%20token/Client%20g%E1%BB%ADi%20access%20token%20%C4%91%E1%BA%BFn%20authorization%20server%20%C4%91%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20truy%20c%E1%BA%ADp.md)
    - [Client ID là để authorization server biết client nào là client nào, còn client secret là để nó đảm bảo rằng client này chính là client đó](./OAuth,%20access%20token/Client%20ID%20l%C3%A0%20%C4%91%E1%BB%83%20authorization%20server%20bi%E1%BA%BFt%20client%20n%C3%A0o%20l%C3%A0%20client%20n%C3%A0o,%20c%C3%B2n%20client%20secret%20l%C3%A0%20%C4%91%E1%BB%83%20n%C3%B3%20%C4%91%E1%BA%A3m%20b%E1%BA%A3o%20r%E1%BA%B1ng%20client%20n%C3%A0y%20ch%C3%ADnh%20l%C3%A0%20client%20%C4%91%C3%B3.md)
    - [Client là ứng dụng muốn truy cập vào dữ liệu của user](./OAuth,%20access%20token/Client%20l%C3%A0%20%E1%BB%A9ng%20d%E1%BB%A5ng%20mu%E1%BB%91n%20truy%20c%E1%BA%ADp%20v%C3%A0o%20d%E1%BB%AF%20li%E1%BB%87u%20c%E1%BB%A7a%20user.md)
    - [Khi access token hết hạn truy cập, client gửi refresh token đến authorization server để được cấp access token mới](./OAuth,%20access%20token/Khi%20access%20token%20h%E1%BA%BFt%20h%E1%BA%A1n%20truy%20c%E1%BA%ADp,%20client%20g%E1%BB%ADi%20refresh%20token%20%C4%91%E1%BA%BFn%20authorization%20server%20%C4%91%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20c%E1%BA%A5p%20access%20token%20m%E1%BB%9Bi.md)
    - [OAuth giúp vẫn biết user kể cả khi user đổi mật khẩu](./OAuth,%20access%20token/OAuth%20gi%C3%BAp%20v%E1%BA%ABn%20bi%E1%BA%BFt%20user%20k%E1%BB%83%20c%E1%BA%A3%20khi%20user%20%C4%91%E1%BB%95i%20m%E1%BA%ADt%20kh%E1%BA%A9u.md)
    - [OAuth là cách để cấp quyền truy cập dữ liệu mà người dùng không phải cấp mật khẩu](./OAuth,%20access%20token/OAuth%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20c%E1%BA%A5p%20quy%E1%BB%81n%20truy%20c%E1%BA%ADp%20d%E1%BB%AF%20li%E1%BB%87u%20m%C3%A0%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng%20kh%C3%B4ng%20ph%E1%BA%A3i%20c%E1%BA%A5p%20m%E1%BA%ADt%20kh%E1%BA%A9u.md)
    - [Redirect URI là nơi](./OAuth,%20access%20token/Redirect%20URI%20l%C3%A0%20n%C6%A1i.md)
    - [Scope là những phạm vi dữ liệu khi ứng dụng truy cập](./OAuth,%20access%20token/Scope%20l%C3%A0%20nh%E1%BB%AFng%20ph%E1%BA%A1m%20vi%20d%E1%BB%AF%20li%E1%BB%87u%20khi%20%E1%BB%A9ng%20d%E1%BB%A5ng%20truy%20c%E1%BA%ADp.md)
    - [❓OAuth là cấp phép cho ai, token là cấp phép được làm cái gì](./OAuth,%20access%20token/%E2%9D%93OAuth%20l%C3%A0%20c%E1%BA%A5p%20ph%C3%A9p%20cho%20ai,%20token%20l%C3%A0%20c%E1%BA%A5p%20ph%C3%A9p%20%C4%91%C6%B0%E1%BB%A3c%20l%C3%A0m%20c%C3%A1i%20g%C3%AC.md)


[Launchpad Online - YouTube](https://www.youtube.com/playlist?list=PLOU2XLYxmsILOIxBRPPhgYbuSslr50KVq)
![Difference between cookies, session and tokens - YouTube](https://www.youtube.com/watch?v=GhrvZ5nUWNg)