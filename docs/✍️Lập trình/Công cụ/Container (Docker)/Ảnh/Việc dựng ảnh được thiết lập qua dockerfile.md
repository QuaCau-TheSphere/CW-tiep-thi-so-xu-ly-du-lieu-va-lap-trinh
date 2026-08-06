---
share: true
created: 2023-10-24T18:26
updated: 2026-08-06T15:36
---
Nguồn:: <iframe width="560" height="315" src="https://www.youtube.com/embed/gAkwW2tuIqE?si=hvz8xyWfGNlOUCqr" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Ví dụ:
```docker
FROM image_cơ_sở
WORKDIR /app
COPY package.json ./
RUN npm install
COPY ./ .
EXPOSE 80
CMD lệnh_khi_image_được_chạy

```
[Mỗi một dòng trong dockerfile sẽ tương ứng với một bước khi dựng ảnh, cũng là một ảnh tạm](./M%E1%BB%97i%20m%E1%BB%99t%20d%C3%B2ng%20trong%20dockerfile%20s%E1%BA%BD%20t%C6%B0%C6%A1ng%20%E1%BB%A9ng%20v%E1%BB%9Bi%20m%E1%BB%99t%20b%C6%B0%E1%BB%9Bc%20khi%20d%E1%BB%B1ng%20%E1%BA%A3nh,%20c%C5%A9ng%20l%C3%A0%20m%E1%BB%99t%20%E1%BA%A3nh%20t%E1%BA%A1m.md)
[Container chỉ là một tiến trình. Nó không có nhân hệ điều hành, mà lấy ở hệ điều hành gốc luôn](../Container/Container%20ch%E1%BB%89%20l%C3%A0%20m%E1%BB%99t%20ti%E1%BA%BFn%20tr%C3%ACnh.%20N%C3%B3%20kh%C3%B4ng%20c%C3%B3%20nh%C3%A2n%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh,%20m%C3%A0%20l%E1%BA%A5y%20%E1%BB%9F%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh%20g%E1%BB%91c%20lu%C3%B4n.md). [Ảnh là template để chạy container](./%E1%BA%A2nh%20l%C3%A0%20template%20%C4%91%E1%BB%83%20ch%E1%BA%A1y%20container.md) 
