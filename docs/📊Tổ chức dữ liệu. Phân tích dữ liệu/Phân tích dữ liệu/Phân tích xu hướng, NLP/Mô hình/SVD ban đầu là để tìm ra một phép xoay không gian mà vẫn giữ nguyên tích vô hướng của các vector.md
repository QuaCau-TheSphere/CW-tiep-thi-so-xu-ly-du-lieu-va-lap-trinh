---
share: true
created: 2023-10-24T18:26
updated: 2024-03-10T16:12
---
Từ mối liên hệ này khái niệm về ma trận trực giao đã hình thành để tạo ra các phép xoay đặc biệt.

Phương pháp SVD sẽ tìm ra một lớp các ma trận xấp xỉ tốt nhất với một ma trận cho trước dựa trên khoảng cách norm Frobenios giữa 2 ma trận. Người ta đã chứng minh được rằng ma trận xấp xỉ tốt nhất được biểu diễn dưới dạng tích của 3 ma trận rất đặc biệt bao gồm 2 _ma trận trực giao_ (orthogonal matrix) và 1 _ma trận đường chéo_ (diagonal matrix). Quá trình nhân ma trận thực chất là quá trình biến đổi các điểm dữ liệu của ma trận gốc thông qua những phép xoay trục (rotation) và phép thay đổi độ lớn (scaling) và từ đó tạo ra những điểm dữ liệu mới trong không gian mới. Điều đặc biệt của ma trận đường chéo đó là các phần tử của nó chính là những giá trị riêng của ma trận gốc. Những điểm dữ liệu trong không gian mới có thể giữ được 100% thông tin ban đầu hoặc chỉ giữ một phần lớn thông tin của dữ liệu ban đầu thông qua các phép truncate SVD. Bằng cách sắp xếp các trị riêng theo thứ tự giảm dần trên đường chéo chính thuật toán SVD có thể thu được ma trận xấp xỉ tốt nhất mà vẫn đảm bảo giảm được hạng của ma trận sau biến đổi và kích thước các ma trận nhân tử nằm trong giới hạn cho phép. Do đó nó tiết kiệm được thời gian và chi phí tính toán và đồng thời cũng tìm ra được một giá trị dự báo cho ma trận gốc với mức độ chính xác cao.

Nguồn:: [Phạm Đình Khánh](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Ph%E1%BA%A1m%20%C4%90%C3%ACnh%20Kh%C3%A1nh.md), [Singular Value Decomposition | Kaggle](https://www.kaggle.com/code/phamdinhkhanh/singular-value-decomposition/notebook)

Bới vì [Độ tương đồng của hai vector chính là tích vô hướng vừa nó](../Vector/%C4%90%E1%BB%99%20t%C6%B0%C6%A1ng%20%C4%91%E1%BB%93ng%20c%E1%BB%A7a%20hai%20vector%20ch%C3%ADnh%20l%C3%A0%20t%C3%ADch%20v%C3%B4%20h%C6%B0%E1%BB%9Bng%20v%E1%BB%ABa%20n%C3%B3.md), nên SVD không làm biến dạng độ tương đồng của chúng
