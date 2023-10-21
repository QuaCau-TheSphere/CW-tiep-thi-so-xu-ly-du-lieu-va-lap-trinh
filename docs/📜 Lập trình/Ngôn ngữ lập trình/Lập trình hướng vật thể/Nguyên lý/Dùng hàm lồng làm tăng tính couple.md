---
share: True
---
Function Nesting Use Cases _(mostly functional idioms, almost certainly incomplete since it's off the top of my head)_:

- closures
- function factory (programmatic function creation based on parameters)
- creating functions by calling functool.partial
- creating functions by using lambda
- any other reasons you need to create functions during call time

Trade-offs:

- functions are strongly coupled
- the code is always called (unless it's in an if block)
- additional code complexity
- additional runtime cost _(potentially, because the inner function get's re-defined with every call to the outer function)_
- much harder to extend
- much harder to introspect on the inner function defintion

Nguồn:: [Stack Overflow](../../../../%E2%9A%A1Hi%E1%BB%83u%20bi%E1%BA%BFt%20s%C3%A2u/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md#), [When to use python function nesting?](https://softwareengineering.stackexchange.com/a/237944/192731)