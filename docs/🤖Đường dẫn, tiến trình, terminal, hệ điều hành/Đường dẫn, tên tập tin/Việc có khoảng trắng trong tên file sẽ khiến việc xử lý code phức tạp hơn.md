---
share: true
created: 2023-09-12T13:33
updated: 2025-10-02T14:01
---
Điều này dễ thấy nhất khi tên file có ở trong biến. Ví dụ, thay vì có thể viết `foo $filename`, ta phải viết `foo "$filename"`. Vì nhỡ `$filename` có khoảng trắng thì 

Khi viết code thì tốt nhất dùng dạng raw. Ví dụ:
```js
const cmd = new Deno.Command("deno", { args: ["run", "--allow-all", "--allow-run", String.raw`${filename}`, câuNhập, '--json-debug'] });
```

Trong việc xử lý URL, dấu cách sẽ được chuyển sang `%20`. Nếu sau dấu cách có ký tự số thì sẽ dễ gây hiểu lầm: `ảnh 1.jpg` → `ảnh%201.jpg`.

Nếu code HTTP không xử lý tốt thì khi người dùng tải `Danh sách.pdf` thì thứ họ nhận được là file `Danh`. Họ phải thêm đuôi `.pdf` thủ công.

Docker và Git bắt phải dùng ký tự ASCII và không có khoảng trắng

[Tên mô đun Python sẽ được dùng làm identifier. Identifier không được có dấu cách](../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/Python/Path,%20env,%20version/T%C3%AAn%20m%C3%B4%20%C4%91un%20Python%20s%E1%BA%BD%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20l%C3%A0m%20identifier.%20Identifier%20kh%C3%B4ng%20%C4%91%C6%B0%E1%BB%A3c%20c%C3%B3%20d%E1%BA%A5u%20c%C3%A1ch.md)

