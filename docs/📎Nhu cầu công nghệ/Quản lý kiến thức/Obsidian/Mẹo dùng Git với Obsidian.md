---
share: true
created: 2023-10-30T14:29
updated: 2026-08-06T15:36
---
## Thêm nội dung vào hàng loạt tập tin
```PowerShell
Get-ChildItem .gitignore -recurse | ForEach-Object { 
    Add-Content $_ .obsidian/plugins/obsidian-mkdocs-publisher/logs.txt
}
```

[Các lệnh Git thường dùng](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/C%C3%B4ng%20c%E1%BB%A5/Git/C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)
Nguồn:: 
