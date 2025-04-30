---
share: true
created: 2023-10-30T14:29
updated: 2025-03-30T18:01
---
| Log level | Khái niệm                                                                                                           | Cách đối ứng                               | Ví dụ                                                               |
| --------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------------- |
| FATAL     | Level này gây cản trở đến việc vận hành của hệ thống                                                                | Cần sửa ngay                               | Không thể kết nối tới DB                                            |
| ERROR     | Việc thực thi gây ra những lỗi ngoài dự tính                                                                        | Sửa trong thời gian hoạt động của hệ thống | Không thể gửi mail                                                  |
| WARN      | Không phải lỗi nhưng là những vấn đề như: input không như mong muốn hoặc thực thi không như mong muốn               | Refactor định kì                           | API xoá dữ liệu một cách định kì                                    |
| INFO      | Thông báo khi bắt đầu hoặc kết thúc một xử lí, transaction. Cũng có thể là việc đưa ra các thông tin cần thiết khác | Không cần phải sửa                         | Đưa ra nội dung của req / res, hoặc khi bắt đầu hoặc kết thúc batch |
| DEBUG     | Thông tin liên quan đến trạng thái hoạt động của hệ thống                                                           | Không đưa ra ở môi trường production       | Có thể đặt ở các hàm bên trong app                                  |
| TRACE     | Thông tin chi tiết ở mức độ cao hơn DEBUG                                                                           | Không đưa ra ở môi trường production       |                                                                     |

Nguồn:: [Viblo](../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Viblo.md), [Title Unavailable \| Site Unreachable](https://viblo.asia/p/thiet-ke-he-thong-logging-vlZL98gBJQK)

[![cheat sheet: which log level should I use](https://i.sstatic.net/z5Fim.png)](https://i.sstatic.net/z5Fim.png)

Nguồn:: [Stack Overflow](../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [logging - When to use the different log levels - Stack Overflow](https://stackoverflow.com/a/64806781/3416774)