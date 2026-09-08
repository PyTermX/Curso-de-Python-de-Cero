# Ejercicios de Python: Tuplas, Listas, Secuencias y pathlib

> Nota: Todos los ejercicios son acorde a los visto en los vídeos del Curso de Python (PyTermX). Si tienen alguna pregunta, no duden en hacermela saber en
> los comentarios del vídeo! Saludos y Suerte!

---

## Parte 1: Tuplas

1. Crea una tupla llamada `colores` con los valores `"rojo"`, `"verde"` y `"azul"`. Imprime el segundo elemento.

2. Dada la tupla `datos = (10, 20, 30, 40, 50)`, obtén una nueva tupla con solo los tres primeros elementos usando slicing.

3. Crea una tupla `punto = (4, 7)` y desempaca sus valores en dos variables `x` e `y`. Imprime ambas.

4. Concatena las tuplas `t1 = (1, 2, 3)` y `t2 = (4, 5, 6)` en una sola tupla llamada `t3`.

5. Dada la tupla `nombres = ("Ana", "Luis", "Carlos", "Marta")`, obtén cuántas veces aparece `"Luis"` usando el método `count`.

6. Convierte la tupla `numeros = (5, 3, 8, 1, 9)` en una lista llamada `numeros_lista`.

7. Dada la tupla `persona = ("Ramiro", 25, "Newyork")`, desempaca sus tres valores en las variables `nombre`, `edad` y `ciudad`.

---

## Parte 2: Listas

1. Crea una lista llamada `frutas` con `"manzana"`, `"pera"` y `"uva"`. Agrega `"kiwi"` al final usando `append`.

2. Dada la lista `numeros = [4, 8, 15, 16, 23, 42]`, obtén una nueva lista con los elementos en orden inverso usando slicing.

3. Crea la lista `letras = ["a", "b", "c", "d"]` y reemplaza el elemento en la posición 1 por `"z"`.

4. Dada la lista `mixta = [3, 1, 4, 1, 5, 9, 2]`, crea una copia ordenada de menor a mayor usando `sorted()`, sin modificar la original.

5. Une las listas `l1 = [1, 2, 3]` y `l2 = [4, 5, 6]` en una sola lista `l3` usando el operador `+`.

6. Dada la lista `animales = ["perro", "gato", "loro"]`, elimina el último elemento usando `pop()` y guarda el valor eliminado en una variable.

---

## Parte 3: Secuencias (operaciones generales aplicables a listas, tuplas y cadenas)

1. Dada la secuencia `s = "Programacion"`, obtén su longitud con `len()`.

2. Dada la lista `valores = [10, 20, 30, 40, 50]`, obtén el máximo y el mínimo usando `max()` y `min()`.

3. Verifica si el número `30` está contenido en la lista `valores = [10, 20, 30, 40, 50]` usando el operador `in`.

4. Dada la tupla `t = (1, 2, 3, 4, 5)`, obtén la suma de todos sus elementos usando `sum()`.

5. Dada la cadena `texto = "Ciberseguridad"`, obtén los caracteres del índice 2 al 7 usando slicing.

6. Dada la lista `datos = [1, 2, 3]`, multiplícala por 3 usando el operador `*` y observa cómo se repite la secuencia.

7. Dada la secuencia `s = [5, 10, 15, 20]`, obtén el índice del valor `15` usando el método `index()`.

---

## Parte 4: pathlib

1. Usando `pathlib.Path`, crea un objeto `ruta` que represente el archivo `"documentos/reporte.txt"` e imprime su nombre (`.name`) y su extensión (`.suffix`).

2. Usando `pathlib.Path`, obtén la ruta absoluta del directorio actual con `Path.cwd()` y construye una nueva ruta que apunte a un archivo `"notas.txt"` dentro de ese directorio usando el operador `/`.

3. Crea una lista `extensiones_validas = [".txt", ".csv", ".pdf"]` y un objeto `ruta = Path("informe.pdf")`. Usando el operador `in`, verifica si `ruta.suffix` está contenido en la lista `extensiones_validas`.

---
