---
share: true
created: 2023-08-25T14:20
updated: 2024-07-13T17:02
---
# Chỉnh launch.json
[launch.json dùng để thiết lập debugger](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/C%C3%B4ng%20c%E1%BB%A5/IDE%20(VS%20Code)/launch.json%20d%C3%B9ng%20%C4%91%E1%BB%83%20thi%E1%BA%BFt%20l%E1%BA%ADp%20debugger.md)

1. Mở VS Code lên
2. Bấm vào nút ![Extensions view trong VS Code](https://code.visualstudio.com/assets/docs/editor/extension-marketplace/extensions-view-icon.png) ở thanh bên trái và kiếm `Deno extension`. Bấm cài đặt
3. Bấm <kbd>Ctrl + Shift + P</kbd> và chọn *Deno: Initialize Workspace Configuration*
4. Đảm bảo rằng file `launch.json` trong thư mục `.vscode` có dạng như sau:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "request": "launch",
            "name": "Launch Program",
            "type": "node",
            "program": "${workspaceFolder}/test/main.debug.js",
            "cwd": "${workspaceFolder}",
            "runtimeExecutable": "XXXXX",
            "runtimeArgs": [
                "run",
                "--unstable",
                "--inspect-wait",
                "--allow-all",
            ],
            "attachSimplePort": 9229
        }
    ]
}
```
Trong đó XXXXX là đường dẫn đến tập tin `deno.exe`. Có thể kiếm bằng cách bật CMD lên và nhập `where deno`

# Phím tắt


| Phím tắt         | Chức năng        |
| ---------------- | ---------------- |
| F5               | Chạy code        |
| F9               | Tạo breakpoint   |
| Ctrl + Shift + D | Mở debug sidebar |
| Ctrl + `         | Mở terminal      |
| Ctrl + Shift + Y | Mở debug console | 

## Cách kiểm tra và sửa lỗi

Cài thêm các plugin: Total TypeScript, Turbo Console Log
![](https://i.imgur.com/iWUq8jB.png)
