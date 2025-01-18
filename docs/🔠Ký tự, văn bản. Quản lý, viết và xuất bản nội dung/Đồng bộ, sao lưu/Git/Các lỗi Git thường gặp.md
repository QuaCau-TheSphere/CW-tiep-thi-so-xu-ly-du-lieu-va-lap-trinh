---
share: true
created: 2024-09-19T17:01
updated: 2025-01-11T12:17
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
### B1. Xác định commit sớm nhất chứa secret
git 
Nếu là blob thì dùng 
```
git log --all --find-object=<BLOB-ID>
```

[Có thể hiểu blob là hash của một file, tree là hash của một folder, còn commit thực ra chỉ là hash của folder tổng](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/C%C3%B3%20th%E1%BB%83%20hi%E1%BB%83u%20blob%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20file,%20tree%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20folder,%20c%C3%B2n%20commit%20th%E1%BB%B1c%20ra%20ch%E1%BB%89%20l%C3%A0%20hash%20c%E1%BB%A7a%20folder%20t%E1%BB%95ng.md)
### B2. `git rebase -i <COMMIT-ID>~1`


Xem thêm:: [Các lệnh Git thường dùng](./C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)