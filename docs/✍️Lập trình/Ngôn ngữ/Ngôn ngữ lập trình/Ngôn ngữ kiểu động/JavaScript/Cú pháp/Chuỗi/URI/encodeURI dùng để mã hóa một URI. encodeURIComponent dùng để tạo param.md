---
share: true
created: 2023-10-30T14:29
updated: 2026-07-06T21:40
---
- `encodeURI()` mã hóa các ký tự đặc biệt, ngoại trừ: `~!@#$&*()=:/,;?+`
- `encodeURIComponent()` mã hóa các ký tự đặc biệt, ngoại trừ: `-_.!~*'()`

```js
s = "http://www.example.com/string with + and ? and & and spaces";
encodeURI(s)  //http://www.example.com/string%20with%20+%20and%20?%20and%20&%20and%20spaces
encodeURIComponent(s)  //http%3A%2F%2Fwww.example.com%2Fstring%20with%20%2B%20and%20%3F%20and%20%26%20and%20spaces
```

[javascript - What is the difference between decodeURIComponent and decodeURI? - Stack Overflow](https://stackoverflow.com/a/747712)

Nguồn:: [Should I use encodeURI or encodeURIComponent for encoding URLs?](https://stackoverflow.com/q/4540753/3416774)


If you're encoding a string to put in a URL component (a querystring parameter), you should call `encodeURIComponent`.

If you're encoding an existing URL, call `encodeURI`.
[Mọi URL đều là URI](../../../../../../../../%F0%9F%9B%9CM%E1%BA%A1ng%20m%C3%A1y%20t%C3%ADnh/T%C3%AAn%20mi%E1%BB%81n,%20URI/M%E1%BB%8Di%20URL%20%C4%91%E1%BB%81u%20l%C3%A0%20URI.md)


[encodeURI nên được đặt tên là fixBrokenURI, còn decodeURI nên được đặt là potentiallyBreakMyPreviouslyWorkingURI](./encodeURI%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%E1%BA%B7t%20t%C3%AAn%20l%C3%A0%20fixBrokenURI,%20c%C3%B2n%20decodeURI%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%E1%BA%B7t%20l%C3%A0%20potentiallyBreakMyPreviouslyWorkingURI.md)
