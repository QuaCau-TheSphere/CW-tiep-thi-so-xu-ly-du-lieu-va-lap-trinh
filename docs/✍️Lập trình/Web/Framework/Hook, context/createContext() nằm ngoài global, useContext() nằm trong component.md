---
share: true
created: 2023-10-30T14:29
updated: 2024-01-26T12:29
---

Lý do:: [Phải viết hook trong component](./Ph%E1%BA%A3i%20vi%E1%BA%BFt%20hook%20trong%20component.md)
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
