---
share: true
updated: 2026-07-24T21:47
created: 2026-07-10T12:48
---
Khái niệm:: 
```js
parseInt('0.5') // 0  
parseInt('0.5') // 0  
parseInt('0.05') // 0  
parseInt('0.005') // 0  
parseInt('0.0005') // 0  
parseInt('0.00005' ) // 0  
parseInt('0.000005') // 0  
parseInt('015') // 15  
parseInt('015', 8) // 13  
parseInt('15px', 10) // 15
```
Nguồn:: [Tại sao trong JavaScript parseInt(0,0000005) kết quả lại là “5” 😊 (Series: Bí kíp Javascript - PHẦN 40)](https://viblo.asia/p/tai-sao-trong-javascript-parseint00000005-ket-qua-lai-la-5-series-bi-kip-javascript-phan-40-3RlL5YoqLbB)

Lý do là vì `parseInt()` dùng `String()`, và lấy số đầu tiên trong chuỗi:
- `String(0,0000005) // 5e-7`
- `parseInt("5foo") // 5`

Nên `parseInt(0,0000005)` sẽ tương đương với `parseInt("5e-7")`. Và kết quả của cái này là 5

[String(x) giống x.tostring(), nhưng không gây ra lỗi nếu x là null hoặc undefined](../String(x)%20gi%E1%BB%91ng%20x.tostring(),%20nh%C6%B0ng%20kh%C3%B4ng%20g%C3%A2y%20ra%20l%E1%BB%97i%20n%E1%BA%BFu%20x%20l%C3%A0%20null%20ho%E1%BA%B7c%20undefined.md)
