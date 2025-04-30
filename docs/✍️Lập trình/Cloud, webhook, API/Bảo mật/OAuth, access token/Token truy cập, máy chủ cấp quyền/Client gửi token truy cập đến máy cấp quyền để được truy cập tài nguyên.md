---
share: true
created: 2023-10-21T20:49
updated: 2025-03-03T18:48
---
Là một đoạn mã dùng để xác thực quyền truy cập, cho phép ứng dụng bên thứ 3 có thể truy cập vào những dữ liệu của người dùng trong một phạm vi nhất định mà nó cho phép. Token này được gửi bởi **Client** như một tham số được truyền vào _hreader_ trong mỗi request khi cần truy cập đến tài nguyên trong **Resource server**.

Nếu để lộ mất _access token_ thì cũng có thể coi như bị lộ _password_ bởi có thể lợi dụng nó để lấy được những tài nguyên mà nó đang bảo vệ. Vì vậy, _access token_ có một thời gian sử dụng nhất định (2 giờ, 2 tháng...) tùy thuộc vào nhu cầu sử dụng cũng như yêu cầu về tính bảo mật. _Access token_ chỉ được sử dụng một lần duy nhất, khi nó hết hiệu lực **Client** sẽ phải gửi lại yêu cầu đến **Authorization server** để lấy một mã _access token_ mới.

Nguồn:: [Viblo](../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Viblo.md), [Tìm hiểu đôi chút về OAuth2](https://viblo.asia/p/tim-hieu-doi-chut-ve-oauth2-eW65GvMLlDO)

[Client nào có thông tin xác thực thì sẽ được nhận token truy cập từ máy chủ cấp quyền](./Client%20n%C3%A0o%20c%C3%B3%20th%C3%B4ng%20tin%20x%C3%A1c%20th%E1%BB%B1c%20th%C3%AC%20s%E1%BA%BD%20%C4%91%C6%B0%E1%BB%A3c%20nh%E1%BA%ADn%20token%20truy%20c%E1%BA%ADp%20t%E1%BB%AB%20m%C3%A1y%20ch%E1%BB%A7%20c%E1%BA%A5p%20quy%E1%BB%81n.md) 
[Một token truy cập có thể truy cập được một vài API với những quyền nhất định trong một khoảng thời gian nhất định](./M%E1%BB%99t%20token%20truy%20c%E1%BA%ADp%20c%C3%B3%20th%E1%BB%83%20truy%20c%E1%BA%ADp%20%C4%91%C6%B0%E1%BB%A3c%20m%E1%BB%99t%20v%C3%A0i%20API%20v%E1%BB%9Bi%20nh%E1%BB%AFng%20quy%E1%BB%81n%20nh%E1%BA%A5t%20%C4%91%E1%BB%8Bnh%20trong%20m%E1%BB%99t%20kho%E1%BA%A3ng%20th%E1%BB%9Di%20gian%20nh%E1%BA%A5t%20%C4%91%E1%BB%8Bnh.md)
[Khi token truy cập hết hạn, client gửi refresh token đến máy chủ cấp quyền để được cấp token truy cập mới](./Khi%20token%20truy%20c%E1%BA%ADp%20h%E1%BA%BFt%20h%E1%BA%A1n,%20client%20g%E1%BB%ADi%20refresh%20token%20%C4%91%E1%BA%BFn%20m%C3%A1y%20ch%E1%BB%A7%20c%E1%BA%A5p%20quy%E1%BB%81n%20%C4%91%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20c%E1%BA%A5p%20token%20truy%20c%E1%BA%ADp%20m%E1%BB%9Bi.md) 
