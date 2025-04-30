---
share: true
created: 2023-05-26T14:51
updated: 2025-03-26T16:21
---
[GitHub - GitAlias/gitalias: Git alias commands for faster easier version control](https://github.com/GitAlias/gitalias)
[GitHub - initialcommit-com/git-sim: Visually simulate Git operations in your own repos with a single terminal command.](https://github.com/initialcommit-com/git-sim)

## Xem danh sách tất cả commit
```bash
git log --oneline
git log --oneline --graph
git log --pretty='%C(yellow)%h %C(cyan)%cd%C(auto)%d %Creset%s' --graph --date=relative --date-order
```

## Xem những thay đổi của một commit
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

## Tìm commit sớm nhất chứa file
```PowerShell
git log --follow --diff-filter=A --find-renames=40% --pretty=reference -- "**Thông tin cho đại lý.md" 
```

## Khởi tạo repo mới và đẩy lên GitHub
```PowerShell
$repo = 'QuaCau-TheSphere/CA-Bao-hiem'
git init
git add -A
git commit -m "init"

gh repo create --public $repo
$url = gh repo view $repo --json url --jq '.url'
git remote add origin $url 
git push -u origin main
```
[Mẹo dùng Git với Obsidian](../../Tr%C3%ACnh%20so%E1%BA%A1n%20th%E1%BA%A3o%20(Obsidian)/M%E1%BA%B9o%20d%C3%B9ng%20Git%20v%E1%BB%9Bi%20Obsidian.md)
Xem thêm:: [Các lỗi Git thường gặp](./C%C3%A1c%20l%E1%BB%97i%20Git%20th%C6%B0%E1%BB%9Dng%20g%E1%BA%B7p.md), [Git tag](./Git%20tag.md)
Xem thêm:: [GitHub - git-tips/tips: Most commonly used git tips and tricks.](https://github.com/git-tips/tips?tab=readme-ov-file#readme)