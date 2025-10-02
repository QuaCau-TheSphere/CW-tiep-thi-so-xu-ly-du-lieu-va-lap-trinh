---
share: true
created: 2023-10-30T14:31
updated: 2025-10-02T14:25
alias:
  - Môi trường thực thi đối với code cũng giống như nhạc cụ đối với nốt nhạc
  - Động cơ đối với code cũng giống như nhạc công đối với nốt nhạc
  - Nếu xem code giống như các nốt nhạc trên một tờ giấy, thì động cơ giống như nhạc công, còn môi trường thực thi giống như nhạc cụ
  - Nếu xem code giống như các nốt nhạc trên một tờ giấy, thì động cơ giống như nhạc công
  - Nếu xem code giống như các nốt nhạc trên một tờ giấy, thì môi trường thực thi giống như nhạc cụ
---
Nếu như một lập trình viên là một nhạc sĩ, thì cái script họ viết ra chính là cái sheet nhạc. Một bản nhạc được phát ra khi nhạc công nhìn vào văn bản nhạc và thao tác trên nhạc cụ. Tương tự, một chương trình chạy được khi *động cơ* đọc code trong *môi trường thực thi*. Động cơ là thứ có thể đọc và hiểu code, còn môi trường thực thi là toàn bộ những thứ mà động cơ dùng để tương tác với môi trường bên ngoài.

Nếu như đây là code của một chương trình:
![|300](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjW6umUr-rqk6ZG5yrJrofzju5iJL3Uy_X7YQEH7Mx2PfS3kxey6cgIKUVdLVVyDAprlND4sCFc9d5twCihMVYsGv_iN5Eqp-tt2g_Xcvhhlt1PS9tlePGUso4OMNfAVIGgIlIt5wlVOKk/s1600/Croatian+Rhapsody_0001.png)
Thì đây là chương trình đó khi nó có động cơ (nhạc công) và môi trường thực thi (nhạc cụ):
<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=3aTEjyzWKFQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Có nhiều cách thức để ta ký hiệu âm thanh xuống trang giấy, cũng như có nhiều cách thức để lưu một ý tưởng vào ổ đĩa. JavaScript là một cách để lưu ý tưởng, Python là một cách khác. Cái code mà bạn thường nghe nói tới chính là cái cách để bạn ký hiệu những ý tưởng của mình. Chúng chỉ là những ký hiệu, giống như những dòng chữ này. 

Để chạy được những ký hiệu này, chúng cần tới động cơ, thứ có thể đọc và hiểu chúng. Có nhiều loại môi trường thực thi khác nhau cho JavaScript, và đây là những môi trường thực thi bạn thường được nghe đến: Firefox, Chrome, Safari, Opera, Edge, Node, Deno, Electron. Như bạn thấy, 5 cái đầu chính là các trình duyệt chứ chẳng phải là gì xa lạ. Còn Electron chính là cái để viết ra phiên bản desktop cho Obsidian, Notion, Slack, VS Code, Discord, Dropbox, Figma, v.v. Trừ Firefox, Safari và Edge ra, thì tất cả các môi trường thực thi còn lại đều dùng V8, một động cơ do Google viết ra.

Node là một môi trường thực thi cho JavaScript. [Sau một thập kỷ phát triển, tác giả của Node đã viết Deno để khắc phục những thiếu sót của Node](../../../Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20(runtime)/Deno/Sau%20m%E1%BB%99t%20th%E1%BA%ADp%20k%E1%BB%B7%20ph%C3%A1t%20tri%E1%BB%83n,%20t%C3%A1c%20gi%E1%BA%A3%20c%E1%BB%A7a%20Node%20%C4%91%C3%A3%20vi%E1%BA%BFt%20Deno%20%C4%91%E1%BB%83%20kh%E1%BA%AFc%20ph%E1%BB%A5c%20nh%E1%BB%AFng%20thi%E1%BA%BFu%20s%C3%B3t%20c%E1%BB%A7a%20Node.md). Có thể xem bài diễn thuyết [10 điều tôi hối hận về Node.js](https://www.youtube.com/watch?v=M3BM9TB-8yA "10 Things I Regret About Node.js - Ryan Dahl - JSConf EU - YouTube") của tác giả. (Tác giả không giải thích cái tên Deno có nghĩa là gì, nhưng nhiều người đoán nó là viết ngược lại của Node.)

Xem thêm:: [Stack Overflow](../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [What is the difference between JavaScript Engine and JavaScript Runtime Environment - Stack Overflow](https://stackoverflow.com/questions/29027845/what-is-the-difference-between-javascript-engine-and-javascript-runtime-environm)

[Runtime là lúc chạy, runtime environment là môi trường thực thi. Nhưng nhiều lúc runtime environment được gọi tắt là runtime](./Runtime%20l%C3%A0%20l%C3%BAc%20ch%E1%BA%A1y,%20runtime%20environment%20l%C3%A0%20m%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi.%20Nh%C6%B0ng%20nhi%E1%BB%81u%20l%C3%BAc%20runtime%20environment%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20t%E1%BA%AFt%20l%C3%A0%20runtime.md)

## Các động cơ được bàn trong kho này
[Ngôn ngữ và động cơ thường trùng tên](../Ng%C3%B4n%20ng%E1%BB%AF%20v%C3%A0%20%C4%91%E1%BB%99ng%20c%C6%A1%20th%C6%B0%E1%BB%9Dng%20tr%C3%B9ng%20t%C3%AAn.md)

| Ngôn ngữ   | Động cơ       |
| ---------- | ------------- |
| JavaScript | V8, Gecko     |
| Python     | Python        |
| TeX        | TeX           |
| bib        | BibTex, Biber |
