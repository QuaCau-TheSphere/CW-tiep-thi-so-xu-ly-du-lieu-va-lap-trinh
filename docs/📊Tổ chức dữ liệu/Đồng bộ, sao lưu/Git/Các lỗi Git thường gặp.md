---
share: true
created: 2024-09-19T17:01
updated: 2025-09-27T16:19
---
[git reflog là phao cứu sinh cho những lỗi lầm khi dùng Git](./Blob,%20tree,%20ref.%20B%C3%AAn%20trong%20Git/Ref/git%20reflog%20l%C3%A0%20phao%20c%E1%BB%A9u%20sinh%20cho%20nh%E1%BB%AFng%20l%E1%BB%97i%20l%E1%BA%A7m%20khi%20d%C3%B9ng%20Git.md)
## Quên add

## Không thấy folder mình tạo được add
Lý do:: [Git không biết gì về folder](./L%C6%B0u%20tr%E1%BB%AF%20(snapshotting)/Git%20kh%C3%B4ng%20bi%E1%BA%BFt%20g%C3%AC%20v%E1%BB%81%20folder.md)

## Thêm file vào  .gitignore rồi mà vẫn không thấy file bị ignore

## Lỡ commit file nặng
```
git filter-branch --force --index-filter 'git rm -r --cached --ignore-unmatch bigfile.txt' --prune-empty --tag-name-filter cat -- --all
```

## Lỡ commit secret
### B1. Xác định commit sớm nhất chứa secret
Nếu biết secret đó là gì thì dùng git blame luôn. Nếu không biết thì xem trong lỗi để biết nó là commit nào. Nếu nó ghi nhiều commit thì dùng git log để xem cái nào là commit sớm nhất. Nếu nó không ghi commit mà ghi blob thì dùng 
```
git log --all --find-object=<BLOB-ID>
```

([Blob có thể hiểu là hash của một file, còn commit là hash của cả folder tổng](./Blob,%20tree,%20ref.%20B%C3%AAn%20trong%20Git/C%C3%B3%20th%E1%BB%83%20hi%E1%BB%83u%20blob%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20t%E1%BB%87p,%20tree%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20th%C6%B0%20m%E1%BB%A5c,%20c%C3%B2n%20commit%20th%E1%BB%B1c%20ra%20ch%E1%BB%89%20l%C3%A0%20hash%20c%E1%BB%A7a%20c%E1%BA%A3%20th%C6%B0%20m%E1%BB%A5c%20t%E1%BB%95ng.md))

### B2. `git rebase -i <COMMIT-ID>~1`
[~ và ^ là để chỉ các commit trước đó](./Blob,%20tree,%20ref.%20B%C3%AAn%20trong%20Git/Ref/D%E1%BA%A5u%20ng%C3%A3%20v%C3%A0%20d%E1%BA%A5u%20m%C5%A9%20l%C3%A0%20%C4%91%E1%BB%83%20ch%E1%BB%89%20c%C3%A1c%20commit%20tr%C6%B0%E1%BB%9Bc%20%C4%91%C3%B3.md)

### B3. đổi pick sang edit ở commit sớm nhất
Sau khi lưu lại, nếu nó xuất hiện dòng:
```
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue
```
Thì là bước này thành công.

### B4. Xoá file chứa secret
Nếu là file tự tạo ra thì cần thêm vào .gitignore  
```
add-Content .\.gitignore .obsidian/plugins/obsidian-mkdocs-publisher/logs.txt && git rm --cache -r . && git add -A && git commit --amend --no-edit && git rebase --continue && git add -A && git rebase --continue
```
### `git commit --amend`
###  `git rebase --continue`

Xem thêm:: [Các lệnh Git thường dùng](./C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)