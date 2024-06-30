---
share: true
created: 2023-10-30T14:29
updated: 2024-04-23T01:46
---
```python
soup = BeautifulSoup('<b class="boldest">Extremely bold</b>', 'html.parser')
tag = soup.b
type(tag)
# <class 'bs4.element.Tag'>
```

```python
tag = BeautifulSoup('<b id="boldest">bold</b>', 'html.parser').b
tag['id']
# 'boldest'
```
Nguồn:: [Beautiful Soup Documentation — Beautiful Soup 4.12.0 documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#bs4.Tag.attrs) 
[Những vật thể đơn giản dùng để tra cứu dữ liệu theo từ khoá gọi là từ điển](../../../Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20l%E1%BA%ADp%20tr%C3%ACnh%20h%C6%B0%E1%BB%9Bng%20v%E1%BA%ADt%20th%E1%BB%83/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/Nh%E1%BB%AFng%20v%E1%BA%ADt%20th%E1%BB%83%20%C4%91%C6%A1n%20gi%E1%BA%A3n%20d%C3%B9ng%20%C4%91%E1%BB%83%20tra%20c%E1%BB%A9u%20d%E1%BB%AF%20li%E1%BB%87u%20theo%20t%E1%BB%AB%20kho%C3%A1%20g%E1%BB%8Di%20l%C3%A0%20t%E1%BB%AB%20%C4%91i%E1%BB%83n.md)