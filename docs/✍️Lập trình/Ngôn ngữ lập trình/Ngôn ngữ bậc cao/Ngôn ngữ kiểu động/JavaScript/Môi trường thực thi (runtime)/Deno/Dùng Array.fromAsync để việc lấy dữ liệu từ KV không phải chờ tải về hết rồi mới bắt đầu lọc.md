---
share: true
created: 2023-10-30T14:29
updated: 2026-08-06T15:36
---
When you list from KV it doesn't pull back everything at once. Instead it pulls results in batches (size is configurable). Thus, you iterate over results in an asynchronous manner as some iterations will fetch data. This allows you to process data as you retrieve it and not have to wait until it is all fetched.

In essence, it's not pulling an array but iterating over a remote data source. You could view KV as one giant array and list iterates over a sub section of that. It would be inefficient to have to wait until all data was downloaded before using it. Thus the async iterator to allow downloading AND processing at the same time.
Nguồn:: [How to list all entries in Deno KV?](https://stackoverflow.com/a/78210091/3416774)

[Nếu không để đường dẫn vào Deno.openKv(), thì mặc định là ở DENO_DIR. Ở local thì dùng deno info để xem](../../../../../../../%F0%9F%97%84%EF%B8%8FT%E1%BB%95%20ch%E1%BB%A9c%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%8Bnh%20d%E1%BA%A1ng%20d%E1%BB%AF%20li%E1%BB%87u/%C4%90%E1%BB%8Bnh%20d%E1%BA%A1ng%20b%E1%BA%A3ng/N%E1%BA%BFu%20kh%C3%B4ng%20%C4%91%E1%BB%83%20%C4%91%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20v%C3%A0o%20Deno.openKv(),%20th%C3%AC%20m%E1%BA%B7c%20%C4%91%E1%BB%8Bnh%20l%C3%A0%20%E1%BB%9F%20DENO_DIR.%20%E1%BB%9E%20local%20th%C3%AC%20d%C3%B9ng%20deno%20info%20%C4%91%E1%BB%83%20xem.md)
