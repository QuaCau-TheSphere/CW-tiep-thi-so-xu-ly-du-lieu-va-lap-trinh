---
share: true
created: 2023-10-24T18:26
updated: 2026-07-24T21:47
---
[JavaScript cố gắng đoán ý định của người viết chứ không báo lỗi](../../../../../%C3%9D%20%C4%91%E1%BB%93%20thi%E1%BA%BFt%20k%E1%BA%BF/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript%20c%E1%BB%91%20g%E1%BA%AFng%20%C4%91o%C3%A1n%20%C3%BD%20%C4%91%E1%BB%8Bnh%20c%E1%BB%A7a%20ng%C6%B0%E1%BB%9Di%20vi%E1%BA%BFt%20ch%E1%BB%A9%20kh%C3%B4ng%20b%C3%A1o%20l%E1%BB%97i.md)
=== là == mà không đổi kiểu (type conversion).

```js
'' == '0'           // false
0 == ''             // true
0 == '0'            // true

false == 'false'    // false
false == '0'        // true

false == undefined  // false
false == null       // false
null == undefined   // true

' \t\r\n ' == 0     // true
```

![](https://i.stack.imgur.com/yISob.png) 
## Toán hạng tham chiếu
```js
var a = [1,2,3];
var b = [1,2,3];

var c = { x: 1, y: 2 };
var d = { x: 1, y: 2 };

var e = "text";
var f = "te" + "xt";

a == b            // false
a === b           // false

c == d            // false
c === d           // false

e == f            // true
e === f           // true
```

```js
"abc" == new String("abc")    // true
"abc" === new String("abc")   // false
```
Nguồn:: [Stack Overflow](../../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [Which equals operator (== vs ===) should be used in JavaScript comparisons?](https://stackoverflow.com/a/359509/3416774)

[JS Comparison Table](https://dorey.github.io/JavaScript-Equality-Table/unified/)

[Vì những người đầu tiên sử dụng JavaScript muốn tiện nên tác giả của nó đã làm nó có những thứ kỳ quặc](../../../../../%C3%9D%20%C4%91%E1%BB%93%20thi%E1%BA%BFt%20k%E1%BA%BF/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/V%C3%AC%20nh%E1%BB%AFng%20ng%C6%B0%E1%BB%9Di%20%C4%91%E1%BA%A7u%20ti%C3%AAn%20s%E1%BB%AD%20d%E1%BB%A5ng%20JavaScript%20mu%E1%BB%91n%20ti%E1%BB%87n%20n%C3%AAn%20t%C3%A1c%20gi%E1%BA%A3%20c%E1%BB%A7a%20n%C3%B3%20%C4%91%C3%A3%20l%C3%A0m%20n%C3%B3%20c%C3%B3%20nh%E1%BB%AFng%20th%E1%BB%A9%20k%E1%BB%B3%20qu%E1%BA%B7c.md)