---
share: true
created: 2023-10-30T14:29
updated: 2025-05-02T11:37
title: "Có 2 chỗ để lưu ref: `.git/refs` và `.git/packed-refs`"
---
[Ref là hệ thống đặt tên các object](./Ref%20l%C3%A0%20h%E1%BB%87%20th%E1%BB%91ng%20%C4%91%E1%BA%B7t%20t%C3%AAn%20c%C3%A1c%20object.md). Mỗi file trong `.git/refs` là một ref. Nội dung mỗi file chỉ là commit hash. Nó dùng cho những ref thay đổi thường xuyên như branch. Còn `.git/packed-refs` là một file. Mỗi dòng trong đó là một commit hash và một ref. Nó dùng cho những ref ít thay đổi như tag. Việc này sẽ giúp làm git chạy nhanh hơn, vì đọc nhiều dòng một file sẽ nhanh hơn là đọc nhiều file một dòng.

Nguồn:: [Git - git-pack-refs Documentation](https://git-scm.com/docs/git-pack-refs)

[[Cái nào có ref thì `git gc` sẽ không đụng tới]]