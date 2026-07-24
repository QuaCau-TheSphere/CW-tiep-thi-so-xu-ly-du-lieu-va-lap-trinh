---
share: true
created: 2023-10-30T14:29
updated: 2026-07-24T21:47
---
## `is` là để hàm kiểm tra ra boolean có thể dùng cho if
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

## `as` là để ép kiểu

[satisfied cho phép ta kiểm tra xem kiểu của một biểu thức có thỏa một kiểu dữ liệu nào đó hay không, trong khi không làm thay đổi kiểu suy luận của chính biểu thức đó](./satisfied%20cho%20ph%C3%A9p%20ta%20ki%E1%BB%83m%20tra%20xem%20ki%E1%BB%83u%20c%E1%BB%A7a%20m%E1%BB%99t%20bi%E1%BB%83u%20th%E1%BB%A9c%20c%C3%B3%20th%E1%BB%8Fa%20m%E1%BB%99t%20ki%E1%BB%83u%20d%E1%BB%AF%20li%E1%BB%87u%20n%C3%A0o%20%C4%91%C3%B3%20hay%20kh%C3%B4ng,%20trong%20khi%20kh%C3%B4ng%20l%C3%A0m%20thay%20%C4%91%E1%BB%95i%20ki%E1%BB%83u%20suy%20lu%E1%BA%ADn%20c%E1%BB%A7a%20ch%C3%ADnh%20bi%E1%BB%83u%20th%E1%BB%A9c%20%C4%91%C3%B3.md)
