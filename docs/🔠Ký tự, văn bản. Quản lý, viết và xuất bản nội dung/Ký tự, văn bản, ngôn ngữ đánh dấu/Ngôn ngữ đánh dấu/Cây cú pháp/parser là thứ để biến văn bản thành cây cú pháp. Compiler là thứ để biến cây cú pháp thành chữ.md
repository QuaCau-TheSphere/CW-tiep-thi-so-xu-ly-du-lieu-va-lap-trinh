---
share: true
created: 2023-10-30T14:29
updated: 2024-11-30T13:54
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
[Compile time là lúc chuyển từ ngôn ngữ lập trình mà người hiểu sang ngôn ngữ máy chỉ có máy mới hiểu. Runtime là lúc máy chạy mã máy](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi/Compile%20time%20l%C3%A0%20l%C3%BAc%20chuy%E1%BB%83n%20t%E1%BB%AB%20ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh%20m%C3%A0%20ng%C6%B0%E1%BB%9Di%20hi%E1%BB%83u%20sang%20ng%C3%B4n%20ng%E1%BB%AF%20m%C3%A1y%20ch%E1%BB%89%20c%C3%B3%20m%C3%A1y%20m%E1%BB%9Bi%20hi%E1%BB%83u.%20Runtime%20l%C3%A0%20l%C3%BAc%20m%C3%A1y%20ch%E1%BA%A1y%20m%C3%A3%20m%C3%A1y.md)