---
share: true
created: 2023-10-09T14:46
updated: 2025-04-26T21:09
---
[Có thể hiểu blob là hash của một tệp, tree là hash của một thư mục, còn commit thực ra chỉ là hash của cả thư mục tổng](./C%C3%B3%20th%E1%BB%83%20hi%E1%BB%83u%20blob%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20t%E1%BB%87p,%20tree%20l%C3%A0%20hash%20c%E1%BB%A7a%20m%E1%BB%99t%20th%C6%B0%20m%E1%BB%A5c,%20c%C3%B2n%20commit%20th%E1%BB%B1c%20ra%20ch%E1%BB%89%20l%C3%A0%20hash%20c%E1%BB%A7a%20c%E1%BA%A3%20th%C6%B0%20m%E1%BB%A5c%20t%E1%BB%95ng.md) 

Git sử dụng 1 database được xây dựng trên 4 objects (đối tượng) chính:

- **Blob**: key-value của file
- **Tree**: key-value của folder, trong tree chứa pointer trỏ đến tree và blob
- **Commit**: chứa pointer trỏ đến tree
- **Annotated Tag**: 1 pointer trỏ đến commit

![](https://giangtester.com/wp-content/uploads/2021/09/image-3-1024x563.png)
![](https://giangtester.com/wp-content/uploads/2021/09/image-4-1024x557.png)

- Blue là blob
- Green là tree
- Orange là commit

Git lưu **blob, tree, commit** ở đâu? —> ở folder `.git\objects` nhé
Nguồn:: [ GiangTester Blog](https://giangtester.com/ban-chat-cua-git/) ](B%E1%BA%A3n%20ch%E1%BA%A5t%20c%E1%BB%A7a%20git.md)

<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?v=MyvyqdQ3OjI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
