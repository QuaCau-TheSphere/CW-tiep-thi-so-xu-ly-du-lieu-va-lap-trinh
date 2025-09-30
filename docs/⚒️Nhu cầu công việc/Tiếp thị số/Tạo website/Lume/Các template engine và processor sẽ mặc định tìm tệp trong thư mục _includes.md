---
share: true
created: 2023-10-30T14:29
updated: 2025-05-22T23:49
---
[Tất cả các thư mục bắt đầu bằng _ hoặc . mặc định đều bị bỏ ra](./T%E1%BA%A5t%20c%E1%BA%A3%20c%C3%A1c%20th%C6%B0%20m%E1%BB%A5c%20b%E1%BA%AFt%20%C4%91%E1%BA%A7u%20b%E1%BA%B1ng%20_%20ho%E1%BA%B7c%20.%20m%E1%BA%B7c%20%C4%91%E1%BB%8Bnh%20%C4%91%E1%BB%81u%20b%E1%BB%8B%20b%E1%BB%8F%20ra.md). `_includes` cũng không phải là ngoại lệ. Nhưng việc bỏ ra đó chỉ là trong lúc build, chứ những tệp trong đó vẫn có thể được dùng cho plugin, template engine, processor, v.v.

if these assets are exported by their own (not imported by other files), yeah. I'd place them outside this folder. 


`_includes` phải ở trong `src`. ([Tất cả mọi thứ đều phải ở trong src. Tất cả các đường dẫn đều bắt đầu từ src](./T%E1%BA%A5t%20c%E1%BA%A3%20m%E1%BB%8Di%20th%E1%BB%A9%20%C4%91%E1%BB%81u%20ph%E1%BA%A3i%20%E1%BB%9F%20trong%20src.%20T%E1%BA%A5t%20c%E1%BA%A3%20c%C3%A1c%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20%C4%91%E1%BB%81u%20b%E1%BA%AFt%20%C4%91%E1%BA%A7u%20t%E1%BB%AB%20src.md))
Nguồn:: [The \_config file - Lume](https://lume.land/docs/configuration/config-file/#includes)
[Discord](https://discord.com/channels/794537085641818124/1375147431532171366)