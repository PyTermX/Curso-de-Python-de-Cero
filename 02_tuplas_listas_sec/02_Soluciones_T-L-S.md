# SOLUCIONES

## Parte 1: Tuplas — Soluciones

**1.**
```python
colores = ("rojo", "verde", "azul")
print(colores[1])  # verde
```

**2.**
```python
datos = (10, 20, 30, 40, 50)
primeros_tres = datos[:3]
print(primeros_tres)  # (10, 20, 30)
```

**3.**
```python
punto = (4, 7)
x, y = punto
print(x, y)  # 4 7
```

**4.**
```python
t1 = (1, 2, 3)
t2 = (4, 5, 6)
t3 = t1 + t2
print(t3)  # (1, 2, 3, 4, 5, 6)
```

**5.**
```python
nombres = ("Ana", "Luis", "Carlos", "Marta")
veces = nombres.count("Luis")
print(veces)  # 1
```

**6.**
```python
numeros = (5, 3, 8, 1, 9)
numeros_lista = list(numeros)
print(numeros_lista)  # [5, 3, 8, 1, 9]
```

**7.**
```python
persona = ("Ramiro", 25, "Newyork")
nombre, edad, ciudad = persona
print(nombre, edad, ciudad)  # Ramiro 25 Newyork
```

---

## Parte 2: Listas — Soluciones

**1.**
```python
frutas = ["manzana", "pera", "uva"]
frutas.append("kiwi")
print(frutas)  # ['manzana', 'pera', 'uva', 'kiwi']
```

**2.**
```python
numeros = [4, 8, 15, 16, 23, 42]
invertida = numeros[::-1]
print(invertida)  # [42, 23, 16, 15, 8, 4]
```

**3.**
```python
letras = ["a", "b", "c", "d"]
letras[1] = "z"
print(letras)  # ['a', 'z', 'c', 'd']
```

**4.**
```python
mixta = [3, 1, 4, 1, 5, 9, 2]
mixta_ordenada = sorted(mixta)
print(mixta_ordenada)  # [1, 1, 2, 3, 4, 5, 9]
print(mixta)            # [3, 1, 4, 1, 5, 9, 2]  (no cambia)
```

**5.**
```python
l1 = [1, 2, 3]
l2 = [4, 5, 6]
l3 = l1 + l2
print(l3)  # [1, 2, 3, 4, 5, 6]
```

**6.**
```python
animales = ["perro", "gato", "loro"]
eliminado = animales.pop()
print(eliminado)  # loro
print(animales)   # ['perro', 'gato']
```
---

## Parte 3: Secuencias — Soluciones

**1.**
```python
s = "Programacion"
print(len(s))  # 12
```

**2.**
```python
valores = [10, 20, 30, 40, 50]
print(max(valores), min(valores))  # 50 10
```

**3.**
```python
valores = [10, 20, 30, 40, 50]
print(30 in valores)  # True
```

**4.**
```python
t = (1, 2, 3, 4, 5)
print(sum(t))  # 15
```

**5.**
```python
texto = "Ciberseguridad"
print(texto[2:7])  # berseg
```

**6.**
```python
datos = [1, 2, 3]
repetida = datos * 3
print(repetida)  # [1, 2, 3, 1, 2, 3, 1, 2, 3]
```

**7.**
```python
s = [5, 10, 15, 20]
print(s.index(15))  # 2
```

---

## Parte 4: pathlib — Soluciones

**1.**
```python
from pathlib import Path

ruta = Path("documentos/reporte.txt")
print(ruta.name)    # reporte.txt
print(ruta.suffix)  # .txt
```

**2.**
```python
from pathlib import Path

directorio_actual = Path.cwd()
ruta_notas = directorio_actual / "notas.txt"
print(ruta_notas)
```

**3.**
```python
from pathlib import Path

extensiones_validas = [".txt", ".csv", ".pdf"]
ruta = Path("informe.pdf")

print(ruta.suffix in extensiones_validas)  # True
```
