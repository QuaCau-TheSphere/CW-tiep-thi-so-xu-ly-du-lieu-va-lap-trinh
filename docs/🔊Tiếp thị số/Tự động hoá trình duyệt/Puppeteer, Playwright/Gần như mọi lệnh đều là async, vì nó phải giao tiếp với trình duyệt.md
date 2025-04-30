---
share: true
created: 2023-10-30T14:29
updated: 2024-11-30T13:45
---
Auto-waiting or not is irrelevant to whether you need to use `await`. `await` is used whenever there's a network call, a system call, or inter-process communication that needs to talk to another process or the operating system. Node is single-threaded, so for it to operate efficiently, it uses asynchronous code constructs like promises to allow it to perform other tasks while the network call is in flight.

Since the browser you're automating with Puppeteer is a separate process from Node, any CDP call is asynchronous, regardless of whether the call involves waiting for a condition or not. So the only calls that don't need `await` are ones that don't involve CDP calls, like `page.locator()`. Don't mix up the words "wait" and "await"--totally different here! See [Why are almost all Puppeteer calls asynchronous?](https://stackoverflow.com/questions/71368256/why-are-almost-all-puppeteer-calls-asynchronous) for details.

Nguồn:: [javascript - Page.locator() is the recommended way to select and interact with elements. Why does it offer less functionalities than Page.$()? - Stack Overflow](https://stackoverflow.com/a/79210080/3416774)

[await với async là cách để viết hàm bất đồng bộ với tư duy khi viết hàm tuần tự](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/C%C3%BA%20ph%C3%A1p/B%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99/await/await%20v%E1%BB%9Bi%20async%20l%C3%A0%20c%C3%A1ch%20%C4%91%E1%BB%83%20vi%E1%BA%BFt%20h%C3%A0m%20b%E1%BA%A5t%20%C4%91%E1%BB%93ng%20b%E1%BB%99%20v%E1%BB%9Bi%20t%C6%B0%20duy%20khi%20vi%E1%BA%BFt%20h%C3%A0m%20tu%E1%BA%A7n%20t%E1%BB%B1.md)