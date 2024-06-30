---
share: true
created: 2023-10-24T18:26
updated: 2024-04-27T16:19
---
```js
api.getUser('pikalong', function (err, user) {
  if (err) throw err
  api.getPostsOfUser(user, function (err, posts) {
    if (err) throw err
    api.getCommentsOfPosts(posts, function (err, comments) {
      // vân vân và mây mây...
    })
  })
})
```

Ví dụ trên khi được viết lại bằng Promise sẽ là:

```js
api
  .getUser('pikalong')
  .then((user) => api.getPostsOfUser(user))
  .then((posts) => api.getCommentsOfPosts(posts))
  .catch((err) => {
    throw err
  })
```

Trích từ:: [Tất tần tật về Promise và async/await - Ehkoo](https://ehkoo.com/bai-viet/tat-tan-tat-ve-promise-va-async-await)
Promise được sinh ra để giải quyết những rắc rối của việc dùng quá nhiều callback. [Callback là những hàm được dùng như đối số của hàm khác](./Callback%20l%C3%A0%20nh%E1%BB%AFng%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20nh%C6%B0%20%C4%91%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20h%C3%A0m%20kh%C3%A1c.md)

[await với async là cách để viết hàm bất đồng bộ với tư duy khi viết hàm tuần tự](./await%20v%E1%BB%9Bi%20async%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20vi%E1%BA%BFt%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20v%E1%BB%9Bi%20t%C6%B0%20duy%20khi%20vi%E1%BA%BFt%20h%C3%A0m%20tu%E1%BA%A7n%20t%E1%BB%B1.md)
[Thực chất promise không giải quyết được chuyện lồng, vì promise cũng lồng vào nhau như if thôi. Thứ nó giải quyết là việc các giá trị trả về từ promise trông như không lồng vào nhau gì cả](./Th%E1%BB%B1c%20ch%E1%BA%A5t%20promise%20kh%C3%B4ng%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20%C4%91%C6%B0%E1%BB%A3c%20chuy%E1%BB%87n%20l%E1%BB%93ng,%20v%C3%AC%20promise%20c%C5%A9ng%20l%E1%BB%93ng%20v%C3%A0o%20nhau%20nh%C6%B0%20if%20th%C3%B4i.%20Th%E1%BB%A9%20n%C3%B3%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20l%C3%A0%20vi%E1%BB%87c%20c%C3%A1c%20gi%C3%A1%20tr%E1%BB%8B%20tr%E1%BA%A3%20v%E1%BB%81%20t%E1%BB%AB%20promise%20tr%C3%B4ng%20nh%C6%B0%20kh%C3%B4ng%20l%E1%BB%93ng%20v%C3%A0o%20nhau%20g%C3%AC%20c%E1%BA%A3.md) 