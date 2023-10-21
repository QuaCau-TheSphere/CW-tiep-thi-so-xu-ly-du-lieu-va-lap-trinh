---
share: True
---
- Install expat library (`sudo apt install libexpat1-dev`)
- Install pangocairo library (`sudo apt install libpango1.0-dev`)
- Compile and install graphviz from source ([https://graphviz.org/download/source/](https://graphviz.org/download/source/)):
	```xml
	./configure --with-pangocairo
	make
	sudo make install
	```
    
Nguồn:: [Stack Overflow](../../../%E2%9A%A1Hi%E1%BB%83u%20bi%E1%BA%BFt%20s%C3%A2u/%CE%9E%20Ngu%E1%BB%93n/Stack%20Overflow.md#), [Why do texts with non-ASCII characters have right padding?](https://stackoverflow.com/a/76630218/3416774)