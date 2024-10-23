# Beautiful Soup

<https://beautiful-soup-4.readthedocs.io/en/latest/>

<https://pypi.org/project/beautifulsoup4/>

Pulls data out of HTML and XML. Good for web scraping. Sits atop HTML or XML parser, providing Pythonic idioms for navigating, searching, and modifying parse tree.

## Load Page and Parse

```python
from bs4 import BeautifulSoup
import requests

url = 'https://en.wikipedia.org/wiki/List_of_S%26P_500_companies'

r = requests.get(url)
print('request status: ', r.status_code)

soup = BeautifulSoup(r.text, features='html.parser')
```

## Navigate

Can directly reference by tag name. If it exists, will return valid object.

```python
soup.title  # first 'title' tag found
soup.title.name  # tag name
soup.title.string  # tag's string content
soup.title.parent.name

soup.p['class']  ## attribute value
```

## Find Element(s)

```python
## list of tags matching search criteria
soup.find_all('a')
soup.find_all('div', class_='product')

## find first matching
soup.find(id='main')
soup.find('span', id='contact')
```

## Children (`contents`)

List of children of current tag:

```python
table.contents
```

## Attributes (`attrs`)

```python
img.attrs
```

## Get All Links

```python
links = soup('a')
for link in links:
    print('URL: ', link.get('href', None))
```

## Get All Text

```python
print(soup.get_text())
```

## `prettify()`

Formats HTML/XML doc into readable string when printed. Available on all tag objects, including root BeautifulSoup object.

```python
print(soup.prettify())
print(div.prettify())
print(table.prettify())
```
