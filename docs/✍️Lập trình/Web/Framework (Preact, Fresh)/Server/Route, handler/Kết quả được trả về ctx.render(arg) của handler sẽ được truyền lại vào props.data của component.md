---
share: true
created: 2023-10-30T14:29
updated: 2025-08-05T22:04
---
 Fresh takes whatever you pass into ctx.render(arg) and sets it on props.data. There is no code to ensure that it is correct or anything. It just passes it along. If nothing is passed to ctx.render() then props.data will be undefined
```tsx
import { Handlers, PageProps } from "$fresh/server.ts"
export const handler: Handlers = {
	GET(req, ctx) {
        return ctx.render({req}) 
    }
}
export default function App(props: PageProps){
    return <h1>
        {props.data.req.url} 
    </h1>
} 
```
[Route cần có ít nhất một handler hoặc một component](./Route%20c%E1%BA%A7n%20c%C3%B3%20%C3%ADt%20nh%E1%BA%A5t%20m%E1%BB%99t%20handler%20ho%E1%BA%B7c%20m%E1%BB%99t%20component.md). [Props là đối số đầu tiên của hàm component, dùng để truyền giá trị các thuộc tính của nó](../../Component,%20JSX/JSX,%20props/Props%20l%C3%A0%20%C4%91%E1%BB%91i%20s%E1%BB%91%20%C4%91%E1%BA%A7u%20ti%C3%AAn%20c%E1%BB%A7a%20h%C3%A0m%20component,%20d%C3%B9ng%20%C4%91%E1%BB%83%20truy%E1%BB%81n%20gi%C3%A1%20tr%E1%BB%8B%20c%C3%A1c%20thu%E1%BB%99c%20t%C3%ADnh%20c%E1%BB%A7a%20n%C3%B3.md)