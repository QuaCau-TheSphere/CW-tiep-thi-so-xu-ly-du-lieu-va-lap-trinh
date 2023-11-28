---
share: true
created: 2023-09-03T00:04
updated: 2023-11-10T13:13
---
Nguồn:: [10 things to avoid in docker containers | Red Hat Developer](https://developers.redhat.com/blog/2016/02/24/10-things-to-avoid-in-docker-containers)
Nếu cần lưu trữ dữ liệu, hãy dùng volume. [Volume là cách để đồng bộ dữ liệu giữa máy chủ và máy ảo](./Volume%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20d%E1%BB%AF%20li%E1%BB%87u%20gi%E1%BB%AFa%20m%C3%A1y%20ch%E1%BB%A7%20v%C3%A0%20m%C3%A1y%20%E1%BA%A3o.md)

Để tự động xoá container sau khi nó chạy xong, dùng `--rm` khi tạo từ image. Nếu kết hợp cờ này với `-it` và bash sẽ hữu ích cho việc debug image:
```
docker run --rm -it [IMAGE] bash
```
