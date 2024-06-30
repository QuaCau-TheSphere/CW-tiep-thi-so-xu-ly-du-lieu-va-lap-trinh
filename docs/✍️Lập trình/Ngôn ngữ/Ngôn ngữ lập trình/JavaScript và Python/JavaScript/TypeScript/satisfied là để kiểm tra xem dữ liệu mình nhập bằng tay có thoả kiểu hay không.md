---
share: true
created: 2023-10-30T14:29
updated: 2024-05-03T21:13
---
```ts
type Colors = "red" | "green" | "blue";
type RGB = [red: number, green: number, blue: number];
const palette = {
	red: [255, 0, 0],
	green: "#00ff00",    
	bleu: [0, 0, 255]
//  ~~~~ The typo is now caught!
} satisfies Record<Colors, string | RGB>;
```

Nguồn:: [freeCodeCamp](../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/freeCodeCamp.md), [How to Use the TypeScript satisfies Operator](https://www.freecodecamp.org/news/typescript-satisfies-operator/)
[TypeScript: Documentation - TypeScript 4.9](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-4-9.html)
[as, is là những cách để nói cho TS biết là mình hiểu nhiều hơn nó](./as,%20is%20l%C3%A0%20nh%E1%BB%AFng%20c%C3%A1ch%20%C4%91%E1%BB%83%20n%C3%B3i%20cho%20TS%20bi%E1%BA%BFt%20l%C3%A0%20m%C3%ACnh%20hi%E1%BB%83u%20nhi%E1%BB%81u%20h%C6%A1n%20n%C3%B3.md)