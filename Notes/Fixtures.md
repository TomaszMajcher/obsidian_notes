Created: 2025-02-26 19:41

---
Note: 
**Commands**

```bash

# lista plus opis wszystkich fixtures dostępnych w danej instalacji pytest
pytest --fixtures

# pokazanie kiedy co sie odpala (jaki fixture)
pytest --setup-show

# pokazanie test case i fixtures jakie używają z dokumentacją i lokalizacją
pytest --fixtures-per-test

```

**Commands**

```python

import pytest  
  
  
@pytest.fixture  
def some_data():  
    """Return answer to ultimate question"""  
    return 42  
  
  
def test_fixture(some_data):  
    assert some_data == 42


```
---
Metadata:

Status: #pending
Tags: #pytest
