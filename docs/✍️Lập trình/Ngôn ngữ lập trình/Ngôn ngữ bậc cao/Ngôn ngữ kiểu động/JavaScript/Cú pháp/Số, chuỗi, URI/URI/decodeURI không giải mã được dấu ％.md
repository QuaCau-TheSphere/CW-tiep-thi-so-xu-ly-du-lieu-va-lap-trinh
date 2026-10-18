---
share: true
created: 2023-10-30T14:29
updated: 2026-10-18T15:09
---
```typescript
/**
 * decodeURI() can't decode the `%` character, as it is used in any encoded character
 * @author [Why does decodeURIComponent('%') lock up my browser?](https://stackoverflow.com/a/54310080/3416774)
 */
export function decodeURIComponentSafe(path: string): string {
  return decodeURIComponent(path.replace(/%(?![0-9a-fA-F]+)/g, "%25"));
}
```

[GitHub - jridgewell/safe-decode-uri-component: Safely decode URI components, leaving invalid sequences as they are](https://github.com/jridgewell/safe-decode-uri-component)

Nguồn:: [Why does decodeURIComponent('%') lock up my browser?](https://stackoverflow.com/a/54310080/3416774)

[encodeURI nên được đặt tên là fixBrokenURI, còn decodeURI nên được đặt là potentiallyBreakMyPreviouslyWorkingURI](./encodeURI%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%E1%BA%B7t%20t%C3%AAn%20l%C3%A0%20fixBrokenURI,%20c%C3%B2n%20decodeURI%20n%C3%AAn%20%C4%91%C6%B0%E1%BB%A3c%20%C4%91%E1%BA%B7t%20l%C3%A0%20potentiallyBreakMyPreviouslyWorkingURI.md)
[Mặc dù trong đường dẫn được phép có ký tự Unicode, các spec khác nhau sẽ có những cách chấp nhận khác nhau](../../../../../../../../%F0%9F%A4%96%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn,%20ti%E1%BA%BFn%20tr%C3%ACnh,%20terminal,%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh/Nguy%C3%AAn%20l%C3%BD%20chung/%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn,%20t%C3%AAn%20t%E1%BA%ADp%20tin/M%E1%BA%B7c%20d%C3%B9%20trong%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20%C4%91%C6%B0%E1%BB%A3c%20ph%C3%A9p%20c%C3%B3%20k%C3%BD%20t%E1%BB%B1%20Unicode,%20c%C3%A1c%20spec%20kh%C3%A1c%20nhau%20s%E1%BA%BD%20c%C3%B3%20nh%E1%BB%AFng%20c%C3%A1ch%20ch%E1%BA%A5p%20nh%E1%BA%ADn%20kh%C3%A1c%20nhau.md)
