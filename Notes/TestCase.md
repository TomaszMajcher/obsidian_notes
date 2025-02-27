Created: 2025-02-25 20:25

---
Note: 

**Obsługa kodu, w którym spodziewamy się wyjątku**

Nie można tego napisac bez contex-managera, gdyż błąd pythona przerywa test.
Zawsze używaj match, w celu upewnienia się, że na pewno odpowiedni wyjątek został wyemitowany.

```python
import pytest

def add(x):
return x

def test_raise_exception_with_info():  
    match_regex = "missing 1 .* positional argument"  
  
    with pytest.raises(TypeError, match=match_regex):  
        add()

def test_raise_exception_with_info_alternative():  
# better performance   
    with pytest.raises(TypeError) as exc_info:  
        add() 
  
    expected = "missing 1 required positional argument"  
    assert expected in str(exc_info.value)
```

**Test structure**

1. Arrange-Act-Assert (AAA)
2. Given -when-then

```python

def test_to_dict():  
    # GIVEN a Card object with known contents
    c1 = Card("something", "yolo", "todo", 123)  
  
    # WHEN we call to_dict() on the object  
    c2 = c1.to_dict()  
  
    # THEN the result will be a dictionary with known content  
    c2_expected = {  
        "summary": "something",  
        "owner": "yolo",  
        "state": "todo",  
        "id": 123,  
    }  
  
    assert c2 == c2_expected


```
---
Metadata:

Status: #pending
Tags: #pytest