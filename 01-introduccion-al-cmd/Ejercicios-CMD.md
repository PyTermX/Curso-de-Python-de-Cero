# Estructura de las Carpetas para el Ejemplo

```q
Escritorio
└── Carpeta_1
    └── Carpeta_2
		|    └── Carpeta_2.1
        └── Carpeta_3 
            ├── Carpeta_3.1 
            │   └── Script_3.1.py
            └── Carpeta_3.2 
                └── Script_3.2.txt
```

**NOTA:** Asumimos que te encuentras en el escritorio. Abrimos una terminal desde tu escritorio. 
**Opcional:** En su defecto, también puedes abrir la terminal desde cualquier carpeta, tal y como se abre una terminal desde el escritorio, para comenzar directamente con el ejercicio 1.

## Ejercicio 1
**Movernos desde la última carpeta hasta el escritorio.**

- **Desde:** `Carpeta_3`
- **Hasta:** `Escritorio`

## Ejercicio 2

**Movernos desde el escritorio hasta la segunda carpeta directamente.**

- **Desde:** `Escritorio`
- **Hasta:** `Carpeta_2` (la segunda en la ruta)

## Ejercicio 3

**Desde el escritorio nos movemos hasta la Carpeta_3.2.**

- **Desde:** `Escritorio`
- **Hasta:** `Carpeta_3.2`

## Ejercicio 4

**Desde el escritorio nos movemos hasta la Carpeta_3.1 y ejecutamos el archivo Script_3.1.py.**

- **Desde:** `Escritorio`
- **Hasta:** `Carpeta_3.1` (última carpeta, número 1)
- **Ejecutar:** `Script_3.1.py`

## Ejercicio 5

**En la Carpeta_2.1 ejecutamos el archivo archi_0.py,** (**no está** en la estructura, lo añadimos para el ejercicio).

- **Desde:** `Carpeta_2
- **Creamos archi_0.py** - Línea de código que debe tener: `print("Código en Python!")`
- **Ejecutar:** `archi_0.py` 

## **Ejercicio 6**

**Desde la Carpeta_3.2 moverse a la carpeta a la Carpeta_2.1 y ejecutar el archivo archi_0.py usando rutas relativas**

- **Desde:** `Carpeta_3.2`
- **Ejecutar:** `archi_0.py`
