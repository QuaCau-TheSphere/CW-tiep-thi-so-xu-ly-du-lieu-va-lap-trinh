---
share: true
created: 2023-09-26T21:04
updated: 2024-02-01T21:39
---
```python
>>> import datetime
>>> today = datetime.datetime.now()

>>> today
datetime.datetime(2023, 2, 18, 18, 40, 2, 160890)

>>> print(today)
2023-02-18 18:40:02.160890
```
Nguồn:: [Real Python](../../../../../%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Real%20Python.md), [When Should You Use .\_\_repr\_\_() vs .\_\_str\_\_() in Python? – Real Python](https://realpython.com/python-repr-vs-str/)
[__repr__() trả về mô tả chi tiết để người lập trình bảo trì và sửa lỗi. __str__() trả về mô tả đơn giản cho người dùng sử dụng](./__repr__()%20tr%E1%BA%A3%20v%E1%BB%81%20m%C3%B4%20t%E1%BA%A3%20chi%20ti%E1%BA%BFt%20%C4%91%E1%BB%83%20ng%C6%B0%E1%BB%9Di%20l%E1%BA%ADp%20tr%C3%ACnh%20b%E1%BA%A3o%20tr%C3%AC%20v%C3%A0%20s%E1%BB%ADa%20l%E1%BB%97i.%20__str__()%20tr%E1%BA%A3%20v%E1%BB%81%20m%C3%B4%20t%E1%BA%A3%20%C4%91%C6%A1n%20gi%E1%BA%A3n%20cho%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng%20s%E1%BB%AD%20d%E1%BB%A5ng.md) 

```python
from datetime import datetime
class Event:
    def __init__(self, summary:str, description:str, location:str, startDate:datetime, endDate:datetime):
        self.summary = summary
        self.description = description
        self.location = location
        self.startDate = startDate
        self.endDate = endDate
    def __str__(self):
        return f'{self.summary}\t{self.startDate.strftime("%Y-%m-%d %H:%M:%S")}'
startDate = datetime(2023, 12, 14, 16, 00, 00)
endDate = datetime(2023, 12, 14, 17, 00, 00)

event = Event('summary', 'description', 'location', startDate, endDate)

print(event)
```