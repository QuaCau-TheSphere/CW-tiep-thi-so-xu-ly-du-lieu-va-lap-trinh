---
share: true
created: 2023-10-30T14:29
updated: 2024-04-03T14:34
---

Khi phải dùng Consumer:
```jsx
import { createContext } from 'preact'

const Username = createContext()

export default function App() {
  return (
    // provide the username value to our subtree:
    <Username.Provider value="Bob">
	  <Username.Consumer>
		{username => (
		  // access the current username from context:
		  <span>{username}</span>
		)}
	  </Username.Consumer>
    </Username.Provider>
  )
}
```

Khi dùng `useContext()`:
```jsx
import { createContext } from 'preact'
import { useContext } from 'preact/hooks'

const Username = createContext()

export default function App() {
  const username = useContext(Username) // "Bob"
  return (
    <Username.Provider value="Bob">
	  <span>{username}</span>
    </Username.Provider>
  )
}
```
Nguồn:: [Context | Preact: Fast 3kb React alternative with the same ES6 API. Components & Virtual DOM.](https://preactjs.com/tutorial/06-context/)
[createContext() nằm ngoài global, useContext() nằm trong component](./createContext()%20n%E1%BA%B1m%20ngo%C3%A0i%20global,%20useContext()%20n%E1%BA%B1m%20trong%20component.md) 