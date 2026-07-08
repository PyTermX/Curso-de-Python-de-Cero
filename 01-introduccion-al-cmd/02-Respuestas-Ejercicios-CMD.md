# Respuestas a los Ejercicios

##### **Ejercicio 1 - Respuesta:**

```q
cd ..
cd ..
cd ..

---------------------------------------- 

cd ..\..\..
```

##### **Ejercicio 2 - Respuesta:**

```q
cd Carpeta_1\Carpeta_2
```

##### **Ejercicio 3 - Respuesta:**

```q
cd Carpeta_1\Carpeta_2\Carpeta_3\Carpeta_3.2
```

##### **Ejercicio 4 - Respuesta:**

```q
cd Carpeta_1\Carpeta_2\Carpeta_3\Carpeta_3.1
py Script_3.1.py

----------------------------------------

py Carpeta_1\Carpeta_2\Carpeta_3\Carpeta_3.1\Script_3.1
```

##### **Ejercicio 5 - Respuesta:**

```q
# Desde la carpeta_2.1 escribimos: 
copy con archi_0.py
print("Código en Python!")
py archi_0.py

----------------------------------------

echo print("Código en Python!") > archi_0.py
py archi_0.py
```

##### **Ejercicio 6 - Respuesta:**

```q
# Desde la Carpeta_3.2
cd ..\..\Carpeta_2.1
py archi_0.py

----------------------------------------
py ..\..\Carpeta_2.1\archi_0.py

```

