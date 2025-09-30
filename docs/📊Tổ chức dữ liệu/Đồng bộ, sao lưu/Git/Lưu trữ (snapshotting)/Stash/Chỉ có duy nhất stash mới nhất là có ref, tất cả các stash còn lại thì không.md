---
share: true
created: 2023-10-30T14:29
updated: 2025-05-02T14:08
---
the commits are created ; the "past stashes" are not referenced by any ref anymore, they are listed in the reflog for the `stash` ref. So: `git reflog stash`, or `cat .git/logs/refs/stash`. The past stashes will eventually be deleted by the gc mechanism -- as for the reflog entries of any other ref.
[Ref là hệ thống đặt tên các object](../../Blob,%20tree,%20ref.%20B%C3%AAn%20trong%20Git/Ref/Ref%20l%C3%A0%20h%E1%BB%87%20th%E1%BB%91ng%20%C4%91%E1%BA%B7t%20t%C3%AAn%20c%C3%A1c%20object.md). [[Cái nào có ref thì `git gc` sẽ không đụng tới]]
[[Có 2 chỗ để lưu ref|Có 2 chỗ để lưu ref: `.git/refs` và `.git/packed-refs`]]
Nguồn:: 