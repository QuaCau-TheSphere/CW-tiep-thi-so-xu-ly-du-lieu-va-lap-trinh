---
share: true
created: 2023-08-25T14:20
updated: 2025-03-03T18:48
---
![regular_expressions.png](../../../attachments/regular_expressions.png)
Nguồn:: [208: Regular Expressions - explain xkcd](https://explainxkcd.com/wiki/index.php/208:_Regular_Expressions)
## Tạo query DQL từ danh sách các key
Do that in several steps. 
1) `^.*$` ⇒ `$& as "$&"`
2) `(?:\G|^\S*)\K\h+(?=.* as ".*"$)` ⇒ `-,`
3)  `(?:\G-|^)[^-]+(?=\S* as ".*"$)` ⇒ `\L$&`
https://stackoverflow.com/questions/75015542/how-to-convert-multiple-words-into-multiple-words-as-multiple-words

[Tự học regex](./T%E1%BB%B1%20h%E1%BB%8Dc%20regex.md)