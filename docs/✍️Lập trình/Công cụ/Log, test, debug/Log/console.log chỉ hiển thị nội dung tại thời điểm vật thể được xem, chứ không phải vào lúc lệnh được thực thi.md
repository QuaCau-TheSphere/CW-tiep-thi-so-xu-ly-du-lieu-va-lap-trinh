---
share: true
created: 2023-10-24T18:26
updated: 2024-04-23T01:41
---
As you can see below, even though the array is logged before the mutating method is applied, the debugger still shows it as already being applied. However, its elements and properties when called specifically still return correctly:

![](https://i.imgur.com/SjzA0DP.png)

If I add a breakpoint before the methods, then it is correct. If I continue then the result doesn't change.

![](https://i.imgur.com/AuWkA4C.png)


```js
const array = ["cat","dog","mouse"]
console.log('array', array);
console.log('array[0] :>> ', array[0]);
console.log('array.length :>> ', array.length);

array.splice(0, 1)
// array.push('bat')
debugger
```


Nguồn:: [Stack Overflow](../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [console.log() async or sync?](https://stackoverflow.com/q/23392111/3416774), [console.log() shows the changed value of a variable before the value actually changes](https://stackoverflow.com/q/11284663/3416774)
