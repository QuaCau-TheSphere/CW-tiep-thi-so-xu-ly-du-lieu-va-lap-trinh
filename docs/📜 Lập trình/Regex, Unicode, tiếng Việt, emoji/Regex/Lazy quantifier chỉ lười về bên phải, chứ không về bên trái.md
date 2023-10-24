---
share: true
created: 2023-10-24T16:28
updated: 2023-10-24T18:26
---
Nếu bạn có chuỗi sau:
```
START START word word word END
```
và có regex này với cờ `gm`:
```
START.*?END
```

Thì kết quả sẽ không phải là:
```
START word word word END
```

mà là nguyên chuỗi gốc.

Nhưng nếu chuỗi có dạng:
```
START word word word END END
```

Thì nó sẽ ra đúng kết quả.

Nguồn:: [Stack Overflow](../../../%E2%9A%A1Hi%E1%BB%83u%20bi%E1%BA%BFt%20s%C3%A2u/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md#), [Why is the lazy quantifier indeed lazy to the right, but not to the left?](https://stackoverflow.com/q/77134671/3416774)