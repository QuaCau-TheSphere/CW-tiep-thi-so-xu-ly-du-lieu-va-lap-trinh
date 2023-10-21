---
share: True
---
Mã JavaScript đó có dạng thế này:
```js
<!-- Google tag (gtag.js) --> 
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XHX9Q6ZB3Q"></script>
<script> 
	window.dataLayer = window.dataLayer || [];
	function gtag(){dataLayer.push(arguments);} gtag('js', new Date()); 
	gtag('config', 'G-********'); </script>
```
Đoạn `G-********` là ID của nó. [Một Google tag có thể có nhiều ID](./M%E1%BB%99t%20Google%20tag%20c%C3%B3%20th%E1%BB%83%20c%C3%B3%20nhi%E1%BB%81u%20ID.md#). [Có thể cài nó trực tiếp trên web, hoặc nhờ plugin hỗ trợ, nhưng tốt nhất là nên cài thông qua Google Tag Manager](./N%C3%AAn%20c%C3%A0i%20Google%20tag%20trong%20Google%20Tag%20Manager%20thay%20v%C3%AC%20c%C3%A0i%20tr%E1%BB%B1c%20ti%E1%BA%BFp%20tr%C3%AAn%20web%20ho%E1%BA%B7c%20qua%20plugin.md#).

Các tag này sẽ đổ dữ liệu về các destination, chính là các web data stream trong GA. 

<sub>Lưu ý rằng ngoài web ra thì các app điện thoại cũng có thể làm data stream cho GA. Nhưng vì ở đó có những cách thức khác để theo dõi hành vi người dùng, nên chúng không được dùng làm destination cho Google tag. Tức là, **Google tag chỉ có duy nhất một loại destination là web data stream**. Nếu bạn chỉ có duy nhất một website để phân tích, thì bạn sẽ chỉ có một Google tag, một destination, một data stream, và tất cả chúng sẽ từa tựa lẫn nhau khiến cho bạn dễ bị rối.</sub>

# Thiết lập các Google tag
Để có một **danh sách tổng hợp tất cả các Google tag mà mình có**, hãy vào [Google Tag Manager](https://tagmanager.google.com/#/home): ![](https://storage.googleapis.com/support-kms-prod/Q5lAquhBvBoVYFmUpBjRYdCc0a45iJVloZPJ) 

Để **thiết lập chi tiết cách data stream làm destination như thế nào**, hãy vào [Google Analytics](https://analytics.google.com/analytics): ![Screenshot of the Google Analytics 4 data stream settings. The Google tag settings are located in the data stream settings](https://storage.googleapis.com/support-kms-prod/jRorNBqYurSg9prt08pizpolkGC6elmHj7qp)

> [!attention] Phân biệt
> Khi bấm vào 
