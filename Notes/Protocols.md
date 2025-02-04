Created: 2025-02-01 14:11

---
Note:

[Typing](https://docs.python.org/3/library/typing.html#module-contents](https://docs.python.org/3/library/typing.html#module-contents)
[Typing RealPython](https://realpython.com/python-protocol/#predefined-protocols-in-python](https://realpython.com/python-protocol/#predefined-protocols-in-python)

| ABC                   | Inherits from              | Abstract Methods                                                 | Mixin Methods                                                                                                                               | Istotne rzeczy o protokole                 |
| --------------------- | -------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| **[[Container ABC]]** | -                          | `__contains__`                                                   | -                                                                                                                                           | Umożliwia operator `in`                    |
| **Hashable**          | -                          | `__hash__`                                                       | -                                                                                                                                           | Umożliwia użycie jako klucz w słownikach   |
| **[[Iterable ABC]]**  | -                          | `__iter__`                                                       | -                                                                                                                                           | Definiuje iterowalność, zwraca iterator    |
| **Iterator**          | Iterable                   | `__next__`                                                       | `__iter__`                                                                                                                                  | Iterowalny obiekt z metodą `__next__`      |
| **Reversible**        | Iterable                   | `__reversed__`                                                   | -                                                                                                                                           | Obsługuje `reversed(obj)`                  |
| **Generator**         | Iterator                   | `send`, `throw`                                                  | `close`, `__iter__`, `__next__`                                                                                                             | Specjalny iterator z `yield`               |
| **[[Sized]]**         | -                          | `__len__`                                                        | -                                                                                                                                           | Umożliwia użycie `len(obj)`                |
| **Callable**          | -                          | `__call__`                                                       | -                                                                                                                                           | Obiekt można wywołać jak funkcję           |
| **Collection**        | Sized, Iterable, Container | `__contains__`, `__iter__`, `__len__`                            | -                                                                                                                                           | Bazowy interfejs dla kolekcji              |
| **Sequence**          | Reversible, Collection     | `__getitem__`, `__len__`                                         | `__contains__`, `__iter__`, `__reversed__`, `index`, `count`                                                                                | Kolekcja indeksowana, np. `list`, `tuple`  |
| **MutableSequence**   | Sequence                   | `__getitem__`, `__setitem__`, `__delitem__`, `__len__`, `insert` | Inherited `Sequence` methods + `append`, `clear`, `reverse`, `extend`, `pop`, `remove`, `__iadd__`                                          | Modyfikowalna sekwencja jak `list`         |
| **ByteString**        | Sequence                   | `__getitem__`, `__len__`                                         | Inherited `Sequence` methods                                                                                                                | Immutable sekwencja bajtów (`bytes`)       |
| **Set**               | Collection                 | `__contains__`, `__iter__`, `__len__`                            | `__le__`, `__lt__`, `__eq__`, `__ne__`, `__gt__`, `__ge__`, `__and__`, `__or__`, `__sub__`, `__rsub__`, `__xor__`, `__rxor__`, `isdisjoint` | Nieuporządkowany zbiór unikalnych wartości |
| **MutableSet**        | Set                        | `__contains__`, `__iter__`, `__len__`, `add`, `discard`          | Inherited `Set` methods + `clear`, `pop`, `remove`, `ior`, `iand`, `ixor`, `isub`                                                           | Modyfikowalny zbiór jak `set`              |

---
Metadata:

Status: #pending
Tags: #python