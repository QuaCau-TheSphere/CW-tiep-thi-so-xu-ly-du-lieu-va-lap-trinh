---
share: true
created: 2023-10-24T18:26
updated: 2025-03-03T18:48
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
[Mỗi một dòng trong dockerfile sẽ tương ứng với một step khi dựng image](./M%E1%BB%97i%20m%E1%BB%99t%20d%C3%B2ng%20trong%20dockerfile%20s%E1%BA%BD%20t%C6%B0%C6%A1ng%20%E1%BB%A9ng%20v%E1%BB%9Bi%20m%E1%BB%99t%20step%20khi%20d%E1%BB%B1ng%20image.md)
[Container chỉ là một process](./Container%20ch%E1%BB%89%20l%C3%A0%20m%E1%BB%99t%20process.md). [Image là template để chạy container](./Image%20l%C3%A0%20template%20%C4%91%E1%BB%83%20ch%E1%BA%A1y%20container.md) 
