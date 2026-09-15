# Valores Truthy y Falsy en Python

## Valores Falsy (se evalúan como `False`)

En Python, los siguientes valores se consideran **falsy**:

| Valor | Tipo |
|---|---|
| `False` | booleano |
| `None` | NoneType |
| `0` | int |
| `0.0` | float |
| `0j` | complex |
| `Decimal(0)` | decimal |
| `Fraction(0, 1)` | fraction |
| `""` | str vacío |
| `[]` | list vacía |
| `()` | tuple vacía |
| `{}` | dict vacío |
| `set()` | set vacío |
| `frozenset()` | frozenset vacío |
| `range(0)` | range vacío |
| objetos con `__bool__()` que retorna `False` | objetos personalizados |
| objetos con `__len__()` que retorna `0` | objetos personalizados |

## Valores Truthy (se evalúan como `True`)

**Todo lo demás** es truthy, incluyendo:

```python
True
1, -1, 42          # cualquier número distinto de cero
0.1, -0.5           # cualquier float distinto de cero
"0"                 # ¡cuidado! string "0" es truthy (no está vacío)
"False"             # ¡cuidado! string con contenido, aunque diga "False"
[0]                 # lista con un elemento (aunque sea 0)
[False]             # lista con un elemento (aunque sea False)
{0: 0}              # diccionario con contenido
(0,)                # tupla con un elemento
" "                 # string con un espacio (no vacío)
float('nan')        # NaN es truthy
float('inf')        # infinito es truthy
```

## Reglas clave a recordar

1. **La regla general**: los contenedores vacíos son falsy; los no vacíos son truthy, sin importar qué contengan.
2. **Cuidado con strings numéricos**: `"0"` es truthy porque es un string no vacío, aunque parezca representar cero.
3. **Python evalúa `bool()` así**:
   - Primero busca `__bool__()` en el objeto.
   - Si no existe, busca `__len__()` (0 = False, cualquier otro valor = True).
   - Si ninguno existe, el objeto es truthy por defecto.

## Ejemplo práctico

```python
def es_truthy(valor):
    return bool(valor)

valores = [False, None, 0, 0.0, "", [], {}, (), set()]
for v in valores:
    print(f"{v!r}: {es_truthy(v)}")  # todos imprimen False

valores_truthy = [True, 1, "0", " ", [0], {0: 0}, -1]
for v in valores_truthy:
    print(f"{v!r}: {es_truthy(v)}")  # todos imprimen True
```
