---
share: true
created: 2023-10-30T14:29
updated: 2025-11-11T11:56
---
[UTF là cách thức để chuyển đổi từ điểm mã sang hệ nhị phân](../../../%F0%9F%94%A0K%C3%BD%20t%E1%BB%B1,%20v%C4%83n%20b%E1%BA%A3n,%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/Ti%E1%BA%BFng%20Vi%E1%BB%87t,%20Unicode,%20emoji/L%C3%BD%20thuy%E1%BA%BFt%20Unicode/%C4%90i%E1%BB%83m%20m%C3%A3/UTF%20l%C3%A0%20c%C3%A1ch%20th%E1%BB%A9c%20%C4%91%E1%BB%83%20chuy%E1%BB%83n%20%C4%91%E1%BB%95i%20t%E1%BB%AB%20%C4%91i%E1%BB%83m%20m%C3%A3%20sang%20h%E1%BB%87%20nh%E1%BB%8B%20ph%C3%A2n.md)
when it comes to capturing the output in a variable or redirecting it, PowerShell decodes the output into .NET strings (first), using the character encoding stored in `[Console]::OutputEncoding`. Therefore, you may have to (temporarily) set it to the encoding used by the external program. E.g., for programs that output UTF-8, such as node: 
`[Console]::OutputEncoding = [System.Text.UTF8Encoding]::new()`

Nguồn:: [Character encoding problem when importing SQL with DBForge and PowerShell into MySQL - Stack Overflow](https://stackoverflow.com/a/78082903/3416774)
