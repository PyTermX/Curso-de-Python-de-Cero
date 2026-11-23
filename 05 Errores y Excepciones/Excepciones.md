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
  <strong>Guía de referencia sobre excepciones en Python: qué son y cómo reconocer las más habituales si estás comenzando.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Lenguaje-Python-FFC928?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
  <img src="https://img.shields.io/badge/Tema-Excepciones-E53935?style=flat-square&labelColor=151515" alt="Tema: excepciones">
  <img src="https://img.shields.io/badge/Tipo-Gu%C3%ADa_de_referencia-333333?style=flat-square&labelColor=151515" alt="Tipo: guía de referencia">
</p>

<p align="center">
  <a href="#que-son">Qué son las excepciones</a> ·
  <a href="#tabla-resumen">Tabla resumen</a>
</p>

# Excepciones en Python

<a id="que-son"></a>

## Qué son las excepciones

Las excepciones son mecanismos que Python utiliza para representar y comunicar situaciones excepcionales durante la ejecución. Por eso, están principalmente asociadas con los errores de ejecución.

> [!NOTE]
> No todos los errores de ejecución tienen que ser necesariamente excepciones provocadas por una operación incorrecta del programador. También podemos generar excepciones intencionalmente, por ejemplo, para validar datos.

Python cuenta con numerosas excepciones incorporadas (*Built-in Exceptions*). No necesitas aprenderlas todas de memoria, pero sí reconocer las más habituales.

<a id="tabla-resumen"></a>

## Tabla resumen: cómo reconocer las excepciones

Usa esta tabla como referencia mientras aprendes Python.

| Excepción | ¿Cuándo ocurre? |
|---|---|
| `ZeroDivisionError` | División entre cero. |
| `TypeError` | Operación con tipos incompatibles. |
| `ValueError` | Valor no válido para una operación. |
| `NameError` | Nombre o variable no definido. |
| `IndexError` | Índice fuera de rango. |
| `KeyError` | Clave inexistente en un diccionario. |
| `AttributeError` | Atributo o método inexistente. |
| `FileNotFoundError` | Archivo o ruta no encontrada. |
| `ImportError` | Error al importar un módulo o nombre. |
| `ModuleNotFoundError` | No se encuentra el módulo que intentamos importar. |

# Apoya el proyecto

Si te gusta el contenido:

Suscríbete al canal para no perderte los próximos tutoriales.
Deja un comentario si tienes dudas o sugerencias.
Comparte el video con alguien que también quiera aprender programación.

Mucha suerte a todos en el camino.
