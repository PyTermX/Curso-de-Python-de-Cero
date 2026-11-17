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
  <strong>Ejercicios prácticos para moverse entre carpetas desde la terminal, ejecutar scripts de Python y practicar rutas relativas.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Ejercicios-6-E53935?style=flat-square&labelColor=151515" alt="6 ejercicios">
  <img src="https://img.shields.io/badge/Tema-Terminal_y_rutas-FFC928?style=flat-square&labelColor=151515" alt="Tema: terminal y rutas">
  <img src="https://img.shields.io/badge/Lenguaje-Python-333333?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
</p>

<p align="center">
  <a href="#estructura">Estructura de carpetas</a> ·
  <a href="#ejercicios">Ejercicios</a>
</p>

# Ejercicios de navegación por carpetas en la terminal

<a id="contenido"></a>

## Contenido

- [Estructura de las carpetas para el ejemplo](#estructura)
- [Ejercicios](#ejercicios)
  - [Ejercicio 1](#ejercicio-1)
  - [Ejercicio 2](#ejercicio-2)
  - [Ejercicio 3](#ejercicio-3)
  - [Ejercicio 4](#ejercicio-4)
  - [Ejercicio 5](#ejercicio-5)
  - [Ejercicio 6](#ejercicio-6)

<a id="estructura"></a>

## Estructura de las carpetas para el ejemplo

Todos los ejercicios usan la siguiente estructura de carpetas:

```text
Escritorio
└── Carpeta_1
    └── Carpeta_2
        ├── Carpeta_2.1
        └── Carpeta_3
            ├── Carpeta_3.1
            │   └── Script_3.1.py
            └── Carpeta_3.2
                └── Script_3.2.txt
```

> [!NOTE]
> Asumimos que te encuentras en el escritorio. Abrimos una terminal desde tu escritorio.

> [!TIP]
> Opcional: en su defecto, también puedes abrir la terminal desde cualquier carpeta, tal y como se abre una terminal desde el escritorio, para comenzar directamente con el ejercicio 1.

<a id="ejercicios"></a>

## Ejercicios

<a id="ejercicio-1"></a>

### Ejercicio 1

**Movernos desde la última carpeta hasta el escritorio.**

- **Desde:** `Carpeta_3`
- **Hasta:** `Escritorio`

<a id="ejercicio-2"></a>

### Ejercicio 2

**Movernos desde el escritorio hasta la segunda carpeta directamente.**

- **Desde:** `Escritorio`
- **Hasta:** `Carpeta_2` (la segunda en la ruta)

<a id="ejercicio-3"></a>

### Ejercicio 3

**Desde el escritorio nos movemos hasta la `Carpeta_3.2`.**

- **Desde:** `Escritorio`
- **Hasta:** `Carpeta_3.2`

<a id="ejercicio-4"></a>

### Ejercicio 4

**Desde el escritorio nos movemos hasta la `Carpeta_3.1` y ejecutamos el archivo `Script_3.1.py`.**

- **Desde:** `Escritorio`
- **Hasta:** `Carpeta_3.1` (última carpeta, número 1)
- **Ejecutar:** `Script_3.1.py`

<a id="ejercicio-5"></a>

### Ejercicio 5

**En la `Carpeta_2.1` ejecutamos el archivo `archi_0.py`.** Este archivo no está en la estructura; lo añadimos para el ejercicio.

- **Desde:** `Carpeta_2`
- **Crear:** `archi_0.py`, con esta línea de código:

  ```python
  print("Código en Python!")
  ```

- **Ejecutar:** `archi_0.py`

<a id="ejercicio-6"></a>

### Ejercicio 6

**Desde la `Carpeta_3.2` movernos a la `Carpeta_2.1` y ejecutar el archivo `archi_0.py` usando rutas relativas.**

- **Desde:** `Carpeta_3.2`
- **Ejecutar:** `archi_0.py`

<!-- TODO: agregar los comandos de solución de cada ejercicio, por ejemplo dentro de <details><summary>Ver solución</summary> ... </details> -->
