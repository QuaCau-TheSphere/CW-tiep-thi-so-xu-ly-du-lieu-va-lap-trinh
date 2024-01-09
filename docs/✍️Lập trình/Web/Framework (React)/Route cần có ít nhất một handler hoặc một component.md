---
share: true
created: 2023-10-30T14:29
updated: 2024-01-04T21:06
---

[Khi có một yêu cầu tới một route, handler được gọi trước, sau đó tới component](./Khi%20c%C3%B3%20m%E1%BB%99t%20y%C3%AAu%20c%E1%BA%A7u%20t%E1%BB%9Bi%20m%E1%BB%99t%20route,%20handler%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20tr%C6%B0%E1%BB%9Bc,%20sau%20%C4%91%C3%B3%20t%E1%BB%9Bi%20component.md)
Nếu không có handler nào thì Fresh sẽ tự động thêm một cái mặc định này:

```tsx
export const handler = {
  get(req, ctx) => ctx.render()
}
```
Fresh takes whatever you pass into ctx.render(arg) and sets it on props.data. There is no code to ensure that it is correct or anything. It just passes it along. If nothing is passed to ctx.render() then props.data will be undefined

Nguồn:: [Routes | Fresh docs](https://fresh.deno.dev/docs/concepts/routes)