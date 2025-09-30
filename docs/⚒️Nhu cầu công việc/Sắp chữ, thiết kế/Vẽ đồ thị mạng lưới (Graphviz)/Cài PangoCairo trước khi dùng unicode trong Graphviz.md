---
share: true
created: 2023-10-24T18:26
updated: 2025-03-03T18:48
---
- Install expat library (`sudo apt install libexpat1-dev`)
- Install PangoCairo library (`sudo apt install libpango1.0-dev`)
- Compile and install Graphviz from [source](https://graphviz.org/download/source):
	```bash
	./configure --with-pangocairo
	make
	sudo make install
	```

Nguồn:: [Stack Overflow](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md), [Why do texts with non-ASCII characters have right padding?](https://stackoverflow.com/a/76630218/3416774)

[Lý thuyết Unicode](../../../%F0%9F%94%A0K%C3%BD%20t%E1%BB%B1,%20v%C4%83n%20b%E1%BA%A3n,%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%C3%A1nh%20d%E1%BA%A5u/Ti%E1%BA%BFng%20Vi%E1%BB%87t,%20Unicode,%20emoji/L%C3%BD%20thuy%E1%BA%BFt%20Unicode/index.md)