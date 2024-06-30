---
share: true
created: 2023-09-27T15:07
updated: 2024-02-01T21:39
---
Nguồn:: [Real Python](../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Real%20Python.md), [When Should You Use .\_\_repr\_\_() vs .\_\_str\_\_() in Python? – Real Python](https://realpython.com/python-repr-vs-str/)

I was advised to not use `vars()` or `__dict__`, just use the actual API of the classes. If an object isn't printing well without that introspection, then that's the devs fault for not writing proper string and print methods (usually via `__repr__`). Or in other words, Python defers the responsibility to display the objects to the dev, while JS takes that responsibility.
Nguồn:: [Is it correct that Python does not encourage us to read objects's content?](https://langdev.stackexchange.com/q/2966/223)
[Trong REPL, gọi trực tiếp vật thể ra thì kết quả là __repr__(). Nếu dùng print thì kết quả là __str__()](./Trong%20REPL,%20g%E1%BB%8Di%20tr%E1%BB%B1c%20ti%E1%BA%BFp%20v%E1%BA%ADt%20th%E1%BB%83%20ra%20th%C3%AC%20k%E1%BA%BFt%20qu%E1%BA%A3%20l%C3%A0%20__repr__().%20N%E1%BA%BFu%20d%C3%B9ng%20print%20th%C3%AC%20k%E1%BA%BFt%20qu%E1%BA%A3%20l%C3%A0%20__str__().md)
[Nếu lớp không định nghĩa cả __repr__() và __str__() thì kết quả trả về có dạng __main__.Class_name object at 0x1025c4ed0](./N%E1%BA%BFu%20l%E1%BB%9Bp%20kh%C3%B4ng%20%C4%91%E1%BB%8Bnh%20ngh%C4%A9a%20c%E1%BA%A3%20__repr__()%20v%C3%A0%20__str__()%20th%C3%AC%20k%E1%BA%BFt%20qu%E1%BA%A3%20tr%E1%BA%A3%20v%E1%BB%81%20c%C3%B3%20d%E1%BA%A1ng%20__main__.Class_name%20object%20at%200x1025c4ed0.md) 
