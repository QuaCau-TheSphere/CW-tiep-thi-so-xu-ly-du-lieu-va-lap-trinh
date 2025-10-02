---
share: true
created: 2023-10-30T14:29
updated: 2025-08-05T22:03
---
Lý do:: [Phải viết hook trong component. Không viết trong loop hoặc if được](../Hook/Ph%E1%BA%A3i%20vi%E1%BA%BFt%20hook%20trong%20component.%20Kh%C3%B4ng%20vi%E1%BA%BFt%20trong%20loop%20ho%E1%BA%B7c%20if%20%C4%91%C6%B0%E1%BB%A3c.md)
[Giá trị trả về của useContext() là giá trị được truyền vào thuộc tính value của provider](./Gi%C3%A1%20tr%E1%BB%8B%20tr%E1%BA%A3%20v%E1%BB%81%20c%E1%BB%A7a%20useContext()%20l%C3%A0%20gi%C3%A1%20tr%E1%BB%8B%20%C4%91%C6%B0%E1%BB%A3c%20truy%E1%BB%81n%20v%C3%A0o%20thu%E1%BB%99c%20t%C3%ADnh%20value%20c%E1%BB%A7a%20provider.md)
```jsx
import { createContext } from 'preact'
import { useContext } from 'preact/hooks'

const TênContext = createContext()

export default function App() {
  return (
    <TênContext.Provider value={giáTrịĐượcTruyềnVàoProvider}>
	  <User />
    </TênContext.Provider>
  )
}

function User() {
  const username = useContext(TênContext) // Nếu giáTrịĐượcTruyềnVàoProvider = 'Bob' thì username = 'Bob'
  return <>{username}</>
}
```

Ví dụ:
```tsx
export const TênContext = createContext('sdf') 

export default function CấuHìnhProvider({ children }) {
    return (
        <ContextCấuHình.Provider value={giáTrịĐượcTruyềnVàoProvider} >
            {children} 
        </ContextCấuHình.Provider>
    )
} 

function Component(){
  const [giáTrịĐượcTruyềnVàoProvider] = useContext(TênContext)
} 
```
[Context – Preact Tutorial](https://preactjs.com/tutorial/06-context/)