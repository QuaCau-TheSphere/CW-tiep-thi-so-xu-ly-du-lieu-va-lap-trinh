---
share: true
created: 2023-10-26T14:59
updated: 2024-08-14T21:32
alias: Các ký hiệu đặc biệt trong các ngôn ngữ khác nhau
cssClass: wide-table
---
| Ký tự               | JavaScript        | Python          | Git                               | PowerShell                                                | AutoHotKey   | CSS                           | CMD     | SQL | Bash | LaTeX |
| ------------------- | ----------------- | --------------- | --------------------------------- | --------------------------------------------------------- | ------------ | ----------------------------- | ------- | --- | ---- | ----- |
| Dấu nháy kép `"`    | Verbatim string   | Verbatim string |                                   | Chuỗi có thể chèn chuỗi khác vào được (expandable string) |              |                               |         |     |      |       |
| Dấu nháy đơn `'`    | Verbatim string   | Verbatim string |                                   | Chuỗi có sao ghi vậy (verbatim string)                    |              |                               |         |     |      |       |
| Dấu backtick ` `` ` | Expandable string |                 |                                   | Thoát khỏi ký tự đặc biệt, ngắt dòng                      |              |                               |         |     |      |       |
| Dấu đô la `$`       |                   |                 |                                   | `$biến`, `$env:path`                                      |              |                               |         |     |      |       |
| Dấu phần trăm `%`   |                   |                 |                                   | `ForEach-Object`                                          | `%biến%`     |                               | `%biến` |     |      |       |
| Dấu chéo `\`        |                   |                 |                                   |                                                           |              |                               |         |     |      |       |
| Dấu chéo ngược `/`  |                   |                 |                                   |                                                           |              |                               |         |     |      |       |
| Dấu sao `*`         |                   |                 |                                   |                                                           |              |                               |         |     |      |       |
| Dấu a còng `@`      |                   |                 | [HEAD](../../%F0%9F%93%8AT%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u.%20Ph%C3%A2n%20t%C3%ADch%20d%E1%BB%AF%20li%E1%BB%87u/T%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u/Git/Commit/HEAD%20l%C3%A0%20commit%20hi%E1%BB%87n%20t%E1%BA%A1i.md) | Chèn nhiều tham số vào cùng lúc (splatting)               |              | Scope                         |         |     |      |       |
| Dấu thăng `#`       |                   |                 |                                   | `# comment`. Mẹo: dùng `##` ở trên function               | `#directive` |                               |         |     |      |       |
| Dấu chấm phẩy `;`   |                   |                 |                                   |                                                           | `; comment`  |                               |         |     |      |       |
| Dấu gạch đứng `\|`  |                   |                 |                                   | Pipe                                                      |              |                               |         |     |      |       |
| Dấu chấm hỏi `?`    |                   |                 |                                   | `Where-Object`                                            |              |                               |         |     |      |       |
| Dấu lớn hơn `>`     |                   |                 |                                   |                                                           |              | Child combinator              |         |     |      |       |
| Dấu cộng `+`        |                   |                 |                                   |                                                           |              | Next-sibling combinator       |         |     |      |       |
| Dấu ngã `~`         |                   |                 |                                   |                                                           |              | Subsequent-sibling combinator |         |     |      |       |
| Ký tự               | JavaScript        | Python          |                                   | PowerShell                                                | AutoHotKey   | CSS                           | CMD     | SQL | Bash | LaTeX |



Ưu tiên dấu nháy đơn `'` hơn là nháy kép `"`. Tuy nhiên nhớ rằng [trong JSON thì chỉ có thể dùng nháy kép chứ không được dùng nháy đơn](./Ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/JSON/JSON%20kh%C3%B4ng%20cho%20ph%C3%A9p%20%C4%91%E1%BB%83%20d%C6%B0%20d%E1%BA%A5u%20ph%E1%BA%A9y,%20kh%C3%B4ng%20c%C3%B3%20comment,%20b%E1%BA%AFt%20bu%E1%BB%99c%20ph%E1%BA%A3i%20d%C3%B9ng%20ngo%E1%BA%B7c%20k%C3%A9p,%20key%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%C3%B3ng%20trong%20ngo%E1%BA%B7c%20k%C3%A9p.md).

[The Complete Guide to PowerShell Punctuation - Simple Talk](https://www.red-gate.com/simple-talk/sysadmin/powershell/the-complete-guide-to-powershell-punctuation/)

