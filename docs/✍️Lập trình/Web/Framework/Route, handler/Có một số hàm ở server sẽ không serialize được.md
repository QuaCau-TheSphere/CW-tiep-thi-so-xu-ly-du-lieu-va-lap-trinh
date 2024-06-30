---
share: true
created: 2023-10-30T14:29
updated: 2024-05-20T12:08
---
Passing props to islands is supported, but only if the props are serializable. Fresh can serialize the following types of values:

- Primitive types `string`, `boolean`, `bigint`, and `null`
- Most `number`s (`Infinity`, `-Infinity`, and `NaN` are silently converted to `null`)
- Plain objects with string keys and serializable values
- Arrays containing serializable values
- Uint8Array
- JSX Elements (restricted to `props.children`)
- Preact Signals (if the inner value is serializable)

Circular references are supported. If an object or signal is referenced multiple times, it is only serialized once and the references are restored upon deserialization. Passing complex objects like `Date`, custom classes, or functions is not supported.

Trích từ:: [Interactive islands | Fresh docs](https://fresh.deno.dev/docs/concepts/islands)
[Why is a function not serializable?](https://stackoverflow.com/q/27926619/3416774)

Hệ quả là [Route không bao giờ được gửi đến client. Island được chạy ở cả server và client](./Route%20kh%C3%B4ng%20bao%20gi%E1%BB%9D%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%ADi%20%C4%91%E1%BA%BFn%20client.%20Island%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BA%A1y%20%E1%BB%9F%20c%E1%BA%A3%20server%20v%C3%A0%20client.md)