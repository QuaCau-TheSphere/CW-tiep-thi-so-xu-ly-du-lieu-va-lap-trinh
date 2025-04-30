---
share: true
created: 2024-01-27T13:38
updated: 2025-04-30T22:26
title: Git
---
Git thật hữu dụng, nhưng với những người mới tập làm quen với Git thì sẽ thấy ngộp nếu phải nhảy ngay vào giao diện dòng lệnh. Bạn có thể dùng các chương trình giao diện đồ hoạ như SourceTree hoặc GitKraken, nhưng tuy chúng cũng đã có một bước tiến lớn về sự thân thiện, bạn vẫn có thể vẫn còn bối rối khi vẫn còn quá nhiều nút bấm, và cũng rốt cuộc không biết rốt cuộc nó hoạt động như thế nào.

Có rất nhiều tài liệu hướng dẫn Git, nhưng trong những tài liệu mình đã xem, mình thấy bài thuyết trình [Git For Ages 4 And Up](https://www.youtube.com/watch?v=3m7BgIvC-uQ) là hấp dẫn và dễ hiểu cho người mới bắt đầu hơn cả. Tác giả dùng các món đồ chơi gỗ để minh hoạ duy nhất một điều: [Tất cả những gì Git làm chỉ để làm một việc là điều khiển các đồ thị](./T%E1%BA%A5t%20c%E1%BA%A3%20nh%E1%BB%AFng%20g%C3%AC%20Git%20l%C3%A0m%20ch%E1%BB%89%20%C4%91%E1%BB%83%20l%C3%A0m%20m%E1%BB%99t%20vi%E1%BB%87c%20l%C3%A0%20%C4%91i%E1%BB%81u%20khi%E1%BB%83n%20c%C3%A1c%20%C4%91%E1%BB%93%20th%E1%BB%8B.md). Xem xong chắc là đủ để bạn bớt bối rối khi dùng các chương trình giao diện đồ hoạ trên. Nếu bạn muốn học tiếp cách dùng ở giao diện dòng lệnh, trang [Learn Git Branching](https://learngitbranching.js.org/) sẽ cho bạn các giải thích sinh động.

![Linux.conf.au 2013 -- Canberra, Australia - Git For Ages 4 And Up [3m7BgIvC-uQ - 963x722 - 21m44s].png](../../../attachments/Linux.conf.au%202013%20--%20Canberra,%20Australia%20-%20Git%20For%20Ages%204%20And%20Up%203m7BgIvC-uQ%20-%20963x722%20-%2021m44s.md)

Đây là một số ý mà mình nghĩ sẽ giúp bạn xây dựng được mental model về Git:
- Nhiều người hay nhầm lẫn GitHub với Git là một. Thực ra chúng khác nhau. Các repo Git chỉ được lưu trên máy của bạn, còn các repo GitHub thì được lưu trên server của GitHub.  Chẳng qua là GitHub cung cấp những cách thức để bạn điều khiển cái repo được lưu trên máy của họ, **như thể bạn đang ngồi ở ngay công ty của họ để làm việc**. [Việc bạn truy cập vào website của GitHub cũng giống như là bạn đang teamview máy họ vậy.](./GitHub/Website%20GitHub%20gi%E1%BB%91ng%20nh%C6%B0%20l%C3%A0%20%C4%91%E1%BB%83%20teamview%20m%C3%A1y%20t%C3%ADnh%20c%E1%BB%A7a%20GitHub.md)
- Các commit trong Git được nối lại với nhau bằng các mã hash. Chính vì vậy nên [có thể xem Git là một dạng xích khối](./C%C3%B3%20th%E1%BB%83%20xem%20Git%20l%C3%A0%20m%E1%BB%99t%20d%E1%BA%A1ng%20x%C3%ADch%20kh%E1%BB%91i.md) (blockchain). Sự khác biệt nằm ở chỗ các xích khối trong tiền mã hoá được thiết kế để chúng ta có thể tin tưởng lẫn nhau, nên chúng có sẵn thuật toán đồng thuận trong đó. Nếu bạn chỉ dùng một mình thì Git với xích khối không khác gì nhau.
- [Trong Git có hai loại lệnh: lệnh sứ (porcelain) và lệnh ống nước (plumbing).](./Blob,%20tree,%20ref.%20Git%20internals/L%E1%BB%87nh%20s%E1%BB%A9%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20d%C3%A0nh%20cho%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng.%20L%E1%BB%87nh%20%E1%BB%91ng%20n%C6%B0%E1%BB%9Bc%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20l%C3%B5i%20%C4%91%E1%BB%83%20d%C3%B9ng%20k%C3%A8m%20v%E1%BB%9Bi%20c%C3%A1c%20l%E1%BB%87nh%20Unix%20kh%C3%A1c.md) Cần biết rằng, [Git được sinh ra để giải quyết nhu cầu của Linus, một người viết nhân hệ điều hành](./Git%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20%C4%91%E1%BB%83%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20nhu%20c%E1%BA%A7u%20c%E1%BB%A7a%20Linus,%20m%E1%BB%99t%20ng%C6%B0%E1%BB%9Di%20vi%E1%BA%BFt%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh.md). Hệ điều hành mà ông này viết, Linux, có triết lý là [các chương trình cần được thiết kế sao cho nó làm tốt duy nhất một nhiệm vụ, và làm tốt việc làm cùng nhau](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/H%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh,%20path%20v%C3%A0%20terminal/Unix,%20Linux/C%C3%A1c%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh%20tr%C3%AAn%20Linux%20h%C6%B0%E1%BB%9Bng%20%C4%91%E1%BA%BFn%20vi%E1%BB%87c%20l%C3%A0m%20t%E1%BB%91t%20%C4%91%C3%BAng%20m%E1%BB%99t%20nhi%E1%BB%87m%20v%E1%BB%A5%20duy%20nh%E1%BA%A5t,%20v%C3%A0%20l%C3%A0m%20t%E1%BB%91t%20vi%E1%BB%87c%20l%C3%A0m%20c%C3%B9ng%20nhau.md). Kết quả của việc này là người dùng Linux thường hay nối các lệnh lại với nhau, và kỹ thuật này được gọi là nối ống nước (pipe). Tức là các lệnh ống nước của Git là các lệnh thường hay được dùng để nối với các lệnh Linux khác. Mà mấy cái ống nước này thường bị chôn sâu trong tường, việc thay thế chúng là khó khăn. Tức là người dùng có thể tin tưởng là cho dù Git có nâng cấp phiên bản gì đi nữa thì các lệnh ống nước cũng sẽ không bị thay đổi. Còn mấy cái đồ sứ như bồn cầu, bồn rửa mặt thì dễ dùng và dễ thay đổi, nên nó để dành cho người dùng sử dụng. 

Khi bạn đã thành thạo Git rồi, bạn có thể xem thêm [danh sách awesome Git này](https://github.com/dictcp/awesome-git?tab=readme-ov-file) này
[GitHub Skills](https://skills.github.com/)


[Git Help Desk](https://jhcarl0814.github.io/ClosedAI/git/git.html)
[GitHub - initialcommit-com/git-sim: Visually simulate Git operations in your own repos with a single terminal command.](https://github.com/initialcommit-com/git-sim)

[GitHub - GitAlias/gitalias: Git alias commands for faster easier version control](https://github.com/GitAlias/gitalias)
<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=CPLdltN7wgE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- \-: 
    - [2 chấm và 3 chấm trong log và diff](./2%20ch%E1%BA%A5m%20v%C3%A0%203%20ch%E1%BA%A5m%20trong%20log%20v%C3%A0%20diff.md)
    - [Các lệnh Git thường dùng](./C%C3%A1c%20l%E1%BB%87nh%20Git%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)
    - [Các lỗi Git thường gặp](./C%C3%A1c%20l%E1%BB%97i%20Git%20th%C6%B0%E1%BB%9Dng%20g%E1%BA%B7p.md)
    - [Có thể xem Git là một dạng xích khối](./C%C3%B3%20th%E1%BB%83%20xem%20Git%20l%C3%A0%20m%E1%BB%99t%20d%E1%BA%A1ng%20x%C3%ADch%20kh%E1%BB%91i.md)
    - [Facebook chuyển sang Mercurial vì nhóm phát triển Git năm 2012 không mặn mà với monorepo](./Facebook%20chuy%E1%BB%83n%20sang%20Mercurial%20v%C3%AC%20nh%C3%B3m%20ph%C3%A1t%20tri%E1%BB%83n%20Git%20n%C4%83m%202012%20kh%C3%B4ng%20m%E1%BA%B7n%20m%C3%A0%20v%E1%BB%9Bi%20monorepo.md)
    - [Fast forward](./Fast%20forward.md)
    - [Git giúp ta du hành thời gian](./Git%20gi%C3%BAp%20ta%20du%20h%C3%A0nh%20th%E1%BB%9Di%20gian.md)
    - [Git tag](./Git%20tag.md)
    - [Git được sinh ra để giải quyết nhu cầu của Linus, một người viết nhân hệ điều hành](./Git%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20%C4%91%E1%BB%83%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20nhu%20c%E1%BA%A7u%20c%E1%BB%A7a%20Linus,%20m%E1%BB%99t%20ng%C6%B0%E1%BB%9Di%20vi%E1%BA%BFt%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh.md)
    - [Real-time collaboration isn't necessary in most cases, but asynchronous collaboration](./Real-time%20collaboration%20isn't%20necessary%20in%20most%20cases,%20but%20asynchronous%20collaboration.md)
    - [Tất cả những gì Git làm chỉ để làm một việc là điều khiển các đồ thị](./T%E1%BA%A5t%20c%E1%BA%A3%20nh%E1%BB%AFng%20g%C3%AC%20Git%20l%C3%A0m%20ch%E1%BB%89%20%C4%91%E1%BB%83%20l%C3%A0m%20m%E1%BB%99t%20vi%E1%BB%87c%20l%C3%A0%20%C4%91i%E1%BB%81u%20khi%E1%BB%83n%20c%C3%A1c%20%C4%91%E1%BB%93%20th%E1%BB%8B.md)

- Blob, tree, ref. Git internals: 
    - [Blob, tree, commit và annotated tag là các object chính](./Blob,%20tree,%20ref.%20Git%20internals/Blob,%20tree,%20commit%20v%C3%A0%20annotated%20tag%20l%C3%A0%20c%C3%A1c%20object%20ch%C3%ADnh.md)
    - [Bản chất của Git chỉ là những cặp giá trị key – value](./Blob,%20tree,%20ref.%20Git%20internals/B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20Git%20ch%E1%BB%89%20l%C3%A0%20nh%E1%BB%AFng%20c%E1%BA%B7p%20gi%C3%A1%20tr%E1%BB%8B%20key%20%E2%80%93%20value.md)
    - [Commitist và treeist](./Blob,%20tree,%20ref.%20Git%20internals/Commitist%20v%C3%A0%20treeist.md)
    - [Các commit được nối với nhau bằng hash](./Blob,%20tree,%20ref.%20Git%20internals/C%C3%A1c%20commit%20%C4%91%C6%B0%E1%BB%A3c%20n%E1%BB%91i%20v%E1%BB%9Bi%20nhau%20b%E1%BA%B1ng%20hash.md)
    - [Có thể hiểu blob là hash của một tệp, tree là hash của một thư mục, còn commit thực ra chỉ là hash của cả thư mục tổng](./Blob,%20tree,%20ref.%20Git%20internals/C%C3%B3%20th%E1%BB%83%20hi%E1%BB%83u%20blob%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20t%E1%BB%87p,%20tree%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20th%C6%B0%20m%E1%BB%A5c,%20c%C3%B2n%20commit%20th%E1%BB%B1c%20ra%20ch%E1%BB%89%20l%C3%A0%20hash%20c%E1%BB%A7a%20c%E1%BA%A3%20th%C6%B0%20m%E1%BB%A5c%20t%E1%BB%95ng.md)
    - [Có thể xem nội dung file với hash là như nhau. Nhưng file thì có thể có kích thước vô cùng lớn, còn hash thì luôn chỉ có 40 ký tự](./Blob,%20tree,%20ref.%20Git%20internals/C%C3%B3%20th%E1%BB%83%20xem%20n%E1%BB%99i%20dung%20file%20v%E1%BB%9Bi%20hash%20l%C3%A0%20nh%C6%B0%20nhau.%20Nh%C6%B0ng%20file%20th%C3%AC%20c%C3%B3%20th%E1%BB%83%20c%C3%B3%20k%C3%ADch%20th%C6%B0%E1%BB%9Bc%20v%C3%B4%20c%C3%B9ng%20l%E1%BB%9Bn,%20c%C3%B2n%20hash%20th%C3%AC%20lu%C3%B4n%20ch%E1%BB%89%20c%C3%B3%2040%20k%C3%BD%20t%E1%BB%B1.md)
    - [Key là hash của object, value là nội dung object](./Blob,%20tree,%20ref.%20Git%20internals/Key%20l%C3%A0%20hash%20c%E1%BB%A7a%20object,%20value%20l%C3%A0%20n%E1%BB%99i%20dung%20object.md)
    - [Lệnh sứ là các lệnh dành cho người dùng. Lệnh ống nước là các lệnh lõi để dùng kèm với các lệnh Unix khác](./Blob,%20tree,%20ref.%20Git%20internals/L%E1%BB%87nh%20s%E1%BB%A9%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20d%C3%A0nh%20cho%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng.%20L%E1%BB%87nh%20%E1%BB%91ng%20n%C6%B0%E1%BB%9Bc%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20l%C3%B5i%20%C4%91%E1%BB%83%20d%C3%B9ng%20k%C3%A8m%20v%E1%BB%9Bi%20c%C3%A1c%20l%E1%BB%87nh%20Unix%20kh%C3%A1c.md)
    - [[🔠Ký tự, văn bản. Quản lý, viết và xuất bản nội dung/Đồng bộ, sao lưu/Git/Blob, tree, ref. Git internals/Ref/Cái nào có ref thì `git gc` sẽ không đụng tới.md|Cái nào có ref thì `git gc` sẽ không đụng tới]]
    - [Có 2 chỗ để lưu ref](./Blob,%20tree,%20ref.%20Git%20internals/Ref/C%C3%B3%202%20ch%E1%BB%97%20%C4%91%E1%BB%83%20l%C6%B0u%20ref.md)
    - [git reflog giúp xem lại các ref không có trong lịch sử commit](./Blob,%20tree,%20ref.%20Git%20internals/Ref/git%20reflog%20gi%C3%BAp%20xem%20l%E1%BA%A1i%20c%C3%A1c%20ref%20kh%C3%B4ng%20c%C3%B3%20trong%20l%E1%BB%8Bch%20s%E1%BB%AD%20commit.md)
    - [git reflog là phao cứu sinh cho những lỗi lầm khi dùng Git](./Blob,%20tree,%20ref.%20Git%20internals/Ref/git%20reflog%20l%C3%A0%20phao%20c%E1%BB%A9u%20sinh%20cho%20nh%E1%BB%AFng%20l%E1%BB%97i%20l%E1%BA%A7m%20khi%20d%C3%B9ng%20Git.md)
    - [Ref là hệ thống đặt tên các object](./Blob,%20tree,%20ref.%20Git%20internals/Ref/Ref%20l%C3%A0%20h%E1%BB%87%20th%E1%BB%91ng%20%C4%91%E1%BA%B7t%20t%C3%AAn%20c%C3%A1c%20object.md)

- Commit: 
    - [@ là viết tắt của HEAD](./Commit/@%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a%20HEAD.md)
    - [Git không biết gì về folder](./Commit/Git%20kh%C3%B4ng%20bi%E1%BA%BFt%20g%C3%AC%20v%E1%BB%81%20folder.md)
    - [git log --all chỉ hiện những commit nào tiếp cận được từ một ref](./Commit/git%20log%20--all%20ch%E1%BB%89%20hi%E1%BB%87n%20nh%E1%BB%AFng%20commit%20n%C3%A0o%20ti%E1%BA%BFp%20c%E1%BA%ADn%20%C4%91%C6%B0%E1%BB%A3c%20t%E1%BB%AB%20m%E1%BB%99t%20ref.md)
    - [git log giúp xem lịch sử các commit](./Commit/git%20log%20gi%C3%BAp%20xem%20l%E1%BB%8Bch%20s%E1%BB%AD%20c%C3%A1c%20commit.md)
    - [HEAD là commit hiện tại](./Commit/HEAD%20l%C3%A0%20commit%20hi%E1%BB%87n%20t%E1%BA%A1i.md)
    - [Khi amend, rebase, push force thì author date vẫn giữ nguyên, còn commit date mới cập nhật](./Commit/Khi%20amend,%20rebase,%20push%20force%20th%C3%AC%20author%20date%20v%E1%BA%ABn%20gi%E1%BB%AF%20nguy%C3%AAn,%20c%C3%B2n%20commit%20date%20m%E1%BB%9Bi%20c%E1%BA%ADp%20nh%E1%BA%ADt.md)
    - [Reset soft dùng để gộp nhiều commit lại với nhau. Reset hard dùng để xoá bỏ những gì đã ghi sau commit được chọn](./Commit/Reset%20soft%20d%C3%B9ng%20%C4%91%E1%BB%83%20g%E1%BB%99p%20nhi%E1%BB%81u%20commit%20l%E1%BA%A1i%20v%E1%BB%9Bi%20nhau.%20Reset%20hard%20d%C3%B9ng%20%C4%91%E1%BB%83%20xo%C3%A1%20b%E1%BB%8F%20nh%E1%BB%AFng%20g%C3%AC%20%C4%91%C3%A3%20ghi%20sau%20commit%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BB%8Dn.md)
    - [stash pop nếu gặp conflict sẽ không pop](./Commit/stash%20pop%20n%E1%BA%BFu%20g%E1%BA%B7p%20conflict%20s%E1%BA%BD%20kh%C3%B4ng%20pop.md)
    - [Thứ ta đang trực tiếp chỉnh sửa mà ta tưởng là dữ liệu của mình thực chất là thứ được vay mượn từ commit](./Commit/Th%E1%BB%A9%20ta%20%C4%91ang%20tr%E1%BB%B1c%20ti%E1%BA%BFp%20ch%E1%BB%89nh%20s%E1%BB%ADa%20m%C3%A0%20ta%20t%C6%B0%E1%BB%9Fng%20l%C3%A0%20d%E1%BB%AF%20li%E1%BB%87u%20c%E1%BB%A7a%20m%C3%ACnh%20th%E1%BB%B1c%20ch%E1%BA%A5t%20l%C3%A0%20th%E1%BB%A9%20%C4%91%C6%B0%E1%BB%A3c%20vay%20m%C6%B0%E1%BB%A3n%20t%E1%BB%AB%20commit.md)
    - [Việc commit giúp ta phá code mà không sợ gì, giống như có đồ bảo hộ rồi thì tha hồ nghịch điện cao thế](./Commit/Vi%E1%BB%87c%20commit%20gi%C3%BAp%20ta%20ph%C3%A1%20code%20m%C3%A0%20kh%C3%B4ng%20s%E1%BB%A3%20g%C3%AC,%20gi%E1%BB%91ng%20nh%C6%B0%20c%C3%B3%20%C4%91%E1%BB%93%20b%E1%BA%A3o%20h%E1%BB%99%20r%E1%BB%93i%20th%C3%AC%20tha%20h%E1%BB%93%20ngh%E1%BB%8Bch%20%C4%91i%E1%BB%87n%20cao%20th%E1%BA%BF.md)
    - [~ và dấu mũ là để chỉ các commit trước đó](./Commit/~%20v%C3%A0%20d%E1%BA%A5u%20m%C5%A9%20l%C3%A0%20%C4%91%E1%BB%83%20ch%E1%BB%89%20c%C3%A1c%20commit%20tr%C6%B0%E1%BB%9Bc%20%C4%91%C3%B3.md)

- File: 
    - [diff does not take into account untracked files](./File/diff/diff%20does%20not%20take%20into%20account%20untracked%20files.md)
    - [git diff chỉ so sánh working tree với index, không phải HEAD. Muốn so sánh với HEAD phải dùng git diff HEAD](./File/diff/git%20diff%20ch%E1%BB%89%20so%20s%C3%A1nh%20working%20tree%20v%E1%BB%9Bi%20index,%20kh%C3%B4ng%20ph%E1%BA%A3i%20HEAD.%20Mu%E1%BB%91n%20so%20s%C3%A1nh%20v%E1%BB%9Bi%20HEAD%20ph%E1%BA%A3i%20d%C3%B9ng%20git%20diff%20HEAD.md)
    - [git diff thường dùng](./File/diff/git%20diff%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng.md)
    - [git status giúp xem những file nào đã được vào stage](./File/git%20status%20gi%C3%BAp%20xem%20nh%E1%BB%AFng%20file%20n%C3%A0o%20%C4%91%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20v%C3%A0o%20stage.md)
    - [ls-files chỉ làm việc với index](./File/ls-files%20ch%E1%BB%89%20l%C3%A0m%20vi%E1%BB%87c%20v%E1%BB%9Bi%20index.md)
    - [pathspecs giúp chọn đường dẫn một cách linh hoạt và tinh tế hơn](./File/pathspecs%20gi%C3%BAp%20ch%E1%BB%8Dn%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20m%E1%BB%99t%20c%C3%A1ch%20linh%20ho%E1%BA%A1t%20v%C3%A0%20tinh%20t%E1%BA%BF%20h%C6%A1n.md)
    - [git add -A làm cho index giống như ở working directory. git commit -am chỉ áp dụng cho những file đã có sẵn trong index](./File/Stage,%20index,%20cache/git%20add%20-A%20l%C3%A0m%20cho%20index%20gi%E1%BB%91ng%20nh%C6%B0%20%E1%BB%9F%20working%20directory.%20git%20commit%20-am%20ch%E1%BB%89%20%C3%A1p%20d%E1%BB%A5ng%20cho%20nh%E1%BB%AFng%20file%20%C4%91%C3%A3%20c%C3%B3%20s%E1%BA%B5n%20trong%20index.md)
    - [Stage, cache, index là những cái tên khác nhau cho cùng một thứ](./File/Stage,%20index,%20cache/Stage,%20cache,%20index%20l%C3%A0%20nh%E1%BB%AFng%20c%C3%A1i%20t%C3%AAn%20kh%C3%A1c%20nhau%20cho%20c%C3%B9ng%20m%E1%BB%99t%20th%E1%BB%A9.md)
    - [Untracked, staged, unchanged và unstaged là 4 trạng thái chính của một file](./File/Stage,%20index,%20cache/Untracked,%20staged,%20unchanged%20v%C3%A0%20unstaged%20l%C3%A0%204%20tr%E1%BA%A1ng%20th%C3%A1i%20ch%C3%ADnh%20c%E1%BB%A7a%20m%E1%BB%99t%20file.md)

- GitHub: 
    - [Bấm dấu . để mở VS Code bản web ngay trên GitHub](./GitHub/B%E1%BA%A5m%20d%E1%BA%A5u%20.%20%C4%91%E1%BB%83%20m%E1%BB%9F%20VS%20Code%20b%E1%BA%A3n%20web%20ngay%20tr%C3%AAn%20GitHub.md)
    - [GitHub Page không nhận ra các thư mục có dash phía trước, chỉ đọc được trong docs](./GitHub/GitHub%20Page%20kh%C3%B4ng%20nh%E1%BA%ADn%20ra%20c%C3%A1c%20th%C6%B0%20m%E1%BB%A5c%20c%C3%B3%20dash%20ph%C3%ADa%20tr%C6%B0%E1%BB%9Bc,%20ch%E1%BB%89%20%C4%91%E1%BB%8Dc%20%C4%91%C6%B0%E1%BB%A3c%20trong%20docs.md)
    - [Template và fork](./GitHub/Template%20v%C3%A0%20fork.md)
    - [Tạo nhánh mới khi tạo PR sẽ dễ quản lý hơn](./GitHub/T%E1%BA%A1o%20nh%C3%A1nh%20m%E1%BB%9Bi%20khi%20t%E1%BA%A1o%20PR%20s%E1%BA%BD%20d%E1%BB%85%20qu%E1%BA%A3n%20l%C3%BD%20h%C6%A1n.md)
    - [Website GitHub giống như là để teamview máy tính của GitHub](./GitHub/Website%20GitHub%20gi%E1%BB%91ng%20nh%C6%B0%20l%C3%A0%20%C4%91%E1%BB%83%20teamview%20m%C3%A1y%20t%C3%ADnh%20c%E1%BB%A7a%20GitHub.md)

- Repo: 
    - [Cây lịch sử có thể được dùng như là bản lưu những gì đã diễn ra, hoặc là một câu chuyện kể về chúng](./Repo/C%C3%A2y%20l%E1%BB%8Bch%20s%E1%BB%AD%20c%C3%B3%20th%E1%BB%83%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20nh%C6%B0%20l%C3%A0%20b%E1%BA%A3n%20l%C6%B0u%20nh%E1%BB%AFng%20g%C3%AC%20%C4%91%C3%A3%20di%E1%BB%85n%20ra,%20ho%E1%BA%B7c%20l%C3%A0%20m%E1%BB%99t%20c%C3%A2u%20chuy%E1%BB%87n%20k%E1%BB%83%20v%E1%BB%81%20ch%C3%BAng.md)
    - [Khi viết tính năng mới nên tạo branch mới](./Repo/Khi%20vi%E1%BA%BFt%20t%C3%ADnh%20n%C4%83ng%20m%E1%BB%9Bi%20n%C3%AAn%20t%E1%BA%A1o%20branch%20m%E1%BB%9Bi.md)
    - [git merge B nên được hiểu là git merge A with B. git rebase A nên được hiểu là git rebase B to A](./Repo/Merge,%20rebase/git%20merge%20B%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20hi%E1%BB%83u%20l%C3%A0%20git%20merge%20A%20with%20B.%20git%20rebase%20A%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20hi%E1%BB%83u%20l%C3%A0%20git%20rebase%20B%20to%20A.md)
    - [Khi merge, ours là branch hiện tại. Khi rebase, theirs là branch hiện tại](./Repo/Merge,%20rebase/Khi%20merge,%20ours%20l%C3%A0%20branch%20hi%E1%BB%87n%20t%E1%BA%A1i.%20Khi%20rebase,%20theirs%20l%C3%A0%20branch%20hi%E1%BB%87n%20t%E1%BA%A1i.md)
    - [Merge dùng để bảo lưu sự song song của các thay đổi đã xảy ra trên code. Rebase dùng để đảm bảo cây lịch sử phản ánh sự tuần tự trong quá trình thay đổi code của mình](./Repo/Merge,%20rebase/Merge%20d%C3%B9ng%20%C4%91%E1%BB%83%20b%E1%BA%A3o%20l%C6%B0u%20s%E1%BB%B1%20song%20song%20c%E1%BB%A7a%20c%C3%A1c%20thay%20%C4%91%E1%BB%95i%20%C4%91%C3%A3%20x%E1%BA%A3y%20ra%20tr%C3%AAn%20code.%20Rebase%20d%C3%B9ng%20%C4%91%E1%BB%83%20%C4%91%E1%BA%A3m%20b%E1%BA%A3o%20c%C3%A2y%20l%E1%BB%8Bch%20s%E1%BB%AD%20ph%E1%BA%A3n%20%C3%A1nh%20s%E1%BB%B1%20tu%E1%BA%A7n%20t%E1%BB%B1%20trong%20qu%C3%A1%20tr%C3%ACnh%20thay%20%C4%91%E1%BB%95i%20code%20c%E1%BB%A7a%20m%C3%ACnh.md)
    - [Rebase thích hợp khi phải merge nhiều branch, do nó làm cây lịch sử gọn hơn](./Repo/Merge,%20rebase/Rebase%20th%C3%ADch%20h%E1%BB%A3p%20khi%20ph%E1%BA%A3i%20merge%20nhi%E1%BB%81u%20branch,%20do%20n%C3%B3%20l%C3%A0m%20c%C3%A2y%20l%E1%BB%8Bch%20s%E1%BB%AD%20g%E1%BB%8Dn%20h%C6%A1n.md)
    - [origin, upstream là những cái tên thường dùng cho remote](./Repo/origin,%20upstream%20l%C3%A0%20nh%E1%BB%AFng%20c%C3%A1i%20t%C3%AAn%20th%C6%B0%E1%BB%9Dng%20d%C3%B9ng%20cho%20remote.md)
    - [pull không lấy file mới về, mà lấy commit mới về](./Repo/pull%20kh%C3%B4ng%20l%E1%BA%A5y%20file%20m%E1%BB%9Bi%20v%E1%BB%81,%20m%C3%A0%20l%E1%BA%A5y%20commit%20m%E1%BB%9Bi%20v%E1%BB%81.md)

