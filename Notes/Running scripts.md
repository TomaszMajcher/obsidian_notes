Created: 2025-02-01 11:37

---
Note:

Uruchomienie skrytpu w python z instalacją tymczasową zależności przy uzyciu [[UV]]

**Commands**

```python

# file example.py

import requests


r = requests.get('https://api.nbp.pl/api/exchangerates/rates/a/usd?format=json')
print(r.json())


```

```shell
uv run --with requests example.py

# --with  mowi jakie zaleznosci powinny by zaisntalowane, --with może byc wiele razy.

```

**Script dependencies**

Deklarowanie metadanych do uruchmienia skryptu automatycznie

```python

# /// script
# dependencies = [
#   "requests<3",
# ]
# ///

import requests


r = requests.get('https://api.nbp.pl/api/exchangerates/rates/a/usd?format=json')
print(r.json())

```
```shell

uv run example.py

```
---
Metadata:

Status: #pending
Tags: #python #scripts #uv