# Entregable_ SEMANA 02 🚀


## Ejercicio 1 | Determinar estado de aprobación 🔥

- A. Solicitar al usuario ingresar una calificación numérica (de 0 a 100).
- B. Evaluar si está aprobada o reprobada basándose en la calificación ingresada.

```python
while True:
        try:
            nota = int(input("\nPor favor ingresa la calificación: "))

            if nota > 100 or nota < 0:
                print("Por favor ingresa una nota entre 0 y 100")
                continue

            if nota >= 60:
                print (f"\nTu nota fue {nota}, aprobado. 🥳")
            else:
                print (f"\nTu nota fue {nota}, reprobado. 🤕")
            break
        except ValueError:
            print ("\nPor favor ingresa una nota válida")
```


## Ejercicio 2 | Calcular el promedio 🤓
- A. Permitir al usuario ingresar una lista de calificaciones (separadas por comas).
- B. Calcular y mostrar el promedio de las calificaciones en la lista.

```python
while True:
    try:
        entrada = input("\nIngresa una lista de calificaciones separadas por comas (ej: 80,90,100): ")
        
        # Divide la entrada en una lista de cadenas usando la coma como separador
        lista = entrada.split(",")

        calificaciones = []  # Lista para guardar las calificaciones válidas

        # Recorre cada valor ingresado
        for valor in lista:
            nota = float(valor.strip())  # Convierte el valor a float y elimina espacios extra
            if 0 <= nota <= 100:
                calificaciones.append(nota)  # Agrega la nota si está en el rango válido
            else:
                raise ValueError("Las calificaciones deben estar entre 0 y 100. 😳")

        if calificaciones:
            # Calcula el promedio si hay calificaciones válidas
            promedio = sum(calificaciones) / len(calificaciones)
            print(f"\nEl promedio de las calificaciones es 👉 {promedio:.2f}")
            break  # Sale del bucle si todo fue correcto
        else:
            print("No ingresaste una calificación válida. 😳")
    except ValueError:
        # Mensaje si hay un error de conversión o si alguna calificación no es válida1
        print("❎ Error: Asegúrate de ingresar solo números válidos separados por comas.")
```


## Ejercicio 3 | Contar calificaciones mayores que un valor específico ➡️
- A. Solicitar al usuario un valor numérico.
- B. Contar y mostrar cuántas calificaciones en la lista son mayores que ese valor.

```python
while True:
    try:
        # Paso 1: pedir una lista de calificaciones separadas por comas
        entrada = input("\nIngresa una lista de calificaciones separadas por comas (ej: 70,85,90): ")
        lista = entrada.split(",")  # Divide la entrada en una lista
        calificaciones = []

        # Convertir y validar cada valor
        for valor in lista:
            nota = float(valor.strip())  # Elimina espacios y convierte a float
            if 0 <= nota <= 100:
                calificaciones.append(nota)
            else:
                raise ValueError("Las calificaciones deben estar entre 0 y 100. 😳")

        if not calificaciones:
            print("No ingresaste una calificación válida. 😳")
            continue

        # Paso 2: solicitar al usuario un valor de comparación
        limite = float(input("Ingresa un valor para comparar (por ejemplo, 80): "))

        # Paso 3: contar cuántas calificaciones son mayores al valor ingresado
        mayores = [n for n in calificaciones if n > limite]
        cantidad = len(mayores)

        # Mostrar resultado
        print(f"\nHay {cantidad} calificaciones mayores que {limite}.")
        break

    except ValueError:
        print("❎ Error: Verifica que los datos sean números válidos.")
```



# EJERCICIO 4 | Verificar y contar calificaciones específicas 📌
- A. Permitir al usuario ingresar una lista de calificaciones (separadas por comas) y una calificación específica.
- B. Contar y mostrar cuántas veces aparece dicha calificación en la lista.

```python
while True:
    try:
        # Paso 1: pedir al usuario una lista de calificaciones separadas por comas
        entrada = input("\nIngresa una lista de calificaciones separadas por comas (ej: 70,80,60): ")
        lista = entrada.split(",")  # Divide la entrada en elementos separados por coma
        calificaciones = []

        # Validar y convertir cada valor a número
        for valor in lista:
            nota = float(valor.strip())  # Elimina espacios y convierte a float
            if 0 <= nota <= 100:
                calificaciones.append(nota)
            else:
                raise ValueError("Las calificaciones deben estar entre 0 y 100. 😳")

        if not calificaciones:
            print("No ingresaste ninguna calificación válida. 😳")
            continue

        # Paso 2: pedir una calificación específica para buscar
        objetivo = float(input("Ingresa la calificación que deseas contar (por ejemplo, 70): "))

        # Paso 3: contar cuántas veces aparece esa calificación
        repeticiones = calificaciones.count(objetivo)

        # Mostrar el resultado
        print(f"\nLa calificación {objetivo} aparece {repeticiones} veces.")
        break

    except ValueError:
        print("❎ Error: Asegúrate de ingresar solo números válidos.")
```
