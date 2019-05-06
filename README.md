*This is a work in progress*

The Python `requests` package creates a convenient API to make http requests, but comes at the price of adding a 3rd party dependency to your project.

You might be able to get away with using Python's standard library (and keeping your sanity) if you're doing something simple.

Feel free to copy any of these code snippets to your codebase, no attribution required.

### http GET request

requests

```python
import requests

requests.get(url)
```

without requests

```python
import urllib.parse
import urllib.request

def http_get(url):
    res = urllib.request.urlopen(url)
    charset = res.headers.get_content_charset() or "utf-8"
    return res.read().decode(charset)
```
