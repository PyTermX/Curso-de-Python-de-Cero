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
  <strong>Soluciones propuestas en Python a los ejercicios sobre sentencias if: tareas, inicio de sesión, descuentos y registro de usuarios.</strong>
</p>

<!-- BADGES: edita el texto entre las barras (Etiqueta-Mensaje-Color). Guion bajo = espacio. -->
<p align="center">
  <img src="https://img.shields.io/badge/Lenguaje-Python-FFC928?style=flat-square&labelColor=151515" alt="Lenguaje: Python">
  <img src="https://img.shields.io/badge/Tema-Sentencias_if-E53935?style=flat-square&labelColor=151515" alt="Tema: sentencias if">
  <img src="https://img.shields.io/badge/Soluciones-4-333333?style=flat-square&labelColor=151515" alt="Soluciones: 4">
</p>

<p align="center">
  <a href="#solucion-1">Tareas pendientes</a> ·
  <a href="#solucion-2">Inicio de sesión</a> ·
  <a href="#solucion-3">Descuentos</a> ·
  <a href="#solucion-4">Registro de usuarios</a>
</p>

# Soluciones: ejercicios sobre sentencias if

Posibles soluciones a los ejercicios sobre sentencias `if`, `elif` y `else`.

> [!NOTE]
> Las soluciones son propuestas, no tienen que ser exactamente iguales a las tuyas. Lo importante es que el programa entregue lo que pide el ejercicio.

<a id="solucion-1"></a>

## 1. Lista de tareas pendientes

```python
tareas = ["Estudiar Python", "Hacer ejercicio", "Leer un libro"]

nueva_tarea = input("Ingresa una nueva tarea: ")

if nueva_tarea == "":
    print("Error: La tarea no puede estar vacía.")

elif nueva_tarea in tareas:
    print("Esta tarea ya existe.")

else:
    tareas.append(nueva_tarea)
    print("Tarea agregada correctamente.")

print("\nLista de tareas:")

if len(tareas) > 0:
    for tarea in tareas:
        print("-", tarea)

else:
    print("No tienes tareas pendientes.")
```

<a id="solucion-2"></a>

## 2. Sistema de inicio de sesión

```python
usuario_registrado = "admin"
contrasena_registrada = "python123"

usuario = input("Usuario: ")
contrasena = input("Contraseña: ")

if usuario == "" or contrasena == "":
    print("Error: Completa todos los campos.")

elif usuario == usuario_registrado and contrasena == contrasena_registrada:
    print("¡Bienvenido! Acceso concedido.")

elif usuario != usuario_registrado:
    print("Error: El usuario no existe.")

else:
    print("Error: Contraseña incorrecta.")
```

<a id="solucion-3"></a>

## 3. Sistema de descuentos en una tienda

```python
compra = input("Ingresa el importe de tu compra: ")

if compra.replace(".", "", 1).isdigit():

    compra = float(compra)

    if compra <= 0:
        print("Error: El importe debe ser mayor a cero.")

    elif compra >= 2000:
        descuento = 0.15

    elif compra >= 1000:
        descuento = 0.10

    elif compra >= 500:
        descuento = 0.05

    else:
        descuento = 0

    if compra > 0:
        total = compra - (compra * descuento)

        print(f"Descuento: {descuento * 100}%")
        print(f"Total a pagar: ${total:.2f}")

else:
    print("Error: Ingresa una cantidad numérica.")
```

Descuentos que aplica esta solución:

| Importe de la compra | Descuento |
|---|---:|
| Menos de 500 | 0% |
| Desde 500 | 5% |
| Desde 1000 | 10% |
| Desde 2000 | 15% |

<a id="solucion-4"></a>

## 4. Validador de registro de usuarios

```python
usuario = input("Nombre de usuario: ")
correo = input("Correo electrónico: ")
contrasena = input("Contraseña: ")
confirmacion = input("Confirma tu contraseña: ")
edad = input("Edad: ")

if usuario == "" or correo == "" or contrasena == "" or edad == "":
    print("Error: Hay campos vacíos.")

elif len(usuario) < 5:
    print("Error: El usuario necesita al menos 5 caracteres.")

elif "@" not in correo or "." not in correo:
    print("Error: El correo no es válido.")

elif len(contrasena) < 8:
    print("Error: La contraseña necesita 8 caracteres.")

elif contrasena != confirmacion:
    print("Error: Las contraseñas no coinciden.")

elif not edad.isdigit():
    print("Error: La edad debe ser numérica.")

elif int(edad) < 18:
    print("Error: Debes tener al menos 18 años.")

elif int(edad) > 120:
    print("Error: La edad no es válida.")

else:
    print("¡Registro completado correctamente!")
```

Validaciones que aplica esta solución, en orden:

1. Campos vacíos.
2. Usuario de al menos 5 caracteres.
3. Correo con `@` y `.`.
4. Contraseña de al menos 8 caracteres.
5. Contraseña y confirmación iguales.
6. Edad numérica, de al menos 18 y no mayor a 120.
