---
share: true
created: 2023-10-30T14:29
updated: 2024-11-24T15:54
---
[Để lấy được giá trị state và result của promise, cần dùng các phương thức then và catch của nó](./%C4%90%E1%BB%83%20l%E1%BA%A5y%20%C4%91%C6%B0%E1%BB%A3c%20gi%C3%A1%20tr%E1%BB%8B%20state%20v%C3%A0%20result%20c%E1%BB%A7a%20promise,%20c%E1%BA%A7n%20d%C3%B9ng%20c%C3%A1c%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20then%20v%C3%A0%20catch%20c%E1%BB%A7a%20n%C3%B3.md)
[Vật thể promise có 2 thuộc tính là state và result, và 3 phương thức là then, catch, và finally](V%E1%BA%ADt%20th%E1%BB%83%20promise%20c%C3%B3%202%20thu%E1%BB%99c%20t%C3%ADnh%20l%C3%A0%20state%20v%C3%A0%20result,%20v%C3%A0%203%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20l%C3%A0%20then,%20catch,%20v%C3%A0%20finally.md)

![](https://javascript.info/article/promise-basics/promise-resolve-reject.svg)

Nguồn:: [Promise](https://javascript.info/promise-basics)
Nguồn:: [Tất tần tật về Promise và async/await - Ehkoo](https://ehkoo.com/bai-viet/tat-tan-tat-ve-promise-va-async-await)

- `.catch(errorHandlingFunction)` tương đương với `.then(null, errorHandlingFunction)`
- `.finally()` không cần đối số, và thường được dùng để dọn dẹp