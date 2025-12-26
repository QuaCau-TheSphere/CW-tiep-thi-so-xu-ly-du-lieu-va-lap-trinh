---
share: true
created: 2023-10-26T14:59
updated: 2025-03-03T18:48
alias: Các ký hiệu đặc biệt trong các ngôn ngữ khác nhau
cssClass: wide-table
---
| Ký tự               | JavaScript                             | Python                                 | PowerShell                                                | Git                               | AutoHotKey   | CSS                           | CMD     | SQL | Bash | LaTeX |
| ------------------- | -------------------------------------- | -------------------------------------- | --------------------------------------------------------- | --------------------------------- | ------------ | ----------------------------- | ------- | --- | ---- | ----- |
| Dấu nháy kép `"`    | Chuỗi có sao ghi vậy (verbatim string) | Chuỗi có sao ghi vậy (verbatim string) | Chuỗi có thể chèn chuỗi khác vào được (expandable string) |                                   |              |                               |         |     |      |       |
| Dấu nháy đơn `'`    | Chuỗi có sao ghi vậy (verbatim string) | Chuỗi có sao ghi vậy (verbatim string) | Chuỗi có sao ghi vậy (verbatim string)                    |                                   |              |                               |         |     |      |       |
| Dấu backtick ` `` ` | Expandable string                      |                                        | Thoát khỏi ký tự đặc biệt, ngắt dòng                      |                                   |              |                               |         |     |      |       |
| Dấu đô la `$`       |                                        |                                        | `$biến`, `$env:path`                                      |                                   |              |                               |         |     |      |       |
| Dấu phần trăm `%`   |                                        |                                        | `ForEach-Object`                                          |                                   | `%biến%`     |                               | `%biến` |     |      |       |
| Dấu chéo `\`        |                                        |                                        |                                                           |                                   |              |                               |         |     |      |       |
| Dấu chéo ngược `/`  |                                        |                                        |                                                           |                                   |              |                               |         |     |      |       |
| Dấu sao `*`         |                                        |                                        |                                                           |                                   |              |                               |         |     |      |       |
| Dấu a còng `@`      |                                        |                                        | Chèn nhiều tham số vào cùng lúc (splatting)               | [HEAD](../../%F0%9F%97%84%EF%B8%8FT%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%93ng%20b%E1%BB%99,%20sao%20l%C6%B0u/Git/Blob,%20tree,%20ref.%20B%C3%AAn%20trong%20Git/Ref/HEAD/HEAD%20l%C3%A0%20commit%20hi%E1%BB%87n%20t%E1%BA%A1i.md) |              | Scope                         |         |     |      |       |
| Dấu thăng `#`       |                                        |                                        | `# comment`. Mẹo: dùng `##` ở trên function               |                                   | `#directive` |                               |         |     |      |       |
| Dấu chấm phẩy `;`   |                                        |                                        |                                                           |                                   | `; comment`  |                               |         |     |      |       |
| Dấu gạch đứng `\|`  |                                        |                                        | Pipe                                                      |                                   |              |                               |         |     |      |       |
| Dấu chấm hỏi `?`    |                                        |                                        | `Where-Object`                                            |                                   |              |                               |         |     |      |       |
| Dấu lớn hơn `>`     |                                        |                                        |                                                           |                                   |              | Child combinator              |         |     |      |       |
| Dấu cộng `+`        |                                        |                                        |                                                           |                                   |              | Next-sibling combinator       |         |     |      |       |
| Dấu ngã `~`         |                                        |                                        |                                                           |                                   |              | Subsequent-sibling combinator |         |     |      |       |
| Ký tự               | JavaScript                             | Python                                 | PowerShell                                                |                                   | AutoHotKey   | CSS                           | CMD     | SQL | Bash | LaTeX |



Ưu tiên dấu nháy đơn `'` hơn là nháy kép `"`. Tuy nhiên nhớ rằng [trong JSON thì chỉ có thể dùng nháy kép chứ không được dùng nháy đơn](../../%F0%9F%97%84%EF%B8%8FT%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%8Bnh%20d%E1%BA%A1ng%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%8Bnh%20d%E1%BA%A1ng%20v%C4%83n%20b%E1%BA%A3n/JSON/JSON%20kh%C3%B4ng%20cho%20ph%C3%A9p%20%C4%91%E1%BB%83%20d%C6%B0%20d%E1%BA%A5u%20ph%E1%BA%A9y,%20kh%C3%B4ng%20c%C3%B3%20comment,%20thu%E1%BB%99c%20t%C3%ADnh%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%C3%B3ng%20trong%20ngo%E1%BA%B7c%20k%C3%A9p.md).

[The Complete Guide to PowerShell Punctuation - Simple Talk](https://www.red-gate.com/simple-talk/sysadmin/powershell/the-complete-guide-to-powershell-punctuation/)

