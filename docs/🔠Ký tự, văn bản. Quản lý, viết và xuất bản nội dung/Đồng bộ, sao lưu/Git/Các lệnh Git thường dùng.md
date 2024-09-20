---
share: true
created: 2023-05-26T14:51
updated: 2024-09-20T13:55
---
## Xem danh sách tất cả commit
```bash
git log --oneline
git log --oneline --graph
git log --pretty='%C(yellow)%h %C(cyan)%cd%C(auto)%d %Creset%s' --graph --date=relative --date-order
```
## Biết xem một commit có những thay đổi
```
git show --stat <commit>
git diff <commit>^!
```
## Xem danh sách tất cả file trong commit mình chọn
```bash
git ls-tree --name-only -r <commitHash>
git ls-tree --name-only 9dea936:"Tài nguyên hỗ trợ/Công việc thời vụ kiếm tiền nhanh"
```
- Bỏ `-r` để không recurse 
## Đọc nội dung một file trong một commit cũ
```
git show <commitHash>:/path/to/file
```
Nếu muốn mở trong vim thì:
```
git show <commitHash>:/path/to/file | vim -
```
Nhược điểm của việc này là vì vim đọc trực tiếp từ stdin, nên không biết định dạng file là gì để mà tô màu. Có thể sửa việc này bằng:
```
git show <commitHash>:/path/to/file | vim -c 'set filetype=python' -
```

Xem thêm:: [Các lỗi Git thường gặp](./C%C3%A1c%20l%E1%BB%97i%20Git%20th%C6%B0%E1%BB%9Dng%20g%E1%BA%B7p.md)