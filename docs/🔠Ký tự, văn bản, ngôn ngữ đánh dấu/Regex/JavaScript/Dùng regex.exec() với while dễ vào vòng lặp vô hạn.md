---
share: true
created: 2023-09-23T21:42
updated: 2024-08-25T20:40
---
Để tránh vào vòng lặp vô hạn, 
- Do _not_ place the regular expression literal (or [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) constructor) within the `while` condition — it will recreate the regex for every iteration and reset [`lastIndex`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/lastIndex).
- Be sure that the [global (`g`) flag](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions#advanced_searching_with_flags) is set, or `lastIndex` will never be advanced.
- If the regex may match zero-length characters (e.g. `/^/gm`), increase its [`lastIndex`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/lastIndex) manually each time to avoid being stuck in the same place.

Nguồn:: [MDN](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/MDN.md), [RegExp.prototype.exec() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/exec#examples "RegExp.prototype.exec() - JavaScript | MDN")
