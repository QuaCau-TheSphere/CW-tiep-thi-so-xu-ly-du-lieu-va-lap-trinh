---
share: true
created: 2023-05-26T14:51
updated: 2023-10-27T19:15
---
# Quên add

# [Git không biết gì về folder](Git%20kh%C3%B4ng%20bi%E1%BA%BFt%20g%C3%AC%20v%E1%BB%81%20folder.md#)

# Thêm file vào  .gitignore rồi mà vẫn không thấy file bị ignore

# Lỡ commit file nặng
```
git filter-branch --force --index-filter 'git rm -r --cached --ignore-unmatch bigfile.txt' --prune-empty --tag-name-filter cat -- --all
```

[Các lệnh git thường sử dụng](./C%C3%A1c%20l%E1%BB%87nh%20git%20th%C6%B0%E1%BB%9Dng%20s%E1%BB%AD%20d%E1%BB%A5ng.md#)