---
share: true
created: 2023-10-24T18:26
updated: 2024-04-27T16:19
---
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
# Toán hạng tham chiếu
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
