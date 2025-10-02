---
share: true
created: 2024-01-12T14:31
updated: 2025-10-02T14:49
---
JSON là để cho máy viết, không phải cho người viết. Người muốn viết thì dùng YAML sẽ tốt hơn.
- Thuộc tính phải được đóng trong ngoặc kép để:
	- Không dụng phải những reserved word trong JS, 
	- Không phải quan tâm xem "ký tự" là gì khi giải quyết unicode ([Cách máy tính hiểu ký tự khác với cách con người hiểu ký tự. Tốt nhất là nên dùng điểm mã khi nói về ký tự máy tính](../../../../%F0%9F%94%A0K%C3%BD%20t%E1%BB%B1,%20v%C4%83n%20b%E1%BA%A3n,%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/Ti%E1%BA%BFng%20Vi%E1%BB%87t,%20Unicode,%20emoji/L%C3%BD%20thuy%E1%BA%BFt%20Unicode/%C4%90i%E1%BB%83m%20m%C3%A3/C%C3%A1ch%20m%C3%A1y%20t%C3%ADnh%20hi%E1%BB%83u%20k%C3%BD%20t%E1%BB%B1%20kh%C3%A1c%20v%E1%BB%9Bi%20c%C3%A1ch%20con%20ng%C6%B0%E1%BB%9Di%20hi%E1%BB%83u%20k%C3%BD%20t%E1%BB%B1.%20T%E1%BB%91t%20nh%E1%BA%A5t%20l%C3%A0%20n%C3%AAn%20d%C3%B9ng%20%C4%91i%E1%BB%83m%20m%C3%A3%20khi%20n%C3%B3i%20v%E1%BB%81%20k%C3%BD%20t%E1%BB%B1%20m%C3%A1y%20t%C3%ADnh.md). [Tuỳ vào phương thức mã hoá mà mỗi ký tự Unicode sẽ được biểu diễn bởi 1-4 đơn vị mã, 1-2 đơn vị mã, hoặc chỉ một đơn vị mã duy nhất](../../../../%F0%9F%94%A0K%C3%BD%20t%E1%BB%B1,%20v%C4%83n%20b%E1%BA%A3n,%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/Ti%E1%BA%BFng%20Vi%E1%BB%87t,%20Unicode,%20emoji/L%C3%BD%20thuy%E1%BA%BFt%20Unicode/Tu%E1%BB%B3%20v%C3%A0o%20ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20m%C3%A3%20ho%C3%A1%20m%C3%A0%20m%E1%BB%97i%20k%C3%BD%20t%E1%BB%B1%20Unicode%20s%E1%BA%BD%20%C4%91%C6%B0%E1%BB%A3c%20bi%E1%BB%83u%20di%E1%BB%85n%20b%E1%BB%9Fi%201-4%20%C4%91%C6%A1n%20v%E1%BB%8B%20m%C3%A3,%201-2%20%C4%91%C6%A1n%20v%E1%BB%8B%20m%C3%A3,%20ho%E1%BA%B7c%20ch%E1%BB%89%20m%E1%BB%99t%20%C4%91%C6%A1n%20v%E1%BB%8B%20m%C3%A3%20duy%20nh%E1%BA%A5t.md)) 
	- Tương thích hơn với Python, vì Python cũng bắt đóng ngoặc kép tất cả các key
- 
[YAML thì để con người dễ đọc, còn JSON là để máy dễ đọc](../YAML/YAML%20th%C3%AC%20%C4%91%E1%BB%83%20con%20ng%C6%B0%E1%BB%9Di%20d%E1%BB%85%20%C4%91%E1%BB%8Dc,%20c%C3%B2n%20JSON%20l%C3%A0%20%C4%91%E1%BB%83%20m%C3%A1y%20d%E1%BB%85%20%C4%91%E1%BB%8Dc.md)

Nguồn:: <iframe width="560" height="315" src="https://www.youtube.com/embed/-C-JoyNuQJs?si=YbirDd_LCVQWUYNx&t=339" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Nếu muốn dùng comment thì có thể xài tạm:
```json
{"//": "A way to use comments in json"}
```
Còn không thì dùng JSONC