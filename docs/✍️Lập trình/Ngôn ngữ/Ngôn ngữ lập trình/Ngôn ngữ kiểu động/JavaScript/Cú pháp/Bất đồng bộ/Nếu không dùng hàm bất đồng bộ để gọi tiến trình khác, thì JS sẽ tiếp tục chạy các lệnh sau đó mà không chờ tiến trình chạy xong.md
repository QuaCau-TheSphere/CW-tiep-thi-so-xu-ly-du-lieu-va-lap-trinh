---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
Kết quả là các lệnh phụ thuộc vào kết quả của tiến trình đó sẽ bị lỗi
```js
readFile("./data.txt", (error, result) => {
  // This callback will be called when the task is done, with the
  // final `error` or `result`. Any operation dependent on the
  // result must be defined within this callback.
});
// Code here is immediately executed after the `readFile` request
// is fired. It does not wait for the callback to be called, hence
// making `readFile` "asynchronous".
```

```js
function loadScript(src, callback) {
  let script = document.createElement('script');
  script.src = src;
  script.onload = () => callback(script);
  document.head.append(script);
}

loadScript('https://cdnjs.cloudflare.com/ajax/libs/lodash.js/3.2.0/lodash.js', script => {
  alert(`Cool, the script ${script.src} is loaded`);
  alert( _ ); // _ is a function declared in the loaded script
});
```

[Chương trình là một đoạn mã được lưu trên ổ đĩa. Tiến trình là khi đoạn mã đó được nạp vào RAM và được CPU đọc](../../../../../../../%F0%9F%A4%96%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn,%20ti%E1%BA%BFn%20tr%C3%ACnh,%20terminal,%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh/Ch%C6%B0%C6%A1ng%20tr%C3%ACnh,%20ti%E1%BA%BFn%20tr%C3%ACnh/Ch%C6%B0%C6%A1ng%20tr%C3%ACnh%20l%C3%A0%20m%E1%BB%99t%20%C4%91o%E1%BA%A1n%20m%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20l%C6%B0u%20tr%C3%AAn%20%E1%BB%95%20%C4%91%C4%A9a.%20Ti%E1%BA%BFn%20tr%C3%ACnh%20l%C3%A0%20khi%20%C4%91o%E1%BA%A1n%20m%C3%A3%20%C4%91%C3%B3%20%C4%91%C6%B0%E1%BB%A3c%20n%E1%BA%A1p%20v%C3%A0o%20RAM%20v%C3%A0%20%C4%91%C6%B0%E1%BB%A3c%20CPU%20%C4%91%E1%BB%8Dc.md)

Chính vì như vậy, những hàm dùng để tương tác với tiến trình khác đều luôn được viết ở dạng bất đồng bộ, kể cả khi việc phiên bản đồng bộ không thay đổi gì. 

Tham khảo:
- [javascript - Why are almost all Puppeteer calls asynchronous? - Stack Overflow](https://stackoverflow.com/q/71368256/3416774)
- [Introduction: callbacks](https://javascript.info/callbacks)