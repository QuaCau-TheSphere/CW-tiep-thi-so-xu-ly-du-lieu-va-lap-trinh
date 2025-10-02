---
share: true
created: 2023-10-30T14:29
updated: 2025-08-05T22:05
---
Fresh is a website framework designed to be used with Deno
Preact is essentially a reactive rendering library
Preact can be used seperately to Fresh
The relationship between Next.JS and React is the same as the relationship between Fresh and Preact 

Preact is just a rendering library and only concerns itself with getting stuff on the screen as fast as possible. It doesn't do routing or any of those other concerns an app typically needs. That's where Fresh comes in. The export default from a route file tells Fresh's file based router that this is a route that you want to use. Then when you go to a route, Fresh basically calls Preact's render() function to render the HTML, so you don't need to do that yourself when working in Fresh 

For simple sites there isn't reall much Preact specific stuff to learn other than that you can compose parts of the HTML by creating functions that return JSX like
```js
function Foo() {
  return <p>Hello world</p>
}

export default function Page() {
  return <div>
    <Foo />
  </div>
}
```
This concept alone gets you pretty far.

In my opinion there is no need to learn Preact before Fresh. That's pointless. Build a site with Fresh and you'll pick up enough Preact knowledge while doing that already

Nguồn:: [Discord](https://discord.com/channels/684898665143206084/991511118524715139/1192090620198662144)
[Fresh dùng Preact cho UI](./Fresh%20d%C3%B9ng%20Preact%20cho%20UI.md)

| Framework | Meta Framework            |
| --------- | ------------------------- |
| Preact    | Fresh                     |
| React     | Next.js, Remix, Gatsby... |
| Vue       | Nuxt                      |
| Svelte    | SvelteKit                 |
| Solid     | SolidStart                | 
Nguồn:: [unable to use preact context in fresh · Issue #983 · denoland/fresh · GitHub](https://github.com/denoland/fresh/issues/983#issuecomment-1891656732)

[React được sinh ra để làm việc với trạng thái](./React%20%C4%91%C6%B0%E1%BB%A3c%20sinh%20ra%20%C4%91%E1%BB%83%20l%C3%A0m%20vi%E1%BB%87c%20v%E1%BB%9Bi%20tr%E1%BA%A1ng%20th%C3%A1i.md)