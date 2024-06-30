---
share: true
created: 2023-10-30T14:29
updated: 2024-05-14T13:12
---
[useEffect được sinh ra là để side effect không tự động chạy mỗi khi component được render](./useEffect%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20l%C3%A0%20%C4%91%E1%BB%83%20side%20effect%20kh%C3%B4ng%20t%E1%BB%B1%20%C4%91%E1%BB%99ng%20ch%E1%BA%A1y%20m%E1%BB%97i%20khi%20component%20%C4%91%C6%B0%E1%BB%A3c%20render.md)
[Trong useEffect chỉ dùng được promise, không dùng async được](./Trong%20useEffect%20ch%E1%BB%89%20d%C3%B9ng%20%C4%91%C6%B0%E1%BB%A3c%20promise,%20kh%C3%B4ng%20d%C3%B9ng%20async%20%C4%91%C6%B0%E1%BB%A3c.md) 
```ts
const [data, setData] = useState()

useEffect(() => {
  const fetchData = async () => {
    const data = await fetch('https://yourapi.com')
    const json = await response.json();
    setData(json);
  }
  // call the function
  fetchData().catch(console.error);
}, [])
```
Nguồn:: 