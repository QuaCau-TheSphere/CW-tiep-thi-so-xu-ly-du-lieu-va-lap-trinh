---
share: True
---
Nguồn:: [Viblo](../../%E2%9A%A1Hi%E1%BB%83u%20bi%E1%BA%BFt%20s%C3%A2u/%CE%9E%20Ngu%E1%BB%93n/Viblo.md#), [Vì sao lại có image `<none>` sau khi build docker?](https://viblo.asia/p/vi-sao-lai-co-image-none-sau-khi-build-docker-L4x5xvBgZBM)

Nếu muốn xoá luôn chúng lúc dựng thì dùng `docker build --rm`. Để xoá hết thì dùng:
```
docker rmi $(docker images -f “dangling=true” -q)
```