---
share: true
updated: 2026-10-20T15:52
created: 2026-10-20T15:52
---
Khái niệm:: 
I wonder how people handle security in Node. Sure, juniors may not appreciate this well, but once people have awareness of this problem, then why don't they seek for a better runtime? Assuming they have responsibility and don't push the risk to the users, then the only reason I can think of is that they do have solution for this

It's generally cheaper at enterprise scale to layer more crap on, like Docker or Synk, than port your 100k+ line codebase.

Dodo/Deno, again, wins for smaller teams in this regard - it's sort of what "secure by default" means. Node is "secure with addons" - and the addons are cheaper than a rewrite when your codebase is big enough

Nguồn:: [Discord](https://discord.com/channels/1558888938251223050/1560790338480906290/1561937356142149643)