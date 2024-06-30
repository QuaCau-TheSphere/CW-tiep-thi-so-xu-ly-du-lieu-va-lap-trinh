---
share: true
created: 2023-10-21T20:49
updated: 2023-11-28T23:49
---
Là một đoạn mã dùng để xác thực quyền truy cập, cho phép ứng dụng bên thứ 3 có thể truy cập vào những dữ liệu của người dùng trong một phạm vi nhất định mà nó cho phép. Token này được gửi bởi **Client** như một tham số được truyền vào _hreader_ trong mỗi request khi cần truy cập đến tài nguyên trong **Resource server**.

Nếu để lộ mất _access token_ thì cũng có thể coi như bị lộ _password_ bởi có thể lợi dụng nó để lấy được những tài nguyên mà nó đang bảo vệ. Vì vậy, _access token_ có một thời gian sử dụng nhất định (2 giờ, 2 tháng...) tùy thuộc vào nhu cầu sử dụng cũng như yêu cầu về tính bảo mật. _Access token_ chỉ được sử dụng một lần duy nhất, khi nó hết hiệu lực **Client** sẽ phải gửi lại yêu cầu đến **Authorization server** để lấy một mã _access token_ mới.

Nguồn:: [Viblo](../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Viblo.md), [Tìm hiểu đôi chút về OAuth2](https://viblo.asia/p/tim-hieu-doi-chut-ve-oauth2-eW65GvMLlDO)

[Authorization sinh ra access token để client sử dụng](./Authorization%20sinh%20ra%20access%20token%20%C4%91%E1%BB%83%20client%20s%E1%BB%AD%20d%E1%BB%A5ng.md) 
[Khi access token hết hạn truy cập, client gửi refresh token đến authorization server để được cấp access token mới](./Khi%20access%20token%20h%E1%BA%BFt%20h%E1%BA%A1n%20truy%20c%E1%BA%ADp,%20client%20g%E1%BB%ADi%20refresh%20token%20%C4%91%E1%BA%BFn%20authorization%20server%20%C4%91%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20c%E1%BA%A5p%20access%20token%20m%E1%BB%9Bi.md) 
