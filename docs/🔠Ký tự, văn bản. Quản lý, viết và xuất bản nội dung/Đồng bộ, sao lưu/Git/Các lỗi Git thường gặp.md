---
share: true
created: 2024-09-19T17:01
updated: 2024-09-20T13:55
---
## Quên add
## Không thấy folder mình tạo được add
Lý do:: [Git không biết gì về folder](./Commit/Git%20kh%C3%B4ng%20bi%E1%BA%BFt%20g%C3%AC%20v%E1%BB%81%20folder.md)
## Thêm file vào  .gitignore rồi mà vẫn không thấy file bị ignore
## Lỡ commit file nặng
```
git filter-branch --force --index-filter 'git rm -r --cached --ignore-unmatch bigfile.txt' --prune-empty --tag-name-filter cat -- --all
```
## Lỡ commit secret

Xem thêm:: [Các lệnh Git thường dùng](./C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)