---
share: true
created: 2024-01-27T13:38
updated: 2025-09-30T07:55
title: Git
---
# Học Git
Git thật hữu dụng, nhưng với những người mới tập làm quen với Git thì sẽ thấy ngộp nếu phải nhảy ngay vào giao diện dòng lệnh. Các client cung cấp giao diện đồ hoạ cho Git như [Sourcetree](https://www.sourcetreeapp.com/) hoặc [GitKraken](https://www.gitkraken.com/git-client) tuy đã làm tăng sự thân thiện và trực quan lên rất nhiều, nhưng vẫn chưa thể làm bạn hết bối rối vì chúng vẫn phải trưng ra nhiều nút bấm. Dù sao thì chúng được sinh ra để bạn dùng Git, chứ không phải để dạy bạn dùng Git. 

![Ảnh chụp màn hình Sourcetree](https://wac-cdn.atlassian.com/dam/jcr:580c367b-c240-453d-aa18-c7ced44324f9/hero-mac-screenshot.png?cdnVersion=2683)

Thực sự là có rất nhiều tài liệu hướng dẫn Git, nhưng chúng đều bắt bạn phải đọc. Mà [ta thường không sẵn sàng để đọc một tài liệu khi ta mới thấy nó](https://obsidian.quảcầu.cc/⚡Hiểu%20biết%20sâu/Nghĩ%20về%20việc%20nghĩ/Môi%20trường%20nghĩ,%20nhận%20thức%20tăng%20cường/Đọc%20và%20viết/Ghi%20chú%20thông%20tin/Ta%20thường%20không%20sẵn%20sàng%20để%20đọc%20một%20tài%20liệu%20khi%20ta%20mới%20thấy%20nó?utm_source=Vault+C+Tiếp+thị+số%2C+xử+lý+dữ+liệu+và+lập+trình+(Hiểu+biết+sâu)&utm_medium=Vault&utm_campaign=C1&utm_content=&utm_term=). [Khi đang dành tâm trí cho một công việc nhưng phải tạm hoãn giữa chừng để học một công cụ, ta sẽ không nhức đầu khi đó là công cụ vật lý, nhưng lại nhức đầu khi đó là công cụ số](https://obsidian.quảcầu.cc/⚡Hiểu%20biết%20sâu/Công%20nghệ%20thông%20tin/Kỹ%20thuật%20phần%20mềm/Nhức%20đầu/Khi%20đang%20dành%20tâm%20trí%20cho%20một%20công%20việc%20nhưng%20phải%20tạm%20hoãn%20giữa%20chừng%20để%20học%20một%20công%20cụ,%20ta%20sẽ%20không%20nhức%20đầu%20khi%20đó%20là%20công%20cụ%20vật%20lý,%20nhưng%20lại%20nhức%20đầu%20khi%20đó%20là%20công%20cụ%20số?utm_source=Vault+C+Tiếp+thị+số%2C+xử+lý+dữ+liệu+và+lập+trình+(Hiểu+biết+sâu)&utm_medium=Vault&utm_campaign=C1&utm_content=&utm_term=). Có lẽ xem video đỡ nhức đầu hơn. Trong những video mình đã xem, mình thấy bài thuyết trình [Git For Ages 4 And Up](https://www.youtube.com/watch?v=3m7BgIvC-uQ) là hấp dẫn và dễ hiểu cho người mới bắt đầu hơn cả. Tác giả dùng các món đồ chơi gỗ để minh hoạ duy nhất một điều: [Tất cả những gì Git làm chỉ để làm một việc là điều khiển các đồ thị](./T%E1%BA%A5t%20c%E1%BA%A3%20nh%E1%BB%AFng%20g%C3%AC%20Git%20l%C3%A0m%20ch%E1%BB%89%20%C4%91%E1%BB%83%20l%C3%A0m%20m%E1%BB%99t%20vi%E1%BB%87c%20l%C3%A0%20%C4%91i%E1%BB%81u%20khi%E1%BB%83n%20c%C3%A1c%20%C4%91%E1%BB%93%20th%E1%BB%8B.md). Việc dùng những vật thể trong không gian khiến bạn có thể mường tượng được cách bạn sẽ thao tác với Git **bằng cơ thể** của mình thế nào. Nhớ rằng, [công cụ là sự nối dài của cơ thể](https://obsidian.quảcầu.cc/⚡Hiểu%20biết%20sâu/Nghĩ%20về%20việc%20nghĩ/Môi%20trường%20nghĩ,%20nhận%20thức%20tăng%20cường/Công%20cụ%20nghĩ/Công%20cụ%20là%20sự%20nối%20dài%20của%20cơ%20thể?utm_source=Vault+C+Tiếp+thị+số%2C+xử+lý+dữ+liệu+và+lập+trình+(Hiểu+biết+sâu)&utm_medium=Vault&utm_campaign=C1&utm_content=&utm_term=), không phải của não. 

![Linux.conf.au 2013 -- Canberra, Australia - Git For Ages 4 And Up [3m7BgIvC-uQ - 963x722 - 21m44s].png](../../../attachments/Linux.conf.au%202013%20--%20Canberra,%20Australia%20-%20Git%20For%20Ages%204%20And%20Up%203m7BgIvC-uQ%20-%20963x722%20-%2021m44s.md)

## Các trò chơi giúp học Git
| Trò chơi                                                      | Mô tả                                                                                         |
| ------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| [Oh My Git!](https://ohmygit.org/)                            | Cài trực tiếp trên máy. Học các lệnh bằng việc kéo thả các thẻ bài                            |
| [GitByBit](https://gitbybit.com/)                             | Cài trên VS Code, có câu chuyện mở đầu hấp dẫn                                                |
| [Git Branching](https://pcottle.github.io/learnGitBranching/) | Chạy trực tiếp trên web, không cần cài đặt                                                    |
| [git gud](https://github.com/benthayer/git-gud)               | Giống Git Branching nhưng chạy trực tiếp trên terminal. Phải cài Python trước                 |
| [githug](https://github.com/Gazler/githug)                    | Giống git gud nhưng cần cài Ruby                                                              |
| [git-sim](https://initialcommit.com/blog/git-sim)             | Tạo ảnh, video giải thích cách Git vận hành trên dự án thực tế của bạn. Phải cài Python trước |
| [Devlands](https://devlands.com/)                             | Tạo một vùng đất Minecraft cho dự án thực tế của bạn. Chưa ra mắt                             |

## Kinh nghiệm tra cứu
Qua giai đoạn cơ bản thì bạn đã xử lý được gần như là tất cả các trường hợp rồi. Nhưng phần còn lại phải tự học. Một số kinh nghiệm
- Đọc phần Discussion và Examples trên tài liệu hướng dẫn chính thức sẽ đỡ rối hơn 
- Nên học thêm về bên trong git, sẽ đỡ bị cảm giác phải lần mò những thứ lắt nhắt hơn. Các thông báo của Git cũng liên quan nhiều đến blob, tree. [The Law of Leaky Abstractions – Joel on Software](https://www.joelonsoftware.com/2002/11/11/the-law-of-leaky-abstractions/)

Các tài liệu:
- [NDP Software :: Git Cheatsheet](https://ndpsoftware.com/git-cheatsheet.html#loc=workspace;)
  ![Pasted image 20250501164322.png](../../../attachments/Pasted%20image%2020250501164322.png)
- [Git Help Desk](https://jhcarl0814.github.io/ClosedAI/git/git.html)

Khi bạn đã thành thạo Git rồi, bạn có thể xem thêm [danh sách awesome Git này](https://github.com/dictcp/awesome-git?tab=readme-ov-file) này

## Một số hiểu biết hữu ích
- Nhiều người hay nhầm lẫn GitHub với Git là một. Thực ra chúng khác nhau. Các repo Git chỉ được lưu trên máy của bạn, còn các repo GitHub thì được lưu trên server của GitHub.  Chẳng qua là GitHub cung cấp những cách thức để bạn điều khiển cái repo được lưu trên máy của họ, **như thể bạn đang ngồi ở ngay công ty của họ để làm việc**. [Việc bạn truy cập vào website của GitHub cũng giống như là bạn đang teamview máy họ vậy.](../GitHub/Website%20GitHub%20gi%E1%BB%91ng%20nh%C6%B0%20l%C3%A0%20%C4%91%E1%BB%83%20teamview%20m%C3%A1y%20t%C3%ADnh%20c%E1%BB%A7a%20GitHub.md)
- Các commit trong Git được nối lại với nhau bằng các mã hash. Chính vì vậy nên [Có thể xem Git là một dạng xích khối](./C%C3%B3%20th%E1%BB%83%20xem%20Git%20l%C3%A0%20m%E1%BB%99t%20d%E1%BA%A1ng%20x%C3%ADch%20kh%E1%BB%91i.md) (blockchain). Sự khác biệt nằm ở chỗ các xích khối trong tiền mã hoá được thiết kế để chúng ta có thể tin tưởng lẫn nhau, nên chúng có sẵn thuật toán đồng thuận trong đó. Nếu bạn chỉ dùng một mình thì Git với xích khối không khác gì nhau.
- [Trong Git có hai loại lệnh: lệnh sứ (porcelain) và lệnh ống nước (plumbing).](./Blob,%20tree,%20ref.%20B%C3%AAn%20trong%20Git/L%E1%BB%87nh%20s%E1%BB%A9%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20d%C3%A0nh%20cho%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng.%20L%E1%BB%87nh%20%E1%BB%91ng%20n%C6%B0%E1%BB%9Bc%20l%C3%A0%20c%C3%A1c%20l%E1%BB%87nh%20l%C3%B5i%20%C4%91%E1%BB%83%20d%C3%B9ng%20k%C3%A8m%20v%E1%BB%9Bi%20c%C3%A1c%20l%E1%BB%87nh%20Unix%20kh%C3%A1c.md) Để hiểu được ý nghĩa của chúng, cần quay lại lý do Git được tạo ra: [giải quyết nhu cầu của Linus, một người viết nhân hệ điều hành](./Git%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20%C4%91%E1%BB%83%20gi%E1%BA%A3i%20quy%E1%BA%BFt%20nhu%20c%E1%BA%A7u%20c%E1%BB%A7a%20Linus,%20m%E1%BB%99t%20ng%C6%B0%E1%BB%9Di%20vi%E1%BA%BFt%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh.md). Hệ điều hành mà ông này viết, Linux, có triết lý là [các chương trình cần được thiết kế sao cho nó làm tốt duy nhất một nhiệm vụ, và làm tốt việc làm cùng nhau](../../../%F0%9F%A4%96%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn,%20ti%E1%BA%BFn%20tr%C3%ACnh,%20terminal,%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh/Unix,%20Linux/C%C3%A1c%20ch%C6%B0%C6%A1ng%20tr%C3%ACnh%20tr%C3%AAn%20Linux%20h%C6%B0%E1%BB%9Bng%20%C4%91%E1%BA%BFn%20vi%E1%BB%87c%20l%C3%A0m%20t%E1%BB%91t%20%C4%91%C3%BAng%20m%E1%BB%99t%20nhi%E1%BB%87m%20v%E1%BB%A5%20duy%20nh%E1%BA%A5t,%20v%C3%A0%20l%C3%A0m%20t%E1%BB%91t%20vi%E1%BB%87c%20l%C3%A0m%20c%C3%B9ng%20nhau.md). Kết quả của việc này là người dùng Linux thường hay nối các lệnh lại với nhau để dữ liệu được chảy từ chương trình này sang chương trình kia, và kỹ thuật này được gọi là nối ống nước (pipe). Tức là các lệnh ống nước của Git là các lệnh thường hay được dùng để nối với các lệnh Linux khác. Mà mấy cái ống nước này thường bị chôn sâu trong tường, việc thay thế chúng là khó khăn. Tức là cho dù Git có nâng cấp phiên bản gì đi nữa thì các lệnh ống nước cũng sẽ không bị thay đổi, và lập trình viên có thể yên tâm nâng cấp Git mà script họ viết không cần phải cập nhật lại. Còn mấy cái đồ sứ như bồn cầu, bồn rửa mặt thì dễ dùng và dễ thay đổi, nên nó để dành cho người dùng sử dụng. 

[Discord](https://discord.gg/GRFVkzgxRd)

## Các ghi chú khác



[GitHub - GitAlias/gitalias: Git alias commands for faster easier version control](https://github.com/GitAlias/gitalias)
<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=CPLdltN7wgE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

