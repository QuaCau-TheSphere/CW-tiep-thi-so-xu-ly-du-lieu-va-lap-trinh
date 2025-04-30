---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
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
[Những vật thể đơn giản dùng để tra cứu dữ liệu theo từ khoá gọi là từ điển](../../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/M%E1%BA%A3ng,%20t%E1%BB%AB%20%C4%91i%E1%BB%83n/Nh%E1%BB%AFng%20v%E1%BA%ADt%20th%E1%BB%83%20%C4%91%C6%A1n%20gi%E1%BA%A3n%20d%C3%B9ng%20%C4%91%E1%BB%83%20tra%20c%E1%BB%A9u%20d%E1%BB%AF%20li%E1%BB%87u%20theo%20t%E1%BB%AB%20kho%C3%A1%20g%E1%BB%8Di%20l%C3%A0%20t%E1%BB%AB%20%C4%91i%E1%BB%83n.md). [Vật thể là dạng dữ liệu có những thuộc tính thành phần](../../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n%20v%C3%A0%20nguy%C3%AAn%20l%C3%BD%20l%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/V%E1%BA%ADt%20th%E1%BB%83,%20l%E1%BB%9Bp/V%E1%BA%ADt%20th%E1%BB%83%20l%C3%A0%20d%E1%BA%A1ng%20d%E1%BB%AF%20li%E1%BB%87u%20c%C3%B3%20nh%E1%BB%AFng%20thu%E1%BB%99c%20t%C3%ADnh%20th%C3%A0nh%20ph%E1%BA%A7n.md)