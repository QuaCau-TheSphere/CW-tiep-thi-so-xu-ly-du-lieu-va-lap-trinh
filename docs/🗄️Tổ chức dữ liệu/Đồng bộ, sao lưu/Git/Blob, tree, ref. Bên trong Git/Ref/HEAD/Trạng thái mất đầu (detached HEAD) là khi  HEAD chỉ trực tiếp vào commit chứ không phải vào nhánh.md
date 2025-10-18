---
share: true
created: 2023-10-30T14:29
updated: 2025-10-17T12:10
---
Khi dùng `git status` và nó ghi `On branch main`nghĩa là tệp `.git/HEAD` đang ghi `ref: refs/heads/main`. Nếu nội dung `.git/HEAD` chỉ ghi commit chứ không phải ref nhánh thì đó là trạng thái mất đầu.

[Ref là hệ thống đặt tên các object](../Ref%20l%C3%A0%20h%E1%BB%87%20th%E1%BB%91ng%20%C4%91%E1%BA%B7t%20t%C3%AAn%20c%C3%A1c%20object.md)
[[Có 2 chỗ để lưu ref|Có 2 chỗ để lưu ref: `.git/refs` và `.git/packed-refs`]]