---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
[Lớp thực ra là một cú pháp ](L%E1%BB%9Bp%20th%E1%BB%B1c%20ra%20l%C3%A0%20m%E1%BB%99t%20c%C3%BA%20ph%C3%A1p.md)
```javascript
function Hero(name, level) {
    this.name = name;
    this.level = level;
}

// Adding a method to the constructor
Hero.prototype.greet = function() {
    return `${this.name} says hello.`;
}
```

Class:
```javascript
class Hero {
    constructor(name, level) {
        this.name = name;
        this.level = level;
    }

    // Adding a method to the constructor
    greet() {
        return `${this.name} says hello.`;
    }
}
```
Nguồn:: [function - JavaScript - What exactly does the "class" keyword actually do? How is it implemented? - Stack Overflow](https://stackoverflow.com/q/77602331/3416774)