<!--
  BANNER: se genera desde una URL, no necesita archivos extra.
  Para editarlo cambia en la URL: text= (título), desc= (subtítulo), color= (fondo, hex sin #),
  fontColor= (color del texto, hex sin #) y height= (alto en píxeles).
  Usa %20 para los espacios. Si no quieres banner, borra este bloque <p>.
-->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=151515&height=220&section=header&text=PyTermX&fontSize=64&fontColor=FFC928&fontAlign=50&fontAlignY=42&desc=Aprende%2C%20practica%20y%20automatiza&descSize=26&descAlign=50&descAlignY=70" alt="PyTermX: Aprende, practica y automatiza" width="100%">
</p>

<p align="center">
  <strong>Ejercicios de Python sobre tuplas, listas, secuencias y pathlib, basados en los videos del Curso de Python de PyTermX.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Ejercicios-23-E53935?style=flat-square&labelColor=151515" alt="23 ejercicios">
  <img src="https://img.shields.io/badge/Lenguaje-Python-FFC928?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
  <img src="https://img.shields.io/badge/Partes-4-333333?style=flat-square&labelColor=151515" alt="4 partes">
</p>

<p align="center">
  <a href="#tuplas">Parte 1: Tuplas</a> ·
  <a href="#listas">Parte 2: Listas</a> ·
  <a href="#secuencias">Parte 3: Secuencias</a> ·
  <a href="#pathlib">Parte 4: pathlib</a>
</p>

# Ejercicios de Python: Tuplas, Listas, Secuencias y pathlib

> [!NOTE]
> Todos los ejercicios corresponden a lo visto en los videos del Curso de Python (PyTermX). Si tienes alguna pregunta, déjala en los comentarios del video. Saludos y mucha suerte.

<a id="tuplas"></a>

## Parte 1: Tuplas

1. Crea una tupla llamada `colores` con los valores `"rojo"`, `"verde"` y `"azul"`. Imprime el segundo elemento.

2. Dada la tupla `datos = (10, 20, 30, 40, 50)`, obtén una nueva tupla con solo los tres primeros elementos usando slicing.

3. Crea una tupla `punto = (4, 7)` y desempaca sus valores en dos variables `x` e `y`. Imprime ambas.

4. Concatena las tuplas `t1 = (1, 2, 3)` y `t2 = (4, 5, 6)` en una sola tupla llamada `t3`.

5. Dada la tupla `nombres = ("Ana", "Luis", "Carlos", "Marta")`, obtén cuántas veces aparece `"Luis"` usando el método `count`.

6. Convierte la tupla `numeros = (5, 3, 8, 1, 9)` en una lista llamada `numeros_lista`.

7. Dada la tupla `persona = ("Ramiro", 25, "Newyork")`, desempaca sus tres valores en las variables `nombre`, `edad` y `ciudad`.

<a id="listas"></a>

## Parte 2: Listas

1. Crea una lista llamada `frutas` con `"manzana"`, `"pera"` y `"uva"`. Agrega `"kiwi"` al final usando `append`.

2. Dada la lista `numeros = [4, 8, 15, 16, 23, 42]`, obtén una nueva lista con los elementos en orden inverso usando slicing.

3. Crea la lista `letras = ["a", "b", "c", "d"]` y reemplaza el elemento en la posición 1 por `"z"`.

4. Dada la lista `mixta = [3, 1, 4, 1, 5, 9, 2]`, crea una copia ordenada de menor a mayor usando `sorted()`, sin modificar la original.

5. Une las listas `l1 = [1, 2, 3]` y `l2 = [4, 5, 6]` en una sola lista `l3` usando el operador `+`.

6. Dada la lista `animales = ["perro", "gato", "loro"]`, elimina el último elemento usando `pop()` y guarda el valor eliminado en una variable.

<a id="secuencias"></a>

## Parte 3: Secuencias (operaciones generales aplicables a listas, tuplas y cadenas)

1. Dada la secuencia `s = "Programacion"`, obtén su longitud con `len()`.

2. Dada la lista `valores = [10, 20, 30, 40, 50]`, obtén el máximo y el mínimo usando `max()` y `min()`.

3. Verifica si el número `30` está contenido en la lista `valores = [10, 20, 30, 40, 50]` usando el operador `in`.

4. Dada la tupla `t = (1, 2, 3, 4, 5)`, obtén la suma de todos sus elementos usando `sum()`.

5. Dada la cadena `texto = "Ciberseguridad"`, obtén los caracteres del índice 2 al 7 usando slicing.

6. Dada la lista `datos = [1, 2, 3]`, multiplícala por 3 usando el operador `*` y observa cómo se repite la secuencia.

7. Dada la secuencia `s = [5, 10, 15, 20]`, obtén el índice del valor `15` usando el método `index()`.

<a id="pathlib"></a>

## Parte 4: pathlib

1. Usando `pathlib.Path`, crea un objeto `ruta` que represente el archivo `"documentos/reporte.txt"` e imprime su nombre (`.name`) y su extensión (`.suffix`).

2. Usando `pathlib.Path`, obtén la ruta absoluta del directorio actual con `Path.cwd()` y construye una nueva ruta que apunte a un archivo `"notas.txt"` dentro de ese directorio usando el operador `/`.

3. Crea una lista `extensiones_validas = [".txt", ".csv", ".pdf"]` y un objeto `ruta = Path("informe.pdf")`. Usando el operador `in`, verifica si `ruta.suffix` está contenido en la lista `extensiones_validas`.
