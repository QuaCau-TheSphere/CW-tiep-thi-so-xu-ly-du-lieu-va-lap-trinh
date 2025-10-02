---
share: true
created: 2023-10-24T18:26
updated: 2025-03-03T18:48
---
- pwd: process working directory
- cwd: current working directory

`process.env.PWD` trong Node **không** tồn tại trên Windows
Nguồn:: [Stack Overflow](../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [process.env.PWD vs process.cwd()](https://stackoverflow.com/a/31436403/3416774)

[Đường dẫn đến tệp ngoài trong một script phụ thuộc vào cwd, không phải đường dẫn tới script mình đang viết](./%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20%C4%91%E1%BA%BFn%20t%E1%BB%87p%20ngo%C3%A0i%20trong%20m%E1%BB%99t%20script%20ph%E1%BB%A5%20thu%E1%BB%99c%20v%C3%A0o%20cwd,%20kh%C3%B4ng%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20t%E1%BB%9Bi%20script%20m%C3%ACnh%20%C4%91ang%20vi%E1%BA%BFt.md)