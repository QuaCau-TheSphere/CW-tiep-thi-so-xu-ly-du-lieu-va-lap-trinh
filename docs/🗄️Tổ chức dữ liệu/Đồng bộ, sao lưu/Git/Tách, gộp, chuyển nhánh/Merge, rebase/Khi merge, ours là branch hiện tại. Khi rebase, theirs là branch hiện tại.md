---
share: true
created: 2023-10-30T14:29
updated: 2025-05-02T17:10
---
[git merge B nên được hiểu là git merge A with B. git rebase A nên được hiểu là git rebase B to A](./git%20merge%20B%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20hi%E1%BB%83u%20l%C3%A0%20git%20merge%20A%20with%20B.%20git%20rebase%20A%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20hi%E1%BB%83u%20l%C3%A0%20git%20rebase%20B%20to%20A.md)
Giả sử ta có 2 branch `A` và `B`. Ta đang ở A:
```
$ git branch
* A
  B
```

Khi merge là lấy commit từ branch khác về branch hiện tại, nên `A` sẽ là `ours`:
```
$ git merge -X ours B
```
Khi rebase thì bị ngược như vậy là vì 
```
# Nếu là rebase thì A là theirs
$ git rebase -X theirs B
```

Có lẽ thay vì dùng `ours` – `theirs`, ta nên dùng `current` – `theirs` cho merge, và `current` – `ours` cho rebase?