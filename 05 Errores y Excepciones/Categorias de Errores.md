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
  <strong>Guía de los tres tipos de errores en Python: sintaxis, ejecución y lógica, con un ejemplo de cada uno.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Lenguaje-Python-FFC928?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
  <img src="https://img.shields.io/badge/Tema-Tipos_de_errores-E53935?style=flat-square&labelColor=151515" alt="Tema: tipos de errores">
  <img src="https://img.shields.io/badge/Tipo-Gu%C3%ADa_de_referencia-333333?style=flat-square&labelColor=151515" alt="Tipo: guía de referencia">
</p>

<p align="center">
  <a href="#sintaxis">Sintaxis</a> ·
  <a href="#ejecucion">Ejecución</a> ·
  <a href="#logica">Lógica</a> ·
  <a href="#comparacion">Comparación</a>
</p>

# Los tres tipos de errores

<a id="sintaxis"></a>

## A. Errores de sintaxis (Syntax Errors)

Son errores que ocurren cuando escribimos código que no respeta las reglas gramaticales de Python. Es decir, Python no puede interpretar correctamente nuestras instrucciones porque existe algún problema en la forma en que están escritas.

**Ejemplo:**

```python
if 10 > 5
    print("Diez es mayor que cinco")
```

¿Puedes identificar el problema? Nos falta colocar dos puntos (`:`) al final de la condición `if`.

Python mostrará un error similar a este:

```text
SyntaxError
File "main.py", line 1
    if 10 > 5
            ^
SyntaxError: expected ':'
```

Python esperaba encontrar dos puntos al finalizar la condición.

**¿Qué debemos recordar?**

- Python detecta el problema antes de ejecutar el programa.
- El programa no comienza su ejecución normal.
- Debemos corregir la sintaxis antes de continuar.

Otros ejemplos habituales son olvidar cerrar paréntesis, escribir incorrectamente una palabra clave o utilizar una estructura sin la indentación adecuada.

<a id="ejecucion"></a>

## B. Errores de ejecución (Runtime Errors)

Estos errores aparecen cuando el código tiene una sintaxis válida, pero ocurre un problema mientras Python está ejecutando las instrucciones. En Python, estos errores se manifiestan mediante excepciones (*Exceptions*).

**Ejemplo:**

```python
numero1 = 10
numero2 = 0
resultado = numero1 / numero2
print(resultado)
```

En este caso, el código está correctamente escrito, pero estamos intentando dividir un número entre cero. Python comienza a ejecutar el programa, llega a la división y genera una excepción:

```text
ZeroDivisionError
Traceback (most recent call last):
  File "main.py", line 3, in <module>
    resultado = numero1 / numero2
ZeroDivisionError: division by zero
```

El programa comenzó a ejecutarse, pero se interrumpió al intentar realizar una división entre cero.

**¿Qué debemos recordar?**

- El programa comienza su ejecución.
- El error aparece cuando se alcanza una instrucción problemática.
- Python genera una excepción que puede interrumpir el programa si no se maneja.

Otros ejemplos son intentar convertir un texto no numérico a entero, acceder a una posición inexistente de una lista o abrir un archivo que no existe.

<a id="logica"></a>

## C. Errores de lógica (Logical Errors)

Estos son especialmente interesantes porque, a diferencia de los anteriores, Python no necesariamente muestra un mensaje de error. El programa se ejecuta correctamente desde el punto de vista de la sintaxis y las operaciones, pero el resultado no es el que esperábamos.

**Ejemplo:**

```python
precio = 100
descuento = 20
total = precio + descuento
print(f"Total a pagar: ${total}")
```

El programa muestra:

```text
Total a pagar: $120
```

¿Pero es correcto? No. Si queremos aplicar un descuento de $20 a un producto de $100, deberíamos obtener $80. El problema está en nuestra operación matemática: utilizamos una suma en lugar de una resta.

La instrucción correcta sería:

```python
total = precio - descuento
```

**¿Qué debemos recordar?**

- El programa no necesariamente genera excepciones.
- Python ejecuta las instrucciones sin detectar ningún problema técnico.
- El resultado es incorrecto porque la lógica o el planteamiento del programa tiene un error.

<a id="comparacion"></a>

## Comparación de los tres tipos de errores

| Tipo | ¿Ejecuta el programa? | ¿Genera error? |
|---|---|---|
| Sintaxis | No comienza la ejecución normal | Sí |
| Ejecución | Comienza, pero puede interrumpirse | Sí |
| Lógica | Sí, normalmente termina | No necesariamente 

# Apoya el proyecto

Si te gusta el contenido:

Suscríbete al canal para no perderte los próximos tutoriales.
Deja un comentario si tienes dudas o sugerencias.
Comparte el video con alguien que también quiera aprender programación.

Mucha suerte a todos en el camino.



|
