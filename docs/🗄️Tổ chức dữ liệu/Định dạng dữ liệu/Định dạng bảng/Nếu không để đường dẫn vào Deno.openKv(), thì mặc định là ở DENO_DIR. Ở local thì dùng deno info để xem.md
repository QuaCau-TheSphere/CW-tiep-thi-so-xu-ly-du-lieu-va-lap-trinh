---
share: true
updated: 2026-08-03T16:02
created: 2026-08-03T15:42
---
Khái niệm:: 
When no path is provided, the database will be opened in a default path for the current script. This location is persistent across script runs and is keyed on the origin storage key (the same key that is used to determine `localStorage` persistence). More information about the origin storage key can be found in the Deno Manual.

Nguồn:: [Cloud - Deno documentation \| Deno Docs](https://docs.deno.com/api/deno/cloud/#Deno.openKv)

[Dùng Array.fromAsync để việc lấy dữ liệu từ KV không phải chờ tải về hết rồi mới bắt đầu lọc](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20b%E1%BA%ADc%20cao/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20(runtime)/Deno/D%C3%B9ng%20Array.fromAsync%20%C4%91%E1%BB%83%20vi%E1%BB%87c%20l%E1%BA%A5y%20d%E1%BB%AF%20li%E1%BB%87u%20t%E1%BB%AB%20KV%20kh%C3%B4ng%20ph%E1%BA%A3i%20ch%E1%BB%9D%20t%E1%BA%A3i%20v%E1%BB%81%20h%E1%BA%BFt%20r%E1%BB%93i%20m%E1%BB%9Bi%20b%E1%BA%AFt%20%C4%91%E1%BA%A7u%20l%E1%BB%8Dc.md)