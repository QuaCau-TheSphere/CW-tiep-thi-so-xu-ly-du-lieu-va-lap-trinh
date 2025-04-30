---
share: true
created: 2024-01-05T14:38
updated: 2025-03-03T18:48
---
Lý do:: [Đường dẫn đến tệp ngoài trong một script phụ thuộc vào cwd, không phải đường dẫn tới script mình đang viết](./%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20%C4%91%E1%BA%BFn%20t%E1%BB%87p%20ngo%C3%A0i%20trong%20m%E1%BB%99t%20script%20ph%E1%BB%A5%20thu%E1%BB%99c%20v%C3%A0o%20cwd,%20kh%C3%B4ng%20ph%E1%BA%A3i%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20t%E1%BB%9Bi%20script%20m%C3%ACnh%20%C4%91ang%20vi%E1%BA%BFt.md)
```ts
import * as path from "$std/path/mod.ts";
const thưMụcHiệnTại = path.dirname(path.fromFileUrl(import.meta.url))
const danhSáchNơiĐăng = Deno.readTextFileSync(thưMụcHiệnTại+'/Nơi đăng.yaml')
```