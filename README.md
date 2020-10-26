<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-configurations-middleware.svg?maxAge=3600)](https://pypi.org/project/django-configurations-middleware/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-configurations-middleware.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-configurations-middleware.py/actions)

### Installation
```bash
$ [sudo] pip install django-configurations-middleware
```

#### Features
key  | default value  | env
-|-|-
`MIDDLEWARE` | `[]` | `DJANGO_MIDDLEWARE`
`MIDDLEWARE_FILE` | `None` | `DJANGO_MIDDLEWARE_FILE`
`MIDDLEWARE_FILES` | `[]` | `DJANGO_MIDDLEWARE_FILES`

##### `settings.py`
```python
from configurations import Configuration
from django_configurations_middleware import MiddlewareMixin

class Base(MiddlewareMixin,Configuration):
    MIDDLEWARE_FILE = 'middleware.txt'

```

example #2:
```python
class Base(MiddlewareMixin,Configuration):
    MIDDLEWARE_FILES = ['middleware1.txt','middleware2.txt']
```

example #3:
```bash
$ export DJANGO_MIDDLEWARE_FILE=middleware.txt
```

#### Links
+   [django-configurations](https://github.com/jazzband/django-configurations)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
