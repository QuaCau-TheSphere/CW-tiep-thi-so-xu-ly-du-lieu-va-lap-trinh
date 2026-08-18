---
share: true
created: 2023-10-24T18:26
updated: 2026-08-13T21:35
---
### Khác với [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)

Các biến được khai báo với `var` có phạm vi `function scope`, còn với `let`, `const` thì nó phạm vi `block scope`

- `function scope`: Biến được khai báo dùng được trong toàn bộ function
    
    ```js
    function usingVar() {
        let x = 1;
        if (true) {
            var y = 2;
            console.log(x); // 1
        }
    
        console.log(y); // 2
    }
    ```
    

`block scope`: Biến được khai báo chỉ sử dụng được trong block {} nơi mà nó được khai báo

```js
function usingLet() {
    let x = 1;
    if (true) {
        let y = 2;
        console.log(x); // 1
    }

    console.log(y); // Error: y is not defined
}
```

Hoặc đối với biến trong vòng for:

```js
for (let i = 0; i < 5; ++i) {
    console.log(i); // OK
}

console.log(i); // Error: y is not defined
```

### let vs const

- `let`: biến đã khai báo có thể được gán lại
    
    ```js
    let letVar = 'My old name';
    if (true) {
        letVar = 'I can have new name';
    }
    ```
    

`const`: biến đã khai báo không thể được gán lại

```js
const constVar = 'Only god can change me';
if (true) {
    constVar = 'Don\'t try to change me'; // Error: invalid assignment
}
```

Tuy nhiên nếu const là object thì giá trị của object vẫn có thể bị thay đổi. Chỉ _không thể bị gán thành object khác_ mà thôi.

```js
const myObject = {
    id: 1,
    name: 'Can be changed'
};
myObject.name = 'New name'; // OK
myObject = null; // Error
```

Nguồn:: [Tham chiếu và ghi chú ngắn về ES6, ESNext](https://viblo.asia/p/tham-chieu-va-ghi-chu-ngan-ve-es6-esnext-Do7544PQ5M6)

[Có thể dùng const cho một biến đã được dùng const ở scope ngoài. Có thể gọi var cho một biến chưa được gọi var trong cùng scope mà chỉ được gọi ở scope nhỏ hơn](./C%C3%B3%20th%E1%BB%83%20d%C3%B9ng%20const%20cho%20m%E1%BB%99t%20bi%E1%BA%BFn%20%C4%91%C3%A3%20%C4%91%C6%B0%E1%BB%A3c%20d%C3%B9ng%20const%20%E1%BB%9F%20scope%20ngo%C3%A0i.%20C%C3%B3%20th%E1%BB%83%20g%E1%BB%8Di%20var%20cho%20m%E1%BB%99t%20bi%E1%BA%BFn%20ch%C6%B0a%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20var%20trong%20c%C3%B9ng%20scope%20m%C3%A0%20ch%E1%BB%89%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BB%8Di%20%E1%BB%9F%20scope%20nh%E1%BB%8F%20h%C6%A1n.md)