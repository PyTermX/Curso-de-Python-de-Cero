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
  <strong>Ejemplos en Python de bucles while, búsqueda de archivos con pathlib y lectura de Excel con pandas, para practicar paso a paso.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Lenguaje-Python-FFC928?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
  <img src="https://img.shields.io/badge/Ejemplos-3-E53935?style=flat-square&labelColor=151515" alt="Ejemplos: 3">
  <img src="https://img.shields.io/badge/Tipo-C%C3%B3digo_de_pr%C3%A1ctica-333333?style=flat-square&labelColor=151515" alt="Tipo: código de práctica">
</p>

<p align="center">
  <a href="#ejemplo-1">Contraseña con while</a> ·
  <a href="#ejemplo-2">Buscador de archivos</a> ·
  <a href="#ejemplo-3">Lectura de Excel</a>
</p>

# Ejemplos de while, pathlib y pandas
Tres programas cortos que muestran cómo repetir una acción hasta cumplir una condición, comprobar si un archivo existe y leer una parte de una hoja de Excel.

> [!NOTE]
> Recuerda que estos ejemplos son explicados en lo vídeos del curso de Python: de cero hasta automatización, a partir del vídeo #32

<!-- TODO: confirmar el título del repositorio o de la clase a la que pertenecen estos ejemplos. -->

<a id="ejemplo-1"></a>

## Ejemplo 1: Contraseña con while

Pide la contraseña hasta que el usuario introduce `12345`. El bucle `while` se repite mientras la condición `password != 12345` sea verdadera.

```python
password = 0

while password != 12345:
    password = int(input("Introduce la contraseña: "))

print("¡Acceso concedido!")
```

<a id="ejemplo-2"></a>

## Ejemplo 2: Buscador de archivos

Pide nombres de archivo hasta que el usuario escribe `salir`. Para cada nombre, construye la ruta con `pathlib` y comprueba si el archivo existe en la carpeta actual.

```python
from pathlib import Path

carpeta = Path(".")

if carpeta.exists() and carpeta.is_dir():

    nombre = ""

    while nombre != "salir":

        nombre = input("Nombre del archivo (o salir): ")

        if nombre != "salir":

            archivo = carpeta / nombre #Curso_Python/bucles/while_4.py

            if archivo.is_file():
                print("Archivo encontrado.")
                print(f"Su ruta relativa es: {archivo}")
            else:
                print("Archivo no encontrado.")

else:
    print("El directorio no existe.")

print("Buscador finalizado.")
```

<a id="ejemplo-3"></a>

## Ejemplo 3: Lectura de Excel

Lee el archivo `mazo_ingles.xlsx` con pandas y muestra las primeras 20 filas de las dos primeras columnas.

> [!NOTE]
> Requiere pandas y un motor para leer `.xlsx` (por ejemplo, `openpyxl`). El archivo `mazo_ingles.xlsx` debe estar en la misma carpeta desde la que se ejecuta el programa.

```python
from pathlib import Path
import pandas as pd

archivo = Path("mazo_ingles.xlsx")

if archivo.exists() and archivo.is_file():

    datos = pd.read_excel(archivo)

    seleccion = datos.iloc[0:20, 0:2]

    print(seleccion)

else:
    print("El archivo no existe.")
```
