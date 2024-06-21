---
share: true
created: 2023-10-30T14:29
updated: 2024-06-01T12:59
---

|                       | Tạo bài đăng hoặc nơi đăng từ URL                                   | Modal                                                                   | Hàm cho modal tạo mới                             |
| --------------------- | ------------------------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------- |
| Mục đích              | Từ URL nhập vào, tạo thông tin để vào modal để người dùng duyệt lại | Người dùng duyệt lại thông tin trước khi nhập vào KV                    | Nhập thông tin người dùng nhập vào vào KV         |
| Nơi dùng              | CORS proxy                                                          | Modal                                                                   | Handler của modal                                 |
| Đặc điểm              |                                                                     | Những thông tin quan trọng hơn với người dùng. Không phải nested object | Giá trị đều là string. Nếu là mảng thì phải split |
| Các trường/thuộc tính | Tiêu đề, mô tả, tên nền tảng, tên nơi đăng, slug                    |                                                                         |                                                   |
Nguồn:: 