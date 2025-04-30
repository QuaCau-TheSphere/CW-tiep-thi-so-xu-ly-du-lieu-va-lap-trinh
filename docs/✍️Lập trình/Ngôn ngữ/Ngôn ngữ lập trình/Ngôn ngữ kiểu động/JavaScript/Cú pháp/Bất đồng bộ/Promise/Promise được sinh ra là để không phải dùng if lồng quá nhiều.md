---
share: true
created: 2023-10-24T18:26
updated: 2025-03-03T18:48
alias: Promise được sinh ra để giải quyết những rắc rối của việc dùng quá nhiều callback.
---
Promise được sinh ra để giải quyết những rắc rối của việc dùng quá nhiều callback. [Callback là những hàm được dùng như đối số của hàm khác và đã xác định sẵn đối số truyền vào cho nó rồi](../../../../../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/H%C3%A0m/Callback%20l%C3%A0%20nh%E1%BB%AFng%20h%C3%A0m%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20nh%C6%B0%20%C4%91%E1%BB%91i%20s%E1%BB%91%20c%E1%BB%A7a%20h%C3%A0m%20kh%C3%A1c%20v%C3%A0%20%C4%91%C3%A3%20x%C3%A1c%20%C4%91%E1%BB%8Bnh%20s%E1%BA%B5n%20%C4%91%E1%BB%91i%20s%E1%BB%91%20truy%E1%BB%81n%20v%C3%A0o%20cho%20n%C3%B3%20r%E1%BB%93i.md)
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


[await với async là cách để viết hàm bất đồng bộ với tư duy khi viết hàm tuần tự](../await/await%20v%E1%BB%9Bi%20async%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20vi%E1%BA%BFt%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20v%E1%BB%9Bi%20t%C6%B0%20duy%20khi%20vi%E1%BA%BFt%20h%C3%A0m%20tu%E1%BA%A7n%20t%E1%BB%B1.md)
[Sự bất đồng bộ có tính lây lan. Bất kỳ hàm nào gọi hàm bất đồng bộ đều trở thành hàm bất đồng bộ](../S%E1%BB%B1%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20c%C3%B3%20t%C3%ADnh%20l%C3%A2y%20lan.%20B%E1%BA%A5t%20k%E1%BB%B3%20h%C3%A0m%20n%C3%A0o%20g%E1%BB%8Di%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20%C4%91%E1%BB%81u%20tr%E1%BB%9F%20th%C3%A0nh%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99.md)
Tham khảo:: [Tất tần tật về Promise và async/await - Ehkoo](https://ehkoo.com/bai-viet/tat-tan-tat-ve-promise-va-async-await)