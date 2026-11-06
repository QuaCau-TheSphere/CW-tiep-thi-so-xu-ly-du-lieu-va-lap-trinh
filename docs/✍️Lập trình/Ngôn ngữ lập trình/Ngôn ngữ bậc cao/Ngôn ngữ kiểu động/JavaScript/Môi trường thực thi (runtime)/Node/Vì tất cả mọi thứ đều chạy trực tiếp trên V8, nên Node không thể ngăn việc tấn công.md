---
share: true
updated: 2026-10-20T15:52
created: 2026-10-20T00:27
---
Khái niệm:: 

to add to what have been already said, it's impossible to have a "deno mode" in node unfortunately. i've looked into it, and just for instance, sandboxing in node is impossible without a huge change in architecture

everything is running directly in v8, whereas deno has v8 bindings to be able to intercept all syscalls to make proper sandboxing

so the "permissions system" that node has is basically useless. i feel like they just implemented it to just say "we have that too ! " but if you look at their official docs they say:

> The permission model implements a "seat belt" approach, which prevents trusted code from unintentionally changing files or using resources that access has not explicitly been granted to. It does not provide security guarantees in the presence of malicious code. Malicious code can bypass the permission model and execute arbitrary code without the restrictions imposed by the permission model.

the whole goal of permissions/sandboxing is that you cannot escape it (or if you can it's a bug, not "by design")

which is why they can't support url imports. without sandboxing, it's insane to run raw external scripts (but tbh even external packages), with one this becomes a non issue. someone tries to harvest your data ? just deny it

in an era where everyone vibe codes and sometimes don't even read the code, idk how everyones put so much trust into each other tbh. sure you have to put some trust somewhere, but it's easier to trust a few persons that a thousand one

for some reason, node seems to copy what bun/deno innovated with, but "half-ass" it (with all the respect). even the native typescript support is just type stripping

tbh I agree it's too bad we have maintain 2 runtimes that are so similar, but i feel like it'll be impossible to convince the node maintainer on such points because the philosophy between both communities diverge

Trích từ:: [Discord](https://discord.com/channels/1558888938251223050/1560790338480906290/1561492632788672529)

[Muốn Node an toàn thì phải bổ sung thêm các lớp khác. Deno thì không](./Mu%E1%BB%91n%20Node%20an%20to%C3%A0n%20th%C3%AC%20ph%E1%BA%A3i%20b%E1%BB%95%20sung%20th%C3%AAm%20c%C3%A1c%20l%E1%BB%9Bp%20kh%C3%A1c.%20Deno%20th%C3%AC%20kh%C3%B4ng.md)