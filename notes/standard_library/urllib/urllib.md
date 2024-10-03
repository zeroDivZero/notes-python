# `urllib`

<https://docs.python.org/3/library/urllib.html>

Package collecting URL handling modules.

* [`urllib.request`](.\request.md) for opening and reading URLs

* `urllib.error` contains exceptions raised by `urllib.request`

* [`urllib.parse`](.\parse.md) for parsing URLs

* `urllib.robotparser` for parsing [**robots.txt**](http://www.robotstxt.org/orig.html) files

Quick and straightforward, no additional installation, good for downloading small files sequentially. Can build on top for complex functionalities, but many high-level 3rd-party libraries already exist.
