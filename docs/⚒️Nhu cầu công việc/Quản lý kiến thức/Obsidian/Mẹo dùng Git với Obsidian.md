---
share: true
created: 2023-10-30T14:29
updated: 2025-10-12T13:17
---
## Thêm nội dung vào hàng loạt tập tin
```PowerShell
Get-ChildItem .gitignore -recurse | ForEach-Object { 
    Add-Content $_ .obsidian/plugins/obsidian-mkdocs-publisher/logs.txt
}
```

[Các lệnh Git thường dùng](../../../%F0%9F%97%84%EF%B8%8FT%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%93ng%20b%E1%BB%99,%20sao%20l%C6%B0u/Git/C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)
Nguồn:: 