---
share: true
created: 2023-10-30T14:29
updated: 2024-11-25T14:48
---
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
[Nếu không dùng hàm bất đồng bộ để gọi tiến trình khác, thì JS sẽ tiếp tục chạy các lệnh sau đó mà không chờ tiến trình chạy xong. Kết quả là các lệnh phụ thuộc vào kết quả của tiến trình đó sẽ bị lỗi](N%E1%BA%BFu%20kh%C3%B4ng%20d%C3%B9ng%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20%C4%91%E1%BB%83%20g%E1%BB%8Di%20ti%E1%BA%BFn%20tr%C3%ACnh%20kh%C3%A1c,%20th%C3%AC%20JS%20s%E1%BA%BD%20ti%E1%BA%BFp%20t%E1%BB%A5c%20ch%E1%BA%A1y%20c%C3%A1c%20l%E1%BB%87nh%20sau%20%C4%91%C3%B3%20m%C3%A0%20kh%C3%B4ng%20ch%E1%BB%9D%20ti%E1%BA%BFn%20tr%C3%ACnh%20ch%E1%BA%A1y%20xong.%20K%E1%BA%BFt%20qu%E1%BA%A3%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20ph%E1%BB%A5%20thu%E1%BB%99c%20v%C3%A0o%20k%E1%BA%BFt%20qu%E1%BA%A3%20c%E1%BB%A7a%20ti%E1%BA%BFn%20tr%C3%ACnh%20%C4%91%C3%B3%20s%E1%BA%BD%20b%E1%BB%8B%20l%E1%BB%97i.md)

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

[Chương trình là một đoạn mã được lưu trên ổ đĩa. Tiến trình là khi đoạn mã đó được nạp vào RAM và được CPU đọc](../../../../../../H%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh,%20path%20v%C3%A0%20terminal/CPU,%20RAM/Ch%C6%B0%C6%A1ng%20tr%C3%ACnh%20l%C3%A0%20m%E1%BB%99t%20%C4%91o%E1%BA%A1n%20m%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20l%C6%B0u%20tr%C3%AAn%20%E1%BB%95%20%C4%91%C4%A9a.%20Ti%E1%BA%BFn%20tr%C3%ACnh%20l%C3%A0%20khi%20%C4%91o%E1%BA%A1n%20m%C3%A3%20%C4%91%C3%B3%20%C4%91%C6%B0%E1%BB%A3c%20n%E1%BA%A1p%20v%C3%A0o%20RAM%20v%C3%A0%20%C4%91%C6%B0%E1%BB%A3c%20CPU%20%C4%91%E1%BB%8Dc.md)

Chính vì như vậy, những hàm dùng để tương tác với tiến trình khác đều luôn được viết ở dạng bất đồng bộ, kể cả khi việc phiên bản đồng bộ không thay đổi gì. 

Tham khảo:
- [javascript - Why are almost all Puppeteer calls asynchronous? - Stack Overflow](https://stackoverflow.com/q/71368256/3416774)
- [Introduction: callbacks](https://javascript.info/callbacks)