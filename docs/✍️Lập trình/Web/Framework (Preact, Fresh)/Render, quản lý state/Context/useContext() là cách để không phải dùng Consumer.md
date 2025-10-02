---
share: true
created: 2023-10-30T14:29
updated: 2025-08-05T22:03
---
Bình thường, hàm `createContext()` sẽ cho ta dùng 2 JSX: `Provider` cho đầu vào, và `Consumer` cho đầu ra.
## Đầu vào
```jsx
import { createContext } from 'preact'

const TênContext = createContext('Alice')

export default function App() {
    return (
	    // provide the username value to our subtree:
	    <TênContext.Provider value="Bob">
		    <ComponentCon>
			    ...
			    <ComponentConCháuChắtChútChít />
			    ...
		    <ComponentCon />
	    </TênContext.Provider>
	)
}
```
## Đầu ra
```jsx
import { TênContext } from "../routes/index.tsx";

export default function ComponentConCháuChắtChútChít(){
	return (
	    <TênContext.Consumer>
			{username => (
			  // access the current username from context:
			  <span>{username}</span>
			)}
	    </TênContext.Consumer>
	)  
} 
```

Khi dùng `useContext()`, đầu ra bây giờ trông như sau:
```jsx
import { TênContext } from "../routes/index.tsx";
import { useContext } from "preact/hooks";

export default function ComponentConCháuChắtChútChít(){
	const username = useContext(TênContext)
	return <span>{username}</span>
} 
```

Việc dùng hook này không chỉ làm code ngắn hơn mà nó còn cho ta được lấy giá trị như một biến bình thường mà không phải ở trong JSX
Nó giống như việc [await với async là cách để viết hàm bất đồng bộ với tư duy khi viết hàm tuần tự](../../../../Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/C%C3%BA%20ph%C3%A1p/B%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99/await/await%20v%E1%BB%9Bi%20async%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20vi%E1%BA%BFt%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20v%E1%BB%9Bi%20t%C6%B0%20duy%20khi%20vi%E1%BA%BFt%20h%C3%A0m%20tu%E1%BA%A7n%20t%E1%BB%B1.md)

Nguồn:: [Context | Preact: Fast 3kb React alternative with the same ES6 API. Components & Virtual DOM.](https://preactjs.com/tutorial/06-context/)
[createContext() nằm ngoài global, useContext() nằm trong component](./createContext()%20n%E1%BA%B1m%20ngo%C3%A0i%20global,%20useContext()%20n%E1%BA%B1m%20trong%20component.md) 