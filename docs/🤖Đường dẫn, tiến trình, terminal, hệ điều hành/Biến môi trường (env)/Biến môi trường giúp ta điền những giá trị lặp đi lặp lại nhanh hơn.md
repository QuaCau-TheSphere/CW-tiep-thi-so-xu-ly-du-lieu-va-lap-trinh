---
share: true
created: 2023-10-24T18:26
updated: 2025-10-02T14:03
---
Biến môi trường tiếng Anh là *environmental variable*. Viết tắt là `env`.
<iframe width="560" height="315" src="https://www.youtube.com/embed/ADh_OFBfdEE?si=U30Tg6HS8hvzgCcv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

[env của người dùng được ưu tiên hơn env của hệ thống. Nhưng với biến path thì ngược lại](./env%20c%E1%BB%A7a%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng%20%C4%91%C6%B0%E1%BB%A3c%20%C6%B0u%20ti%C3%AAn%20h%C6%A1n%20env%20c%E1%BB%A7a%20h%E1%BB%87%20th%E1%BB%91ng.%20Nh%C6%B0ng%20v%E1%BB%9Bi%20bi%E1%BA%BFn%20path%20th%C3%AC%20ng%C6%B0%E1%BB%A3c%20l%E1%BA%A1i.md)

Dùng lệnh này để liệt kê tất cả các env trong [PowerShell](../Terminal,%20shell,%20console/PowerShell/PowerShell%20l%C3%A0%20m%E1%BB%99t%20ng%C3%B4n%20ng%E1%BB%AF%20shell.md):
```PowerShell
get-childitem env:
```