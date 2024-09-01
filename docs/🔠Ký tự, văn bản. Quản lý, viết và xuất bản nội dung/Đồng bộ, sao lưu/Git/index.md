---
share: true
created: 2024-01-27T13:38
updated: 2024-09-01T18:00
title: Git
---

- \-: 
    - [Các lệnh Git thường dùng. Các lỗi Git thường gặp](./C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.%20C%C3%A1c%20l%E1%BB%97i%20Git%20th%C6%B0%E1%BB%9Dng%20g%E1%BA%B7p.md)
    - [Facebook chuyển sang Mercurial vì nhóm phát triển Git năm 2012 không mặn mà với monorepo](./Facebook%20chuy%E1%BB%83n%20sang%20Mercurial%20v%C3%AC%20nh%C3%B3m%20ph%C3%A1t%20tri%E1%BB%83n%20Git%20n%C4%83m%202012%20kh%C3%B4ng%20m%E1%BA%B7n%20m%C3%A0%20v%E1%BB%9Bi%20monorepo.md)
    - [Git giúp ta du hành thời gian](./Git%20gi%C3%BAp%20ta%20du%20h%C3%A0nh%20th%E1%BB%9Di%20gian.md)
    - [Real-time collaboration isn't necessary in most cases, but asynchronous collaboration](./Real-time%20collaboration%20isn't%20necessary%20in%20most%20cases,%20but%20asynchronous%20collaboration.md)
    - [Git tag](./Git%20tag.md)

- Blob, tree, ref. Bản chất của Git: 
    - [Có 4 loại object chính – blob, tree, commit, annotated tag](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/C%C3%B3%204%20lo%E1%BA%A1i%20object%20ch%C3%ADnh%20%E2%80%93%20blob,%20tree,%20commit,%20annotated%20tag.md)
    - [Có thể xem nội dung file với hash là như nhau. Nhưng file thì có thể có kích thước vô cùng lớn, còn hash thì luôn chỉ có 40 ký tự](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/C%C3%B3%20th%E1%BB%83%20xem%20n%E1%BB%99i%20dung%20file%20v%E1%BB%9Bi%20hash%20l%C3%A0%20nh%C6%B0%20nhau.%20Nh%C6%B0ng%20file%20th%C3%AC%20c%C3%B3%20th%E1%BB%83%20c%C3%B3%20k%C3%ADch%20th%C6%B0%E1%BB%9Bc%20v%C3%B4%20c%C3%B9ng%20l%E1%BB%9Bn,%20c%C3%B2n%20hash%20th%C3%AC%20lu%C3%B4n%20ch%E1%BB%89%20c%C3%B3%2040%20k%C3%BD%20t%E1%BB%B1.md)
    - [Bản chất của Git chỉ là những cặp giá trị key – value](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git%20ch%E1%BB%89%20l%C3%A0%20nh%E1%BB%AFng%20c%E1%BA%B7p%20gi%C3%A1%20tr%E1%BB%8B%20key%20%E2%80%93%20value.md)
    - [Có thể hiểu blob là hash của một file, tree là hash của một folder, còn commit thực ra chỉ là hash của folder tổng](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/C%C3%B3%20th%E1%BB%83%20hi%E1%BB%83u%20blob%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20file,%20tree%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20folder,%20c%C3%B2n%20commit%20th%E1%BB%B1c%20ra%20ch%E1%BB%89%20l%C3%A0%20hash%20c%E1%BB%A7a%20folder%20t%E1%BB%95ng.md)
    - [Ref là hệ thống đặt tên các object](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/Ref%20l%C3%A0%20h%E1%BB%87%20th%E1%BB%91ng%20%C4%91%E1%BA%B7t%20t%C3%AAn%20c%C3%A1c%20object.md)
    - [Key là hash của object, value là nội dung object](./Blob,%20tree,%20ref.%20B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git/Key%20l%C3%A0%20hash%20c%E1%BB%A7a%20object,%20value%20l%C3%A0%20n%E1%BB%99i%20dung%20object.md)

- Commit: 
    - [@ là viết tắt của HEAD](./Commit/@%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a%20HEAD.md)
    - [HEAD là commit hiện tại](./Commit/HEAD%20l%C3%A0%20commit%20hi%E1%BB%87n%20t%E1%BA%A1i.md)
    - [Git không biết gì về folder](./Commit/Git%20kh%C3%B4ng%20bi%E1%BA%BFt%20g%C3%AC%20v%E1%BB%81%20folder.md)
    - [git log giúp xem lịch sử các commit](./Commit/git%20log%20gi%C3%BAp%20xem%20l%E1%BB%8Bch%20s%E1%BB%AD%20c%C3%A1c%20commit.md)
    - [git reflog giúp xem lại các ref không có trong lịch sử commit](./Commit/git%20reflog%20gi%C3%BAp%20xem%20l%E1%BA%A1i%20c%C3%A1c%20ref%20kh%C3%B4ng%20c%C3%B3%20trong%20l%E1%BB%8Bch%20s%E1%BB%AD%20commit.md)
    - [stash pop nếu gặp conflict sẽ không pop](./Commit/stash%20pop%20n%E1%BA%BFu%20g%E1%BA%B7p%20conflict%20s%E1%BA%BD%20kh%C3%B4ng%20pop.md)
    - [Thứ ta đang trực tiếp chỉnh sửa mà ta tưởng là dữ liệu của mình thực chất là thứ được vay mượn từ commit](./Commit/Th%E1%BB%A9%20ta%20%C4%91ang%20tr%E1%BB%B1c%20ti%E1%BA%BFp%20ch%E1%BB%89nh%20s%E1%BB%ADa%20m%C3%A0%20ta%20t%C6%B0%E1%BB%9Fng%20l%C3%A0%20d%E1%BB%AF%20li%E1%BB%87u%20c%E1%BB%A7a%20m%C3%ACnh%20th%E1%BB%B1c%20ch%E1%BA%A5t%20l%C3%A0%20th%E1%BB%A9%20%C4%91%C6%B0%E1%BB%A3c%20vay%20m%C6%B0%E1%BB%A3n%20t%E1%BB%AB%20commit.md)
    - [Reset soft dùng để gộp nhiều commit lại với nhau. Reset hard dùng để xoá bỏ những gì đã ghi sau commit được chọn](./Commit/Reset%20soft%20d%C3%B9ng%20%C4%91%E1%BB%83%20g%E1%BB%99p%20nhi%E1%BB%81u%20commit%20l%E1%BA%A1i%20v%E1%BB%9Bi%20nhau.%20Reset%20hard%20d%C3%B9ng%20%C4%91%E1%BB%83%20xo%C3%A1%20b%E1%BB%8F%20nh%E1%BB%AFng%20g%C3%AC%20%C4%91%C3%A3%20ghi%20sau%20commit%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BB%8Dn.md)
    - [~ và dấu mũ là để chỉ các commit trước đó](./Commit/~%20v%C3%A0%20d%E1%BA%A5u%20m%C5%A9%20l%C3%A0%20%C4%91%E1%BB%83%20ch%E1%BB%89%20c%C3%A1c%20commit%20tr%C6%B0%E1%BB%9Bc%20%C4%91%C3%B3.md)
    - [Việc commit giúp ta phá code mà không sợ gì, giống như có đồ bảo hộ rồi thì tha hồ nghịch điện cao thế](./Commit/Vi%E1%BB%87c%20commit%20gi%C3%BAp%20ta%20ph%C3%A1%20code%20m%C3%A0%20kh%C3%B4ng%20s%E1%BB%A3%20g%C3%AC,%20gi%E1%BB%91ng%20nh%C6%B0%20c%C3%B3%20%C4%91%E1%BB%93%20b%E1%BA%A3o%20h%E1%BB%99%20r%E1%BB%93i%20th%C3%AC%20tha%20h%E1%BB%93%20ngh%E1%BB%8Bch%20%C4%91i%E1%BB%87n%20cao%20th%E1%BA%BF.md)

- File: 
    - [diff does not take into account untracked files](./File/diff%20does%20not%20take%20into%20account%20untracked%20files.md)
    - [git diff](./File/git%20diff.md)
    - [git add -A làm cho index giống như ở working directory. git commit -am chỉ áp dụng cho những file đã có sẵn trong index](./File/Stage,%20index,%20cache/git%20add%20-A%20l%C3%A0m%20cho%20index%20gi%E1%BB%91ng%20nh%C6%B0%20%E1%BB%9F%20working%20directory.%20git%20commit%20-am%20ch%E1%BB%89%20%C3%A1p%20d%E1%BB%A5ng%20cho%20nh%E1%BB%AFng%20file%20%C4%91%C3%A3%20c%C3%B3%20s%E1%BA%B5n%20trong%20index.md)
    - [Stage, cache, index là những cái tên khác nhau cho cùng một thứ](./File/Stage,%20index,%20cache/Stage,%20cache,%20index%20l%C3%A0%20nh%E1%BB%AFng%20c%C3%A1i%20t%C3%AAn%20kh%C3%A1c%20nhau%20cho%20c%C3%B9ng%20m%E1%BB%99t%20th%E1%BB%A9.md)
    - [Untracked, staged, unchanged và unstaged là 4 trạng thái chính của một file](./File/Stage,%20index,%20cache/Untracked,%20staged,%20unchanged%20v%C3%A0%20unstaged%20l%C3%A0%204%20tr%E1%BA%A1ng%20th%C3%A1i%20ch%C3%ADnh%20c%E1%BB%A7a%20m%E1%BB%99t%20file.md)
    - [git status giúp xem những file nào đã được vào stage](./File/git%20status%20gi%C3%BAp%20xem%20nh%E1%BB%AFng%20file%20n%C3%A0o%20%C4%91%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20v%C3%A0o%20stage.md)
    - [ls-files chỉ làm việc với index](./File/ls-files%20ch%E1%BB%89%20l%C3%A0m%20vi%E1%BB%87c%20v%E1%BB%9Bi%20index.md)
    - [pathspecs giúp chọn đường dẫn một cách linh hoạt và tinh tế hơn](./File/pathspecs%20gi%C3%BAp%20ch%E1%BB%8Dn%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20m%E1%BB%99t%20c%C3%A1ch%20linh%20ho%E1%BA%A1t%20v%C3%A0%20tinh%20t%E1%BA%BF%20h%C6%A1n.md)

- GitHub: 
    - [Bấm dấu . để mở VS Code web ngay trên GitHub](./GitHub/B%E1%BA%A5m%20d%E1%BA%A5u%20.%20%C4%91%E1%BB%83%20m%E1%BB%9F%20VS%20Code%20web%20ngay%20tr%C3%AAn%20GitHub.md)
    - [Website GitHub giống như để remote control máy của GitHub](./GitHub/Website%20GitHub%20gi%E1%BB%91ng%20nh%C6%B0%20%C4%91%E1%BB%83%20remote%20control%20m%C3%A1y%20c%E1%BB%A7a%20GitHub.md)
    - [Template và fork](./GitHub/Template%20v%C3%A0%20fork.md)
    - [GitHub Page không nhận ra các thư mục có dash phía trước, chỉ đọc được trong docs](./GitHub/GitHub%20Page%20kh%C3%B4ng%20nh%E1%BA%ADn%20ra%20c%C3%A1c%20th%C6%B0%20m%E1%BB%A5c%20c%C3%B3%20dash%20ph%C3%ADa%20tr%C6%B0%E1%BB%9Bc,%20ch%E1%BB%89%20%C4%91%E1%BB%8Dc%20%C4%91%C6%B0%E1%BB%A3c%20trong%20docs.md)

- Repo: 
    - [Khi merge, ours là branch hiện tại. Khi rebase, theirs là branch hiện tại](./Repo/Khi%20merge,%20ours%20l%C3%A0%20branch%20hi%E1%BB%87n%20t%E1%BA%A1i.%20Khi%20rebase,%20theirs%20l%C3%A0%20branch%20hi%E1%BB%87n%20t%E1%BA%A1i.md)
    - [Khi viết tính năng mới nên tạo branch mới](./Repo/Khi%20vi%E1%BA%BFt%20t%C3%ADnh%20n%C4%83ng%20m%E1%BB%9Bi%20n%C3%AAn%20t%E1%BA%A1o%20branch%20m%E1%BB%9Bi.md)
    - [Upstream, origin là những cái tên thường dùng cho remote](./Repo/Upstream,%20origin%20l%C3%A0%20nh%E1%BB%AFng%20c%C3%A1i%20t%C3%AAn%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng%20cho%20remote.md)
    - [pull không lấy file mới về, mà lấy commit mới về](./Repo/pull%20kh%C3%B4ng%20l%E1%BA%A5y%20file%20m%E1%BB%9Bi%20v%E1%BB%81,%20m%C3%A0%20l%E1%BA%A5y%20commit%20m%E1%BB%9Bi%20v%E1%BB%81.md)


[GitHub Skills](https://skills.github.com/)
<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=CPLdltN7wgE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>