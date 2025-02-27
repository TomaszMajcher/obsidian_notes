Created: 2025-02-25 20:48

---
Note: 

**Commands**

```shell

# odpala wszystkie testy
pytest

# pojedynczy test suite
pytest <dirs>/<module>.py

# błędy z diffem
pytest -vv

# pojedyncza metoda w klasie
pytest <path>/<module>.py::TestClass::test_method

# pojedyncza klasa 
pytest <path>/<module>.py::TestClass

# pojedyncza funkcja
pytest <path>/<module>.py::test_function

# wszystkie test suites w package
pytest <path>/<path>

# wszystkie ktore pasuja do wyrazenia
pytest -k pattern

# wszystkie po markerze
pytest -m marker_name

# bez traceback z podsumowaniem na końcu
pytest -v --tb=no 

# warunki logiczne do -k
pytest -v --tb=no "(dict or ids) and not inequaliy"

```

---
Metadata:

Status: #pending
Tags: #pytest #CLI
