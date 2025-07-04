---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
# `is` là để hàm kiểm tra ra boolean có thể dùng cho if
Giả sử ta có code sau:
```ts
interface Chó {
    sủa: 'gâu gâu'
} 
interface Mèo {
    kêu: 'meo meo'
} 
declare function lấyTênThú(): Chó | Mèo 
```

Ta tạo hàm kiểm tra xem một con thú có phải là chó hay không. Đây là một hàm boolean bình thường:
```ts
/** Nếu `thú.sủa === 'gâu gâu'` thì `return true`, tức là đây chính là chó. Còn nếu `thú.sủa === undefined` thì `return false`, tức là đây không phải là chó */
function làChó(thú: Chó | Mèo){
    return thú.sủa !== undefined;
}
const thú = lấyTênThú()
if (làChó(thú)) {
    thú.sủa    
} else {
    thú.kêu
}
```
Khi viết như này thì TS không tự hiểu được là ở block true `thú` chỉ có thể là `Chó`, còn ở block false thì chỉ có thể là `Mèo`:
![](https://i.imgur.com/IMNk1h9.png)
(bị lỗi font, đừng để ý đến màu, mà hãy để ý đến gạch chân) 

Lý do nó không hiểu được là  vì nó chỉ biết hàm `làChó()` trả về `true` hoặc `false`, chứ không biết là trả về `Chó` hay `Mèo`:
![](https://i.imgur.com/NXfYqNy.png)

Nhưng nếu ở hàm `làChó()` ta dùng `thú is Chó` như sau:
```diff
- function làChó(thú: Chó | Mèo){
+ function làChó(thú: Chó | Mèo): thú is Chó {
```
Thì nó sẽ biết là nếu trả về `true`, thì `true` đó phải được hiểu là `Chó`. Khi đó, trong if nó sẽ tự động nhận dạng được và sẽ tự động gợi ý được luôn:
![](https://i.imgur.com/EbEqDUv.png)
![](https://i.imgur.com/koobLhe.png)

Cái này gọi là **type predicate** hoặc là type guard.

# `as` là để ép kiểu

[satisfied là để kiểm tra xem dữ liệu mình nhập bằng tay có thoả kiểu hay không](./satisfied%20l%C3%A0%20%C4%91%E1%BB%83%20ki%E1%BB%83m%20tra%20xem%20d%E1%BB%AF%20li%E1%BB%87u%20m%C3%ACnh%20nh%E1%BA%ADp%20b%E1%BA%B1ng%20tay%20c%C3%B3%20tho%E1%BA%A3%20ki%E1%BB%83u%20hay%20kh%C3%B4ng.md)