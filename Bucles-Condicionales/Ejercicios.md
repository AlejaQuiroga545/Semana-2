# Ejercicio 1: Clasificador de números ↔️

Escribe un programa que pida al usuario un número entero y determine si es positivo, negativo o cero.

```python
import random
import time

# Ejercicio 1 | Clasificador de números

while True:
    try:
        numero = int(input("Por favor ingresa un número entero: "))
        if numero > 0:
            print("\nEs un número positivo ➕")
        elif numero < 0:
            print("\nEs un número negativo ➖")
        else:
            print("\nTu número es igual a 0")
        break  # Sale del while si todo fue bien
    except ValueError:
        print("\nNo es un número válido 🤕, intenta nuevamente")
time.sleep(2)
```

# Ejercicio 2: ✅ Aprobado o ❎ Reprobado 

Crea un programa que reciba la calificación de un estudiante (0 a 100) e indique si está aprobado (60 o más) o reprobado (menos de 60).

```python
# Ejercicio 2 | Calificación de estudiante

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
time.sleep(2)
```

# Ejercicio 3: Tabla de multiplicar ✳️

Escribe un programa que muestre la tabla de multiplicar de un número ingresado por el usuario (del 1 al 10) usando un bucle for.

```python
# Ejercicio 3 | Tablas de multiplicar

while True:
    try:
       numeroTab = int(input("\nPor favor ingresa un número para saber su tabla de multiplicar: "))
       break
    except ValueError:
        print ("\nNo es un número válido 🤕, intenta nuevamente")

for i in range (1, 11):
    resultado = numeroTab * i
    print (f"{numeroTab} * {i} = {resultado:.0f}")
time.sleep(2)
```

# Ejercicio 4: Contador regresivo ⌛

Crea un programa que pida un número positivo al usuario y haga una cuenta regresiva desde ese número hasta 0 usando un bucle while.

```python
# Ejercicio 4 | Contador regresivo

while True:
    try:
        cuenta = int(input("\nPor favor digita un número positivo: "))
        
        if cuenta <= 0:
            print ("El número debe ser positivo, inténtalo nuevamente")
            continue

        while cuenta >= 0:
          print (cuenta)
          cuenta -=1
        break

    except ValueError:
        print ("No es un número válido 🤕, intenta nuevamente")
time.sleep(2)
```

# Ejercicio 5: Adivina el número 👀

Crea un programa que genere un número aleatorio entre 1 y 10, y le pida al usuario que lo adivine. El programa debe indicar si el número ingresado es mayor, menor o correcto. El usuario tiene hasta 3 intentos.

```python
# Ejercicio 5 | Adivina el número

numeroAlt = random.randint(1, 10)

intentos = 3

while True:
    try:
        number = int(input(f"\nTienes {intentos} intentos, adivina el número (del 1 a 10) 💡: "))

        if number > numeroAlt:
            print ("El número es menor 👀")

        elif number < numeroAlt:
            print ("El número es mayor 👀")

        else:
            print (f"\n¡Adivinaste! 🥳, el número es {numeroAlt}.")
            break

        intentos -=1

        if intentos ==0:
           print (f"\nLo sentimos, te quedaste sin intentos 🤕. El número es: {numeroAlt}.")
           break
           
    except ValueError:
        print ("Ingresa un número válido entre 1 y 10")
```
