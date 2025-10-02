---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
[Đường dẫn trong launch.json là cwd](../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/C%C3%B4ng%20c%E1%BB%A5/IDE/VS%20Code/%C4%90%C6%B0%E1%BB%9Dng%20d%E1%BA%ABn%20trong%20launch.json%20l%C3%A0%20cwd.md) 
Ví dụ `script.ts` này gọi đến `file.txt`:
```ts
const đườngDẫnTươngĐối = '../file.txt'
const nộiDungFile = await Deno.readTextFile(đườngDẫnTươngĐối)
console.log(nộiDungFile)
```
Ta sẽ chia ra hai trường hợp:
## 1. `file.txt` nằm ngoài folder (trong `.`) :
```
. 
├── file.txt 
└── folder/ 
	└── script.ts
```
## 2. `file.txt` nằm trong folder (trong `./folder`):
```
. 
└── folder/ 
	├── script.ts 
	└── file.txt
```
[pwd là thư mục mà tiến trình sẽ chạy. cwd là thư mục mà mình đang ở đó](./pwd%20l%C3%A0%20th%C6%B0%20m%E1%BB%A5c%20m%C3%A0%20ti%E1%BA%BFn%20tr%C3%ACnh%20s%E1%BA%BD%20ch%E1%BA%A1y.%20cwd%20l%C3%A0%20th%C6%B0%20m%E1%BB%A5c%20m%C3%A0%20m%C3%ACnh%20%C4%91ang%20%E1%BB%9F%20%C4%91%C3%B3.md)

| Vị trí của `file.txt` | Đường dẫn đến `file.txt` trong `script.ts` | PWD và lệnh chạy `script.ts` ở terminal     | Kết quả |
| --------------------- | ------------------------------------------ | ------------------------------------------- | ------- |
| `./folder`            | `./file.txt`                               | Ở `./folder` chạy `deno run -A ./script.ts` | ✔       |
| `.`                   | `../file.txt`                              | Ở `./folder` chạy `deno run -A ./script.ts` | ✔       |
| `.`                   | `./file.txt`                               | Ở `.` chạy `deno run -A ./folder/script.ts` | ✔       |
| `.`                   | `./file.txt`                               | Ở `./folder` chạy `deno run -A ./script.ts` | ❌      |
| `.`                   | `../file.txt`                              | Ở `.` chạy `deno run -A ./folder/script.ts` | ❌      |
| `./folder`            | `./file.txt`                               | Ở `.` chạy `deno run -A ./folder/script.ts` | ❌      |
| `./folder`            | `../file.txt`                              | Ở `./folder` chạy `deno run -A ./script.ts` | ❌      |
| `./folder`            | `../file.txt`                              | Ở `.` chạy `deno run -A ./folder/script.ts` | ❌      |

Chính vì như vậy, nên [Dùng absolute path cho lành](./D%C3%B9ng%20absolute%20path%20cho%20l%C3%A0nh.md)