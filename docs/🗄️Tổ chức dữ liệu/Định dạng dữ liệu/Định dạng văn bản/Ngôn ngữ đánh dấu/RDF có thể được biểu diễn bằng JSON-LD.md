---
share: true
created: 2023-10-30T14:29
updated: 2025-10-02T14:49
---
key-value. Triple store là key-predicate-value
It's more conducive to real work to convert triples like:
```
Anakin (this is an ID that I've elected to make quite readable, not an arbitrary stril)
  hasMentor
    Palpatine

Anakin
  AKA
    Darth Vader

Anakin
  hasName
    Anakin Skywalker
```
to something structured like
```js
{
  @id: "Anakin",
  name: [
    "Anakin Skywalker",
    "Darth Vader"
  ],
  hasMentor: {
    "@id": "Palpatine"
  },
}
```
My `AKA` and `hasName` thing is real weird but then again actual data often does have strange choices like that so just take it as realism

Nguồn:: 
[Thế mạnh của RDF triplestore là tạo ra những liên kết mới không có sẵn lúc nhập vào](../../../../%E2%9A%92%EF%B8%8FNhu%20c%E1%BA%A7u%20c%C3%B4ng%20vi%E1%BB%87c/Ph%C3%A2n%20t%C3%ADch%20d%E1%BB%AF%20li%E1%BB%87u/Ph%C3%A2n%20t%C3%ADch%20m%E1%BA%A1ng%20l%C6%B0%E1%BB%9Bi/Th%E1%BA%BF%20m%E1%BA%A1nh%20c%E1%BB%A7a%20RDF%20triplestore%20l%C3%A0%20t%E1%BA%A1o%20ra%20nh%E1%BB%AFng%20li%C3%AAn%20k%E1%BA%BFt%20m%E1%BB%9Bi%20kh%C3%B4ng%20c%C3%B3%20s%E1%BA%B5n%20l%C3%BAc%20nh%E1%BA%ADp%20v%C3%A0o.md)