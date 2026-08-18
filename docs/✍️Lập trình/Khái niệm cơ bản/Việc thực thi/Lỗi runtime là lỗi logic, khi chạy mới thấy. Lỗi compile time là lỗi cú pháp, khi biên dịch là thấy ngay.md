---
share: true
created: 2023-10-30T14:29
updated: 2026-08-10T16:08
---
Nguồn:: [câu hỏi thắc mắc về run time , compile time và translation time - programming - Dạy Nhau Học](https://daynhauhoc.com/t/cau-hoi-thac-mac-ve-run-time-compile-time-va-translation-time/5686)

![](https://www.monkeyuser.com/2017/compile-vs-runtime-error/70-runtime-vs-compile-time-errors.png)
[Vì lỗi compile time là lỗi cú pháp, và vì language server giúp bắt lỗi cú pháp, nên nó khiến cho code editor trở thành IDE mà không cần có compiler](../../C%C3%B4ng%20c%E1%BB%A5/IDE/V%C3%AC%20l%E1%BB%97i%20compile%20time%20l%C3%A0%20l%E1%BB%97i%20c%C3%BA%20ph%C3%A1p,%20v%C3%A0%20v%C3%AC%20language%20server%20gi%C3%BAp%20b%E1%BA%AFt%20l%E1%BB%97i%20c%C3%BA%20ph%C3%A1p,%20n%C3%AAn%20n%C3%B3%20khi%E1%BA%BFn%20cho%20code%20editor%20tr%E1%BB%9F%20th%C3%A0nh%20IDE%20m%C3%A0%20kh%C3%B4ng%20c%E1%BA%A7n%20c%C3%B3%20compiler.md)

[Can all compiler errors be caught by language server?](https://software.codidact.com/posts/296487)
One example is an assignment to a variable where the expression is a symbol. When that symbol is the name of a variable of the correct type, then that's fine. If the symbol is something that doesn't result in an expression or an expression of the wrong type (depending on language), then it's a compile-time error. However, it is still _syntactically_ correct.