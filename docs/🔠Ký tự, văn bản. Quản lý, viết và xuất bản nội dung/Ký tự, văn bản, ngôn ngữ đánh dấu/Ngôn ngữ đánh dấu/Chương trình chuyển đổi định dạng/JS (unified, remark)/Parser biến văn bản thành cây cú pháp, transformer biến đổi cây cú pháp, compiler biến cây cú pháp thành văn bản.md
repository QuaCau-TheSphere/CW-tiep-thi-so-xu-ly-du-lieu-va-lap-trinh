---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
```
| ........................ process ........................... |
| .......... parse ... | ... run ... | ... stringify ..........|

          +--------+                     +----------+
Input ->- | Parser | ->- Syntax Tree ->- | Compiler | ->- Output
          +--------+          |          +----------+
                              X
                              |
                       +--------------+
                       | Transformers |
                       +--------------+
```
Nguồn:: 
Trong pandoc thì parser, transformer với compiler lần lượt được gọi là [reader, filter, writer](../Pandoc/Reader%20bi%E1%BA%BFn%20v%C4%83n%20b%E1%BA%A3n%20th%C3%A0nh%20c%C3%A2y%20c%C3%BA%20ph%C3%A1p,%20filter%20bi%E1%BA%BFn%20%C4%91%E1%BB%95i%20c%C3%A2y%20c%C3%BA%20ph%C3%A1p,%20writer%20bi%E1%BA%BFn%20c%C3%A2y%20c%C3%BA%20ph%C3%A1p%20th%C3%A0nh%20v%C4%83n%20b%E1%BA%A3n.md)

Chữ "compile" ở đây không quá chính xác, vì [Compile thực sự là việc chuyển từ ngôn ngữ lập trình mà người hiểu sang ngôn ngữ máy chỉ có máy mới hiểu](../../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Ki%E1%BB%83u%20v%C3%A0%20vi%E1%BB%87c%20th%E1%BB%B1c%20thi/Compile%20time%20l%C3%A0%20l%C3%BAc%20chuy%E1%BB%83n%20t%E1%BB%AB%20ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh%20m%C3%A0%20ng%C6%B0%E1%BB%9Di%20hi%E1%BB%83u%20sang%20ng%C3%B4n%20ng%E1%BB%AF%20m%C3%A1y%20ch%E1%BB%89%20c%C3%B3%20m%C3%A1y%20m%E1%BB%9Bi%20hi%E1%BB%83u.%20Runtime%20l%C3%A0%20l%C3%BAc%20m%C3%A1y%20ch%E1%BA%A1y%20m%C3%A3%20m%C3%A1y.md). Nó nên hiểu là "converter" thì đúng hơn.