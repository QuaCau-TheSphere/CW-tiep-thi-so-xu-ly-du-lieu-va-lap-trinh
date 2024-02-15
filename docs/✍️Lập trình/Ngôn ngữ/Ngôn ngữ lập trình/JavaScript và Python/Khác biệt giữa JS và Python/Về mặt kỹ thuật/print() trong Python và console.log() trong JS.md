---
share: true
created: 2023-10-30T14:29
updated: 2024-02-01T21:39
---

Lý do:: [Việc đọc vật thể trong JS dễ dàng hơn so với Python vì Python từ đầu đã được thiết kế để cố gắng đảm bảo tính đóng gói, còn JS thì không](../V%E1%BB%81%20m%E1%BA%B7t%20tri%E1%BA%BFt%20l%C3%BD/Vi%E1%BB%87c%20%C4%91%E1%BB%8Dc%20v%E1%BA%ADt%20th%E1%BB%83%20trong%20JS%20d%E1%BB%85%20d%C3%A0ng%20h%C6%A1n%20so%20v%E1%BB%9Bi%20Python%20v%C3%AC%20Python%20t%E1%BB%AB%20%C4%91%E1%BA%A7u%20%C4%91%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20thi%E1%BA%BFt%20k%E1%BA%BF%20%C4%91%E1%BB%83%20c%E1%BB%91%20g%E1%BA%AFng%20%C4%91%E1%BA%A3m%20b%E1%BA%A3o%20t%C3%ADnh%20%C4%91%C3%B3ng%20g%C3%B3i,%20c%C3%B2n%20JS%20th%C3%AC%20kh%C3%B4ng.md)

Trong REPL của JS (console), chỉ cần gọi vật thể ra là được. Ở Python thì không như vậy. [Trong REPL, gọi trực tiếp vật thể ra thì kết quả là __repr__(). Nếu dùng print thì kết quả là __str__()](../../Python/Class/Trong%20REPL,%20g%E1%BB%8Di%20tr%E1%BB%B1c%20ti%E1%BA%BFp%20v%E1%BA%ADt%20th%E1%BB%83%20ra%20th%C3%AC%20k%E1%BA%BFt%20qu%E1%BA%A3%20l%C3%A0%20__repr__().%20N%E1%BA%BFu%20d%C3%B9ng%20print%20th%C3%AC%20k%E1%BA%BFt%20qu%E1%BA%A3%20l%C3%A0%20__str__().md)

|                | JS                                        | Python                    |
| -------------- | ----------------------------------------- | ------------------------- |
| Đọc thuộc tính | `object.attribute`, `object['attribute']` | `object.get('attribute')` |

