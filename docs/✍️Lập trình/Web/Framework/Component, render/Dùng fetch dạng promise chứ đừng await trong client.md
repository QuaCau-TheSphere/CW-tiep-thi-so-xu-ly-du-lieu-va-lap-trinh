---
share: true
created: 2023-10-30T14:29
updated: 2024-04-12T00:37
---

Lý do:: 
- Island không được phép là async 

[Promise được sinh ra là để không phải dùng if lồng quá nhiều](../../../Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/JavaScript%20v%C3%A0%20Python/JavaScript/Callback,%20promise,%20async,%20await/Promise%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20l%C3%A0%20%C4%91%E1%BB%83%20kh%C3%B4ng%20ph%E1%BA%A3i%20d%C3%B9ng%20if%20l%E1%BB%93ng%20qu%C3%A1%20nhi%E1%BB%81u.md)
```js
fetch('https://jsonplaceholder.typicode.com/postses').then(function (response) {
	// The API call was successful
	// (wait, it was?)
	console.log(response.status);
	return response.json();
}).then(function (data) {
	// This is the JSON from our response
	console.log(data);
}).catch(function (error) {
	// There was an error
	console.warn(error);
});
```
Tham khảo:: [The JavaScript fetch() method | Go Make Things](https://gomakethings.com/the-javascript-fetch-method/)