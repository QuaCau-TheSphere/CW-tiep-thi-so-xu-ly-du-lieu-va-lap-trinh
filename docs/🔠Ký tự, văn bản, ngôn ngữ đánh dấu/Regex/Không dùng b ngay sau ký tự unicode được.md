---
share: true
created: 2023-08-25T14:20
updated: 2024-08-25T20:54
title: Không dùng \b ngay sau ký tự unicode được
---
[Why does /đ\b/ not match đ? (duplicate)](https://stackoverflow.com/q/76627655/3416774)
Nếu dùng `(?=$|\P{L})` thì lại chạy lâu. Dễ nhất là thêm khoảng trắng ở ngay sau input và 
```js
input = input + ' '
var regex = new RegExp(word + ' ', 'gi');
const test = regex.test(input)
```
[Ý nghĩa của biểu thức regex trong hàm lọcDữLiệuCầnTựĐộngNhậnDạng()](../../%E2%9A%92%EF%B8%8FNhu%20c%E1%BA%A7u%20c%C3%B4ng%20vi%E1%BB%87c/Ph%C3%A2n%20lo%E1%BA%A1i%20d%E1%BB%AF%20li%E1%BB%87u%20(Tr%E1%BA%A5n%20K%E1%BB%B3)/3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/%C3%9D%20ngh%C4%A9a%20c%E1%BB%A7a%20bi%E1%BB%83u%20th%E1%BB%A9c%20regex%20trong%20h%C3%A0m%20l%E1%BB%8DcD%E1%BB%AFLi%E1%BB%87uC%E1%BA%A7nT%E1%BB%B1%C4%90%E1%BB%99ngNh%E1%BA%ADnD%E1%BA%A1ng().md)
Nguồn:: [Stack Overflow](../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [How can I use Unicode-aware regular expressions in JavaScript?](https://stackoverflow.com/a/52205643/3416774)
