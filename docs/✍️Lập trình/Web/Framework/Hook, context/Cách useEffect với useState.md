---
share: true
created: 2023-10-30T14:29
updated: 2024-04-03T14:34
---

```ts
const [data, setData] = useState()

useEffect(() => {
  const fetchData = async () => {
    const data = await fetch(<https://yourapi.com<)
    const json = await response.json();
    setData(json);
  }

  // call the function
  fetchData()
    .catch(console.error);;
}, [])
```
Nguồn:: 