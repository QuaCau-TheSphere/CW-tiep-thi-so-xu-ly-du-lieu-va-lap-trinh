---
share: true
created: 2023-10-30T14:29
updated: 2025-10-18T10:14
---
- Nếu quan hệ hàm số của bản mã với bản rõ là phi tuyến thì sẽ khó bị tấn công hơn. Việc tạo **hỗn loạn (confusion)** sẽ giúp giải quyết việc này. Nó được thực hiện bằng **phép thay thế (substitution)**.
- Trong ngôn ngữ hay có những từ lặp lại thường xuyên (VD: `the` trong tiếng Anh). Kẻ tấn công có thể thống kê những mẫu này để dò ra khoá. Việc **khuếch tán (diffusion)** sẽ giúp giải quyết việc này. Nó được thực hiện bằng **phép hoán vị (permutation)**.

Các loại mã dựa trên một chuỗi các phép thay thế và hoán vị này gọi là mạng SP ([Substitution–permutation network - Wikipedia](https://en.wikipedia.org/wiki/Substitution–permutation_network))
![SubstitutionPermutationNetwork-en.svg 1.png](../../attachments/SubstitutionPermutationNetwork-en.svg%201.png)

Trong khi confusion được thực hiện bằng phép thay thế (substitution) thì diffusion được tạo ra bằng các phép chuyển đổi chỗ (tranposition) hay hoán vị.

Tham khảo:: [users.soict.hust.edu.vn/vannk/AntoanThongtin/MatMaKhoi-KhoaDX.pdf](https://users.soict.hust.edu.vn/vannk/AntoanThongtin/MatMaKhoi-KhoaDX.pdf)
[Véc tơ khởi tạo (iv) dùng để đảm bảo những bản rõ giống nhau không tạo ra bản mã giống nhau](./V%C3%A9c%20t%C6%A1%20kh%E1%BB%9Fi%20t%E1%BA%A1o%20(iv)%20d%C3%B9ng%20%C4%91%E1%BB%83%20%C4%91%E1%BA%A3m%20b%E1%BA%A3o%20nh%E1%BB%AFng%20b%E1%BA%A3n%20r%C3%B5%20gi%E1%BB%91ng%20nhau%20kh%C3%B4ng%20t%E1%BA%A1o%20ra%20b%E1%BA%A3n%20m%C3%A3%20gi%E1%BB%91ng%20nhau.md)