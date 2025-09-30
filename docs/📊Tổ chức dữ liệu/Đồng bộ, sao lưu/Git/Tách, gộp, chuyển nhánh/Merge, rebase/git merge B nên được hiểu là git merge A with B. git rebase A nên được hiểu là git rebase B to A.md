---
share: true
created: 2023-10-30T14:29
updated: 2025-05-01T16:29
---
Giả sử ta có 2 branch `A` và `B`. Ta đều muốn gắn B lên A.

Khi merge là lấy commit từ nơi khác về mình. Nên nếu muốn gắn B lên A thì phải đứng ở A để gọi lệnh merge lên B:
```
git switch A
git merge B
```

Tức là lúc này nên đọc lệnh này là:
```
git merge B (into A)
git merge (A with) B 
```

Còn rebase là bứng commit hiện tại sang nơi khác. Nếu muốn gắn B lên A thì phải đứng ở B để gọi lệnh rebase lên A:
```
git switch B
git rebase A
```

Tức là lúc này nên đọc lệnh này là:
```
git rebase (B to) A
```

## 2 tham số
```
git switch B
git rebase A
```
Tương đương với
```
git rebase A B
```

[Khi merge, ours là branch hiện tại. Khi rebase, theirs là branch hiện tại](./Khi%20merge,%20ours%20l%C3%A0%20branch%20hi%E1%BB%87n%20t%E1%BA%A1i.%20Khi%20rebase,%20theirs%20l%C3%A0%20branch%20hi%E1%BB%87n%20t%E1%BA%A1i.md)
Nguồn:: <iframe width="560" height="315" src="https://www.youtube.com/embed/xot40u-_1FI?si=NZpW5vl5Fq-WtjJL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

```git
git checkout foo
git checkout -b newbar
git cherry-pick C D E
git checkout bar
git reset --hard newbar
git branch -d newbar`
```
is equivalent to this:
```
git rebase foo bar
```
Nguồn:: [A Helpful Mnemonic for 'git rebase' Arguments // Think Like (a) Git](https://think-like-a-git.net/sections/rebase-from-the-ground-up/a-helpful-mnemonic-for-git-rebase-arguments.html)