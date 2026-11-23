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
  <strong>Guía del ciclo while en Python: estructura, evaluación de la condición, diferencias con if y cómo evitar ciclos infinitos.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Lenguaje-Python-FFC928?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
  <img src="https://img.shields.io/badge/Tema-Ciclo_while-E53935?style=flat-square&labelColor=151515" alt="Tema: ciclo while">
  <img src="https://img.shields.io/badge/Tipo-Gu%C3%ADa_de_estudio-333333?style=flat-square&labelColor=151515" alt="Tipo: guía de estudio">
</p>

<p align="center">
  <a href="#estructura">Estructura</a> ·
  <a href="#condicion">Condición</a> ·
  <a href="#evaluacion">Evaluación</a> ·
  <a href="#cero-veces">Cero veces</a> ·
  <a href="#while-vs-if">while e if</a> ·
  <a href="#actualizacion">Actualización</a>
</p>

# Ciclo `while` en Python

El ciclo `while` es una estructura de control que permite repetir un bloque de instrucciones mientras una determinada condición sea verdadera (`True`).

Su idea fundamental puede resumirse así:

> "Mientras esta condición sea verdadera, continúa ejecutando estas instrucciones."

A diferencia de una estructura `if`, que normalmente evalúa una condición para decidir si ejecuta un bloque una vez, `while` utiliza esa condición para decidir si debe continuar repitiendo el bloque.

## Contenido

- [1. Estructura básica](#estructura)
- [2. Lo más importante: while depende de una condición](#condicion)
- [3. Cómo funciona la evaluación](#evaluacion)
- [4. El while puede ejecutarse cero veces](#cero-veces)
- [5. Qué hace diferente al while de if](#while-vs-if)
- [6. La actualización de la condición](#actualizacion)

<a id="estructura"></a>

## 1. Estructura básica

La sintaxis general es:

```python
while condicion:
    instrucciones
```

Podemos identificar tres elementos:

```text
while → palabra reservada que inicia el ciclo

condicion → expresión que produce True o False

instrucciones → bloque que se repetirá mientras la condición sea True
```

Por ejemplo:

```python
contador = 1
while contador <= 5:
    print(contador)
    contador += 1
```

Aquí ocurre algo fundamental:

```text
contador = 1
      ↓
¿contador <= 5?
      ↓
    True
      ↓
ejecutar bloque
      ↓
contador += 1
      ↓
volver a evaluar condición
      ↓
¿contador <= 5?
```

El ciclo continúa hasta que la condición deja de cumplirse.

<a id="condicion"></a>

## 2. Lo más importante: while depende de una condición

Esta es probablemente la idea que debes dominar antes de avanzar:

> [!IMPORTANT]
> Un `while` no está definido por la cantidad de veces que se ejecutará, sino por una condición que determina cuándo debe dejar de ejecutarse.

Por eso:

```python
while x < 10:
```

no significa "Ejecuta esto 10 veces". Significa "Ejecuta esto mientras `x` sea menor que 10". Esto es una diferencia conceptual muy importante.

<a id="evaluacion"></a>

## 3. Cómo funciona la evaluación

Supongamos:

```python
contador = 1
while contador <= 3:
    print(contador)
    contador += 1
```

Python realiza aproximadamente este proceso.

**Primera evaluación**

```text
contador <= 3
1 <= 3
True
```

Se ejecuta el cuerpo:

```python
print(contador)
contador += 1
```

Ahora:

```text
contador = 2
```

Python regresa a la condición.

**Segunda evaluación**

```text
2 <= 3
True
```

Se ejecuta nuevamente el bloque. Ahora:

```text
contador = 3
```

Se vuelve a evaluar:

```text
3 <= 3
True
```

Se ejecuta nuevamente. Ahora:

```text
contador = 4
```

Y nuevamente:

```text
4 <= 3
False
```

Esta representación es mucho más importante que memorizar la sintaxis.

<a id="cero-veces"></a>

## 4. El while puede ejecutarse cero veces

Este es otro concepto fundamental. Observa:

```python
contador = 10
while contador < 5:
    print(contador)
```

La condición se evalúa inmediatamente:

```text
10 < 5
False
```

Por lo tanto, el cuerpo nunca se ejecuta. Esto significa que un ciclo `while` puede ejecutarse cero, una o muchas veces.

<a id="while-vs-if"></a>

## 5. Qué hace diferente al while de if

Observa:

```python
if condicion:
    instrucciones
```

y:

```python
while condicion:
    instrucciones
```

La diferencia fundamental es:

**`if`** evalúa:

```text
condición → bloque → continúa
```

**`while`** evalúa:

```text
condición → bloque → condición → bloque → condición...
```

Por ejemplo:

```python
x = 1
if x < 5:
    print(x)
```

El `print()` ocurre como máximo una vez. Mientras que:

```python
x = 1
while x < 5:
    print(x)
    x += 1
```

el `print()` puede ejecutarse varias veces. Podríamos decir: `if` controla una decisión; `while` controla una repetición condicionada.

<a id="actualizacion"></a>

## 6. La actualización de la condición

Aquí aparece uno de los errores más importantes al comenzar a estudiar `while`. Considera:

```python
contador = 1
while contador <= 5:
    print(contador)
```

¿Qué ocurre? La condición comienza siendo:

```text
1 <= 5
True
```

Se imprime:

```text
1
```

Pero `contador` nunca cambia. Por lo tanto, la siguiente evaluación vuelve a ser:

```text
1 <= 5
True
```

Y nuevamente:

```text
1 <= 5
True
```

Y nuevamente... El ciclo nunca alcanza una condición falsa. Esto produce un *infinite loop*, es decir, un ciclo infinito.

> [!WARNING]
> Si ejecutas este ejemplo, el programa no termina por sí solo. Para detenerlo en la terminal usa `Ctrl + C`.

Por eso normalmente necesitamos que dentro del ciclo exista algún mecanismo que permita que la condición eventualmente cambie. Por ejemplo:

```python
contador += 1
```

# Apoya el proyecto

Si te gusta el contenido:

Suscríbete al canal para no perderte los próximos tutoriales.
Deja un comentario si tienes dudas o sugerencias.
Comparte el video con alguien que también quiera aprender programación.

Mucha suerte a todos en el camino.
