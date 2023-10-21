---
share: true
created: 2023-08-25T14:20
updated: 2023-09-23T14:46
---
[Why does /đ\b/ not match đ? (duplicate)](https://stackoverflow.com/q/76627655/3416774)
Nếu dùng `(?=$|\P{L})` thì lại chạy lâu. Dễ nhất là thêm khoảng trắng ở ngay sau input và 
```js
input = input + ' '
var regex = new RegExp(word + ' ', 'gi');
const test = regex.test(input)
```
[Ý nghĩa của biểu thức regex trong hàm lọcDữLiệuCầnTựĐộngNhậnDạng()](../../../%F0%9F%91%8FTr%E1%BA%A5n%20K%E1%BB%B3/H%C6%B0%E1%BB%9Bng%20d%E1%BA%ABn%20s%E1%BB%AD%20d%E1%BB%A5ng%20Tr%E1%BA%A5n%20K%E1%BB%B3/3.%20Hi%E1%BB%83u%20code%20n%C3%B3i%20g%C3%AC/%C3%9D%20ngh%C4%A9a%20c%E1%BB%A7a%20bi%E1%BB%83u%20th%E1%BB%A9c%20regex%20trong%20h%C3%A0m%20l%E1%BB%8DcD%E1%BB%AFLi%E1%BB%87uC%E1%BA%A7nT%E1%BB%B1%C4%90%E1%BB%99ngNh%E1%BA%ADnD%E1%BA%A1ng().md#)
Nguồn:: [Stack Overflow](../../../%E2%9A%A1Hi%E1%BB%83u%20bi%E1%BA%BFt%20s%C3%A2u/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md#), [How can I use Unicode-aware regular expressions in JavaScript?](https://stackoverflow.com/a/52205643/3416774)