Created: 2025-02-01 14:23

---
Note:

Zwraca liczbę elementów **len(sized)**.
Nie może zużywac ani modyfikowac kolekcji.

```python

class X:
	def __len__(self) -> int:
	return 42

x = X()
len(x) #42


```
---
Metadata:

Status: #pending
Tags: #python #sized