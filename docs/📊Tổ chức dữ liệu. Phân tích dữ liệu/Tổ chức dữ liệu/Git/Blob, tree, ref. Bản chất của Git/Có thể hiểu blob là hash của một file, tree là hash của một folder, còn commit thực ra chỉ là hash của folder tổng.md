---
share: true
created: 2023-10-30T14:29
updated: 2024-07-21T14:01
---
Chính vì [nội dung file với hash là như nhau, nhưng file thì có kích thước vô cùng lớn, còn hash thì chỉ có 40 ký tự](./C%C3%B3%20th%E1%BB%83%20xem%20n%E1%BB%99i%20dung%20file%20v%E1%BB%9Bi%20hash%20l%C3%A0%20nh%C6%B0%20nhau.%20Nh%C6%B0ng%20file%20th%C3%AC%20c%C3%B3%20th%E1%BB%83%20c%C3%B3%20k%C3%ADch%20th%C6%B0%E1%BB%9Bc%20v%C3%B4%20c%C3%B9ng%20l%E1%BB%9Bn,%20c%C3%B2n%20hash%20th%C3%AC%20lu%C3%B4n%20ch%E1%BB%89%20c%C3%B3%2040%20k%C3%BD%20t%E1%BB%B1.md), nên thay vì ta phải quản lý file, thì ta chỉ cần quản lý hash của chúng là được. Điểm trừ tất nhiên là ta không thể tái tạo lại nội dung file từ hash, vì hàm băm là hàm một chiều. Nhưng điều đó không quan trọng, nếu tất cả những gì ta cần là quản lý.

Folder cũng tương tự như vậy. Thay vì quản lý một folder với các file, ta chỉ tạo ra một file là danh sách chứa các hash của các file trong folder đó, rồi quản lý cái hash của cái file đó là được. 

Nguồn:: 