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
  <strong>Respuestas a los ejercicios de navegación por carpetas en la terminal, con las alternativas de cada solución.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Respuestas-6_ejercicios-E53935?style=flat-square&labelColor=151515" alt="Respuestas a 6 ejercicios">
  <img src="https://img.shields.io/badge/Tema-Terminal_y_rutas-FFC928?style=flat-square&labelColor=151515" alt="Tema: terminal y rutas">
  <img src="https://img.shields.io/badge/Comandos-Windows-333333?style=flat-square&labelColor=151515" alt="Comandos de Windows">
</p>

<p align="center">
  <a href="#ejercicio-1">Ejercicio 1</a> ·
  <a href="#ejercicio-2">Ejercicio 2</a> ·
  <a href="#ejercicio-3">Ejercicio 3</a> ·
  <a href="#ejercicio-4">Ejercicio 4</a> ·
  <a href="#ejercicio-5">Ejercicio 5</a> ·
  <a href="#ejercicio-6">Ejercicio 6</a>
</p>

# Respuestas a los ejercicios

> [!NOTE]
> Los comandos usan la sintaxis de Windows: rutas con `\` y el lanzador `py` para ejecutar scripts de Python.

## Contenido

- [Ejercicio 1](#ejercicio-1)
- [Ejercicio 2](#ejercicio-2)
- [Ejercicio 3](#ejercicio-3)
- [Ejercicio 4](#ejercicio-4)
- [Ejercicio 5](#ejercicio-5)
- [Ejercicio 6](#ejercicio-6)

<a id="ejercicio-1"></a>

## Ejercicio 1 - Respuesta

**Opción 1: paso a paso**

```bat
cd ..
cd ..
cd ..
```

**Opción 2: en un solo comando**

```bat
cd ..\..\..
```

<a id="ejercicio-2"></a>

## Ejercicio 2 - Respuesta

```bat
cd Carpeta_1\Carpeta_2
```

<a id="ejercicio-3"></a>

## Ejercicio 3 - Respuesta

```bat
cd Carpeta_1\Carpeta_2\Carpeta_3\Carpeta_3.2
```

<a id="ejercicio-4"></a>

## Ejercicio 4 - Respuesta

**Opción 1: entrar a la carpeta y ejecutar**

```bat
cd Carpeta_1\Carpeta_2\Carpeta_3\Carpeta_3.1
py Script_3.1.py
```

**Opción 2: en un solo comando**

```bat
py Carpeta_1\Carpeta_2\Carpeta_3\Carpeta_3.1\Script_3.1.py
```

<a id="ejercicio-5"></a>

## Ejercicio 5 - Respuesta

Desde la `Carpeta_2.1` escribimos:

**Opción 1: con `copy con`**

```bat
copy con archi_0.py
print("Código en Python!")
py archi_0.py
```

> [!NOTE]
> Con `copy con`, después de escribir la línea de código presiona `Ctrl+Z` y luego `Enter` para guardar el archivo. Solo entonces ejecuta `py archi_0.py`.

**Opción 2: con `echo`**

```bat
echo print("Código en Python!") > archi_0.py
py archi_0.py
```

<a id="ejercicio-6"></a>

## Ejercicio 6 - Respuesta

Desde la `Carpeta_3.2`:

**Opción 1: entrar a la carpeta y ejecutar**

```bat
cd ..\..\Carpeta_2.1
py archi_0.py
```

**Opción 2: en un solo comando**

```bat
py ..\..\Carpeta_2.1\archi_0.py
```

# Apoya el proyecto

Si te gusta el contenido:

Suscríbete al canal para no perderte los próximos tutoriales.
Deja un comentario si tienes dudas o sugerencias.
Comparte el video con alguien que también quiera aprender programación.

Mucha suerte a todos en el camino.
