---
share: true
created: 2023-10-30T14:29
updated: 2025-10-13T09:05
---
Có vẻ như toàn bộ script sẽ được bọc trong một hàm. `return` của hàm này sẽ cho thông báo
Nguồn:: [What is the JS version? - API & Programming - Fibery Community](https://community.fibery.io/t/what-is-the-js-version/4837/9?u=ooker)
[Node với Deno là những môi trường thực thi của JavaScript](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20(runtime)/Node%20v%E1%BB%9Bi%20Deno%20l%C3%A0%20nh%E1%BB%AFng%20m%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20c%E1%BB%A7a%20JavaScript.md)

Ngày xưa thì dùng Node 12. Mà Node 12 thì không có Temporal, nên nếu muốn dùng thì phải bundle với polyfill của Temporal. Nhưng nếu làm vậy thì script lại quá lớn, Fibery không chịu. Nên mới chấp nhận dùng dạng ISO.