---
share: True
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


Nguồn:: [Stack Overflow](../../../%E2%9A%A1Hi%E1%BB%83u%20bi%E1%BA%BFt%20s%C3%A2u/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md#), [console.log() async or sync?](https://stackoverflow.com/q/23392111/3416774), [console.log() shows the changed value of a variable before the value actually changes](https://stackoverflow.com/q/11284663/3416774)