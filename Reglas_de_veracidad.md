# Truthy y Falsy en Python

En Python, cualquier objeto puede evaluarse en un contexto booleano con `bool(obj)`.

- **Falsy**: valores que se evalúan como `False`.
- **Truthy**: valores que se evalúan como `True`.

> No existe una lista exhaustiva de valores *truthy*, porque **cualquier objeto es truthy por defecto**, salvo que sea uno de los valores falsy incorporados o que implemente reglas personalizadas.

---

## Valores Falsy incorporados en Python

| Valor | `bool(valor)` | Notas |
|---|---:|---|
| `None` | `False` | |
| `False` | `False` | |
| `0` | `False` | Entero cero |
| `0.0` | `False` | Float cero |
| `-0.0` | `False` | También es cero |
| `0j` | `False` | Complejo cero |
| `Decimal(0)` | `False` | Requiere `from decimal import Decimal` |
| `Decimal('0')` | `False` | |
| `Decimal('-0')` | `False` | |
| `Fraction(0, 1)` | `False` | Requiere `from fractions import Fraction` |
| `""` / `''` | `False` | String vacío |
| `b""` / `b''` | `False` | Bytes vacío |
| `bytearray()` | `False` | Bytearray vacío |
| `memoryview(b'')` | `False` | Memoryview vacío |
| `[]` | `False` | Lista vacía |
| `()` | `False` | Tupla vacía |
| `{}` | `False` | Diccionario vacío |
| `set()` | `False` | Conjunto vacío |
| `frozenset()` | `False` | Conjunto inmutable vacío |
| `range(0)` | `False` | Rango vacío |
| Objeto con `__bool__` que retorna `False` | `False` | Personalizado |
| Objeto con `__len__` que retorna `0` | `False` | Personalizado |

> Importante: `float('nan')` **no** es falsy. Es truthy.
> También: `0.0` y `-0.0` sí son falsy.

---

## Valores Truthy

No se pueden enumerar todos, porque cualquier objeto es truthy por defecto. Son truthy, por ejemplo:

- `True`
- Números distintos de cero: `1`, `-1`, `3.14`, `-2.5`, `1j`, `Decimal('1')`, `Fraction(1, 2)`, etc.
- Strings no vacíos: `"0"`, `"False"`, `" "`, `"None"`, etc.
- Bytes no vacíos: `b"0"`, `b"\x00"`, etc.
- Colecciones no vacías: `[0]`, `(None,)`, `{0: False}`, `{0}`, `range(1)`, etc.
- `float('nan')`, `float('inf')`, `float('-inf')`
- Funciones, clases, módulos, excepciones, `object()`, `Ellipsis`, etc.
- Cualquier objeto por defecto si no define `__bool__` ni `__len__`.

---

## Reglas de evaluación booleana

1. Si el objeto define `__bool__`, Python usa ese método.
2. Si no define `__bool__`, pero define `__len__`, Python usa `len(obj) != 0`.
3. Si no define ninguno, el objeto es truthy.

```python
class Falso:
    def __bool__(self):
        return False

class Vacio:
    def __len__(self):
        return 0

class Verdadero:
    pass

print(bool(Falso()))     # False
print(bool(Vacio()))     # False
print(bool(Verdadero())) # True
```

---

## Ejemplos rápidos

```python
valores_falsy = [
    None,
    False,
    0,
    0.0,
    -0.0,
    0j,
    "",
    b"",
    bytearray(),
    memoryview(b""),
    [],
    (),
    {},
    set(),
    frozenset(),
    range(0),
]

for valor in valores_falsy:
    print(repr(valor), bool(valor))
```

```python
valores_truthy = [
    True,
    1,
    -1,
    0.1,
    "0",
    "False",
    " ",
    b"0",
    [0],
    (None,),
    {0: False},
    {0},
    range(1),
    float("nan"),
    object(),
]

for valor in valores_truthy:
    print(repr(valor), bool(valor))
```

---

## Nota sobre librerías externas

Bibliotecas como NumPy o pandas pueden definir sus propias reglas de truthiness. Por ejemplo, un array de NumPy con más de un elemento no se puede convertir directamente a `bool` y lanza `ValueError`.
