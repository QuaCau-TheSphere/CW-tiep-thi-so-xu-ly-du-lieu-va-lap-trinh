---
share: true
created: 2023-10-30T14:29
updated: 2024-04-23T01:41
title: ~ và ^ là để chỉ các commit trước đó
---
```
G   H   I   J
 \ /     \ /
  D   E   F
   \  |  / \
    \ | /   |
     \|/    |
      B     C
       \   /
        \ /
         A

A =      = A^0
B = A^   = A^1     = A~1
C = A^2
D = A^^  = A^1^1   = A~2
E = B^2  = A^^2
F = B^3  = A^^3
G = A^^^ = A^1^1^1 = A~3
H = D^2  = B^^2    = A^^^2  = A~2^2
I = F^   = B^3^    = A^^3^
J = F^2  = B^3^2   = A^^3^2
```


Lưu ý: `A~2 = D`, nhưng `A^2 = C`

> [!tip] Cách nhớ
> - `~` nằm ngang nên nó chỉ đi thẳng
> - `^` có sự hội tụ giữa hai đường nên nó là dành cho merge

[![Illustration of relative references in Git](https://i.stack.imgur.com/Ye1H7.jpg)](https://i.stack.imgur.com/Ye1H7.jpg)

[HEAD là commit hiện tại](./HEAD%20l%C3%A0%20commit%20hi%E1%BB%87n%20t%E1%BA%A1i.md). [@ là viết tắt của HEAD](./@%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a%20HEAD.md)
Nguồn:: [Stack Overflow](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [What's the difference between HEAD^ and HEAD\~ in Git? - Stack Overflow](https://stackoverflow.com/q/2221658/3416774)