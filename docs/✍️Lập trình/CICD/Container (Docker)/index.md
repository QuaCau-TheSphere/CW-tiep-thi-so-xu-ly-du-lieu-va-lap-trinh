---
share: true
created: 2023-11-10T13:13
updated: 2026-08-04T16:07
title: Container (Docker)
---
[Hướng dẫn Docker & Compose - YouTube](https://www.youtube.com/playlist?list=PLAunJn2-NeUlnatQTkog-zO92eYOpcxx0)

Tiếng Pháp, phụ đề tiếng Anh: [Understanding Docker in a visual way - YouTube](https://www.youtube.com/playlist?list=PLmw3X80dPdlyRV2EUKnFOvBACs_tcArd0)

[Docker guides \| Docker Docs](https://docs.docker.com/guides/)

- \-: 
    - [Docker không dạy bạn cách network hoạt động. Nó chỉ giúp bạn trốn tránh việc phải hiểu nó](./Docker%20kh%C3%B4ng%20d%E1%BA%A1y%20b%E1%BA%A1n%20c%C3%A1ch%20network%20ho%E1%BA%A1t%20%C4%91%E1%BB%99ng.%20N%C3%B3%20ch%E1%BB%89%20gi%C3%BAp%20b%E1%BA%A1n%20tr%E1%BB%91n%20tr%C3%A1nh%20vi%E1%BB%87c%20ph%E1%BA%A3i%20hi%E1%BB%83u%20n%C3%B3.md)
    - [Nếu nhân hệ điều hành trong container khác với nhân hệ điều hành dùng để chạy Docker, thì phải chạy trên máy ảo](./N%E1%BA%BFu%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh%20trong%20container%20kh%C3%A1c%20v%E1%BB%9Bi%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh%20d%C3%B9ng%20%C4%91%E1%BB%83%20ch%E1%BA%A1y%20Docker,%20th%C3%AC%20ph%E1%BA%A3i%20ch%E1%BA%A1y%20tr%C3%AAn%20m%C3%A1y%20%E1%BA%A3o.md)
    - [Volume là cách để đồng bộ dữ liệu giữa máy chủ và máy ảo](./Volume%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20d%E1%BB%AF%20li%E1%BB%87u%20gi%E1%BB%AFa%20m%C3%A1y%20ch%E1%BB%A7%20v%C3%A0%20m%C3%A1y%20%E1%BA%A3o.md)

- Ảnh: 
    - [Lớp là một ảnh tạm được sinh ra từ mỗi dòng trong dockerfile](./%E1%BA%A2nh/L%E1%BB%9Bp%20l%C3%A0%20m%E1%BB%99t%20%E1%BA%A3nh%20t%E1%BA%A1m%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20t%E1%BB%AB%20m%E1%BB%97i%20d%C3%B2ng%20trong%20dockerfile.md)
    - [Mỗi một dòng trong dockerfile sẽ tương ứng với một bước khi dựng ảnh, cũng là một ảnh tạm](./%E1%BA%A2nh/M%E1%BB%97i%20m%E1%BB%99t%20d%C3%B2ng%20trong%20dockerfile%20s%E1%BA%BD%20t%C6%B0%C6%A1ng%20%E1%BB%A9ng%20v%E1%BB%9Bi%20m%E1%BB%99t%20b%C6%B0%E1%BB%9Bc%20khi%20d%E1%BB%B1ng%20%E1%BA%A3nh,%20c%C5%A9ng%20l%C3%A0%20m%E1%BB%99t%20%E1%BA%A3nh%20t%E1%BA%A1m.md)
    - [Nếu cần xóa các tệp tạm được tạo ra từ một lệnh khác thì dùng trong một lệnh RUN, đừng tách thành hai lệnh](./%E1%BA%A2nh/N%E1%BA%BFu%20c%E1%BA%A7n%20x%C3%B3a%20c%C3%A1c%20t%E1%BB%87p%20t%E1%BA%A1m%20%C4%91%C6%B0%E1%BB%A3c%20t%E1%BA%A1o%20ra%20t%E1%BB%AB%20m%E1%BB%99t%20l%E1%BB%87nh%20kh%C3%A1c%20th%C3%AC%20d%C3%B9ng%20trong%20m%E1%BB%99t%20l%E1%BB%87nh%20RUN,%20%C4%91%E1%BB%ABng%20t%C3%A1ch%20th%C3%A0nh%20hai%20l%E1%BB%87nh.md)
    - [Nếu dựng lại ảnh mà đánh tag giống nhau thì ảnh cũ sẽ thành ảnh treo (dangling image)](./%E1%BA%A2nh/N%E1%BA%BFu%20d%E1%BB%B1ng%20l%E1%BA%A1i%20%E1%BA%A3nh%20m%C3%A0%20%C4%91%C3%A1nh%20tag%20gi%E1%BB%91ng%20nhau%20th%C3%AC%20%E1%BA%A3nh%20c%C5%A9%20s%E1%BA%BD%20th%C3%A0nh%20%E1%BA%A3nh%20treo%20(dangling%20image).md)
    - [Việc dựng ảnh được thiết lập qua dockerfile](./%E1%BA%A2nh/Vi%E1%BB%87c%20d%E1%BB%B1ng%20%E1%BA%A3nh%20%C4%91%C6%B0%E1%BB%A3c%20thi%E1%BA%BFt%20l%E1%BA%ADp%20qua%20dockerfile.md)
    - [Ảnh là template để chạy container](./%E1%BA%A2nh/%E1%BA%A2nh%20l%C3%A0%20template%20%C4%91%E1%BB%83%20ch%E1%BA%A1y%20container.md)

- Container: 
    - [Bản chất của việc tắt container là tắt tiến trình PID 1](./Container/B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20vi%E1%BB%87c%20t%E1%BA%AFt%20container%20l%C3%A0%20t%E1%BA%AFt%20ti%E1%BA%BFn%20tr%C3%ACnh%20PID%201.md)
    - [Container là phù du](./Container/Container%20l%C3%A0%20ph%C3%B9%20du.md)
    - [Container chỉ là một tiến trình. Nó không có nhân hệ điều hành, mà lấy ở hệ điều hành gốc luôn](./Container/Container%20ch%E1%BB%89%20l%C3%A0%20m%E1%BB%99t%20ti%E1%BA%BFn%20tr%C3%ACnh.%20N%C3%B3%20kh%C3%B4ng%20c%C3%B3%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh,%20m%C3%A0%20l%E1%BA%A5y%20%E1%BB%9F%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh%20g%E1%BB%91c%20lu%C3%B4n.md)
    - [Docker mặc định sinh ra IP ngẫu nhiên cho container. Không có DNS hoặc static IP management thì service không thể biết nhau](./Container/Docker%20m%E1%BA%B7c%20%C4%91%E1%BB%8Bnh%20sinh%20ra%20IP%20ng%E1%BA%ABu%20nhi%C3%AAn%20cho%20container.%20Kh%C3%B4ng%20c%C3%B3%20DNS%20ho%E1%BA%B7c%20static%20IP%20management%20th%C3%AC%20service%20kh%C3%B4ng%20th%E1%BB%83%20bi%E1%BA%BFt%20nhau.md)
    - [exec để chạy lệnh cho một container đang chạy](./Container/exec%20%C4%91%E1%BB%83%20ch%E1%BA%A1y%20l%E1%BB%87nh%20cho%20m%E1%BB%99t%20container%20%C4%91ang%20ch%E1%BA%A1y.md)
    - [Mặc định là container sẽ chạy bằng quyền root. Dùng USER để chỉ định người dùng](./Container/M%E1%BA%B7c%20%C4%91%E1%BB%8Bnh%20l%C3%A0%20container%20s%E1%BA%BD%20ch%E1%BA%A1y%20b%E1%BA%B1ng%20quy%E1%BB%81n%20root.%20D%C3%B9ng%20USER%20%C4%91%E1%BB%83%20ch%E1%BB%89%20%C4%91%E1%BB%8Bnh%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng.md)

- Động cơ: 
    - [CLI client lúc thì được nói là nằm trong động cơ, lúc thì được nói là nằm ngoài](./%C4%90%E1%BB%99ng%20c%C6%A1/CLI%20client%20l%C3%BAc%20th%C3%AC%20%C4%91%C6%B0%E1%BB%A3c%20n%C3%B3i%20l%C3%A0%20n%E1%BA%B1m%20trong%20%C4%91%E1%BB%99ng%20c%C6%A1,%20l%C3%BAc%20th%C3%AC%20%C4%91%C6%B0%E1%BB%A3c%20n%C3%B3i%20l%C3%A0%20n%E1%BA%B1m%20ngo%C3%A0i.md)
    - [Docker Desktop tạo ra một máy ảo để chạy động cơ docker. Trên Windows thì WSL chính là máy ảo đó](./%C4%90%E1%BB%99ng%20c%C6%A1/Docker%20Desktop%20t%E1%BA%A1o%20ra%20m%E1%BB%99t%20m%C3%A1y%20%E1%BA%A3o%20%C4%91%E1%BB%83%20ch%E1%BA%A1y%20%C4%91%E1%BB%99ng%20c%C6%A1%20docker.%20Tr%C3%AAn%20Windows%20th%C3%AC%20WSL%20ch%C3%ADnh%20l%C3%A0%20m%C3%A1y%20%E1%BA%A3o%20%C4%91%C3%B3.md)
    - [Trong trường hợp của Docker Desktop, CLI client nằm ở máy host, còn daemon nằm ở máy ảo](./%C4%90%E1%BB%99ng%20c%C6%A1/Trong%20tr%C6%B0%E1%BB%9Dng%20h%E1%BB%A3p%20c%E1%BB%A7a%20Docker%20Desktop,%20CLI%20client%20n%E1%BA%B1m%20%E1%BB%9F%20m%C3%A1y%20host,%20c%C3%B2n%20daemon%20n%E1%BA%B1m%20%E1%BB%9F%20m%C3%A1y%20%E1%BA%A3o.md)
    - [Động cơ bao gồm CLI client, API và daemon](./%C4%90%E1%BB%99ng%20c%C6%A1/%C4%90%E1%BB%99ng%20c%C6%A1%20bao%20g%E1%BB%93m%20CLI%20client,%20API%20v%C3%A0%20daemon.md)
    - [Có vẻ như ban đầu động cơ Docker được hiểu là chính là daemon](./%C4%90%E1%BB%99ng%20c%C6%A1/C%C3%B3%20v%E1%BA%BB%20nh%C6%B0%20ban%20%C4%91%E1%BA%A7u%20%C4%91%E1%BB%99ng%20c%C6%A1%20Docker%20%C4%91%C6%B0%E1%BB%A3c%20hi%E1%BB%83u%20l%C3%A0%20ch%C3%ADnh%20l%C3%A0%20daemon.md)



[Hết dung lượng disk do chạy Docker trong thời gian dài](https://viblo.asia/p/het-dung-luong-disk-do-chay-docker-trong-thoi-gian-dai-oK9Vyze94QR#comment-bXP4WgPr47G)

