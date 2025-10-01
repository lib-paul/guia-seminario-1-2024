# Guia practica/teorica para SEMINARIO 1 (Python)
El proposito de esta guia es proveer conocimientos basicos/intermedios sobre <strong>Python</strong> y asimismo afinar algunos conceptos. Vamos a ir paso a paso y por cada parte de la breve teoria se van a dejar en conjunto
un seleccionado de ejercicios al final los cuales deberan ser entregados por los alumnos para la aprobación de la materia.

---
# Parte 1 ¿Programar? ¿Python?
---

## 1.1 ¿Qué es programar?

Programar es darle instrucciones a la computadora para que haga cosas por vos.  
Podés pensarlo como explicarle una receta paso a paso: vos escribís el código (las instrucciones), y la máquina lo ejecuta.  

En el proceso, esas instrucciones se "traducen" a un lenguaje que la computadora entiende, y después vemos el resultado. Ese resultado puede ser texto, imágenes, sonidos, gráficos, o cualquier combinación.  

Un programa puede ser algo muy simple (mostrar un mensaje en pantalla) o muy complejo (el sistema de Netflix, un videojuego, una red social). En todos los casos, se trata de conjuntos de instrucciones que persiguen un propósito concreto.


## 1.2 ¿Por qué Python?🐍

Existen muchísimos lenguajes de programación, pero Python se ganó un lugar especial porque es **simple de leer y escribir**. Su sintaxis se parece bastante al idioma humano, lo que lo convierte en una gran puerta de entrada para quienes recién empiezan.  

Python no solo es fácil: también es **poderoso y versátil**. Con el mismo lenguaje podés crear programas muy distintos:  
- pequeñas aplicaciones que te resuelven una tarea diaria,  
- páginas web completas,  
- análisis de datos científicos,  
- inteligencia artificial,  
- hasta videojuegos.  

Además, tiene una comunidad enorme que comparte código, librerías y tutoriales. Eso significa que si te trabás, casi siempre alguien ya tuvo el mismo problema y podés encontrar ayuda rápido.  

En resumen: Python combina lo mejor de dos mundos → **aprendizaje sencillo** para principiantes y **herramientas avanzadas** para proyectos grandes. Por eso es uno de los lenguajes más usados en el mundo hoy en día.

## 1.3 ¿Como instalar Python?

Para esta partecita voy a usar una referencia a una guia creada por mi anteriormente, en la cual se explica brevemente como instalar Python.
[Guia Django Partes 1.1 y 2.1](https://github.com/lib-paul/guia-seminario-1-2024/blob/main/README.md#11-instalaci%C3%B3n-de-requerimientos)
Yo para "codear" en Python (en estas instancias al menos) recomiendo usar VSCode con el conjunto de "Extensiones" recomendadas en esas partes de la guía. En caso de requerir mas ayuda se puede usar el apartado "Issues" de este repositorio para reportar un inconveniente
o duda 😄.

---

# Parte 2: Primeros Pasos con Datos 🚀
---

## 2.0 Mostrando resultados: la función `print()` 📝

Hasta ahora hablamos de qué es programar y por qué Python, una vez que tenemos nuestro IDE abierto y nuestro primer archivo .py preparado ¿que hacemos primero? ¿cómo hacemos para que la computadora nos diga algo? 🤔
Ahí entra en juego `print()`.

La función `print()` sirve para mostrar información en la pantalla 📺. Es como si la computadora hablara y nos devolviera un mensaje 💬.
Ejemplo básico 🤔
```python
print("Hola, mundo! 🌎")
```
Esto devuelve el mensaje, entre las comillas. Esta es una de las funciones mas utiles que existen en cualquier lenguaje, en Python se llama `print()` pero por ejemplo en JavaScript podriamos usar el conocido `console.log(). Hay que tenerla siempre en cuenta 👀.

## 2.1 Tipos de Datos 📊

En Python, todo lo que usamos tiene un tipo 🤔.
Los tipos de datos nos dicen qué clase de cosa estamos manejando y qué operaciones se pueden hacer con ella 📚. 

Algunos de los más comunes son:
```
Enteros (int) → números sin decimales: 1, 50, -200 📝
Flotantes (float) → números con decimales: 3.14, -0.5 📊
Cadenas de texto (str) → cualquier cosa entre comillas: "Hola", 'Python' 💬
Booleanos (bool) → valores lógicos: True (verdadero) o False (falso) 🔒
```

Ejemplos en acción 🎥
```python
print(10)        # entero 📝
print(3.5)       # flotante 📊
print("Hola")    # cadena de texto 💬
print(True)      # booleano 🔒
```

Cada tipo tiene sus particularidades 🤔:

    Con números podés hacer cuentas 📝
    Con textos podés unirlos, repetirlos, etc. 💬
    Con booleanos podés representar condiciones de sí/no, encendido/apagado 🔒

A diferencia de otros lenguajes, Python es dinámicamente tipado. Esto significa que no necesitas declarar el tipo de dato de una variable; el intérprete lo reconoce automáticamente, lo que hace el código más flexible y rápido de escribir 😆.

## 2.2 Variables 📦

Ahora que sabemos los tipos de datos mas relevantes para esta parte, llega la pregunta: ¿cómo los guardamos para usarlos después? 🤔
Ahí entran las variables 📦.

Una variable es como una caja con un nombre, donde podés guardar un valor 📦 (del tipo que necesites).
Cuando quieras, podés abrir la caja (leer el valor) o cambiar su contenido (reasignar el valor) 🔄.
Ejemplo 📝

```python
x = 5          # guardo el número 5 en la variable x
nombre = "Ana" # guardo el texto "Ana" en la variable nombre
print(x)       # muestra 5
print(nombre)  # muestra Ana
```
Cosas importantes a tener en cuenta:

    Se usa el signo = para asignar valores 📝
    El tipo de dato se determina automáticamente, no hace falta declararlo (Python lo hace solo como describimos antes) 🤖
    Podés reasignar una variable cuando quieras 🔄

```python
x = 10
print(x)   # en el ejemplo anterior era 5 ahora ya reasignada va a mostrar el número 10
```

💡 Una variable es simplemente una etiqueta para un valor. Te ayuda a no repetir y a darle más claridad a tu programa. Por convención, lo ideal es utilizar nombres descriptivos para las variables, en el caso de que se busque alguna su nombre pueda
decirnos que es la variable que buscamos (tanto a nosotros como a otros programadores).

---

# Parte 3: Operadores y Expresiones

---

## 3.1 ➕ Operadores Aritméticos

Los operadores aritméticos son los que usamos para hacer cuentas.  
En Python funcionan igual que en la matemática de todos los días.

| Operador | Descripción         | Ejemplo      | Resultado |
|----------|---------------------|--------------|-----------|
| `+`      | Suma                | `5 + 3`      | `8`       |
| `-`      | Resta               | `10 - 4`     | `6`       |
| `*`      | Multiplicación      | `2 * 6`      | `12`      |
| `/`      | División (decimal)  | `7 / 2`      | `3.5`     |
| `//`     | División entera     | `7 // 2`     | `3`       |
| `%`      | Módulo (resto)      | `7 % 2`      | `1`       |
| `**`     | Exponenciación      | `2 ** 3`     | `8`       |

📌 Ejemplo en código:

```python
print(10 + 3)   # suma → 13
print(7 // 2)   # división entera → 3
print(2 ** 5)   # 2 elevado a la 5 → 32
```
## 3.2 ⚖️ Operadores de Comparación

Estos sirven para comparar valores.
La respuesta siempre es True o False.

| Operador | Significado   | Ejemplo  | Resultado |
| -------- | ------------- | -------- | --------- |
| `==`     | Igual         | `5 == 5` | `True`    |
| `!=`     | Distinto      | `5 != 3` | `True`    |
| `>`      | Mayor que     | `7 > 10` | `False`   |
| `<`      | Menor que     | `4 < 9`  | `True`    |
| `>=`     | Mayor o igual | `5 >= 5` | `True`    |
| `<=`     | Menor o igual | `3 <= 2` | `False`   |

📌 Ejemplo en código:
```python
print(10 > 3)   # True
print(5 == 2)   # False📌 Ejemplo en código:
```

Un pequeño dato a parte aca, notamos que el `=` no esta presente 🤔, esto es debido a que el `=` es el operador de asignacíón y el `==` el operador de igualdad. Esto quiere decir que uno asigna un "algo" a una variable y el otro compara si 
los datos que estan en sus extremos son iguales devolviendo un `TRUE` o `FALSE`.

## 3.3 🔗 Operadores Lógicos

Los usamos para combinar condiciones.
Pensalo como reglas de sí/no.

| Operador | Descripción                     | Ejemplo          | Resultado |
| -------- | ------------------------------- | ---------------- | --------- |
| `and`    | Y lógico (ambos deben ser True) | `True and False` | `False`   |
| `or`     | O lógico (con uno True alcanza) | `True or False`  | `True`    |
| `not`    | Negación (invierte el valor)    | `not True`       | `False`   |

📌 Ejemplo en código:
```python
edad = 20
print(edad > 18 and edad < 30)  # True si está entre 18 y 30
print(edad < 18 or edad > 65)   # True si está fuera de ese rango
```

## 3.4 🧮 Expresiones

Una expresión es cualquier combinación de valores, variables y operadores que produce un resultado.

📌 Ejemplo en código:
```python
x = 5
y = 3
resultado = (x * 2) + y
print(resultado)   # muestra 13
```
## 3.5 ⌨️ Entrada de Datos con `input()`

Hasta ahora mostramos cosas con `print()`.
Pero, ¿cómo hacemos para que el usuario nos dé información? (Ingresa por la terminal/consola)

👉 Usamos `input()`.

`input()` espera que el usuario escriba algo en la consola y lo guarda como un texto (str).
Después podemos asignarlo a una variable para usarlo.

📌 Ejemplo:
```python
nombre = input("¿Cómo te llamás? ")
print("Hola,", nombre)
```
🔎 Si escribís `Ana` cuando lo pide, la salida será:
```
¿Cómo te llamás? Ana
Hola, Ana
```

⚠️ Importante: todo lo que devuelve ```input()``` es un texto.
Si necesitás un número, hay que convertirlo (pero eso lo vemos más adelante con casting 😉).

---
# Parte 4: Estructuras de Control
---

Las estructuras de control son las que nos permiten que el programa tome decisiones o repita acciones.
Acá es donde el código empieza a volverse más “inteligente”.


## 4.1 🔀 Condicionales (if, elif, else)

Con los condicionales podemos decirle a Python:
👉 “Si pasa tal cosa, hacé esto. Si no, hacé otra cosa". Un `if` es como un `¿Si?` un `elif` es como un `¿Si no, puede ser?` y el ultimo el `else` es como un `¿Si no?` o `De øtra forma`. El ultimo else se evalua si todas las condiciones anteriores no se
cumplieron. El primer condicional es el "if" en el caso de que haya que evaluar mas expresiones contenidas a la original se utiliza el "elseif" y la condición final cuando ninguna se cumplio "else".

📌 Ejemplo básico:
```python
x = 5

if x > 10:
    print("x es mayor que 10")
elif x == 5:
    print("x es igual a 5")
else:
    print("x es menor que 10 y no es 5")
```

## 4.2 🔁 Ciclos

Los ciclos sirven para repetir instrucciones sin tener que escribirlas muchas veces.

while → mientras se cumpla una condición:
```python
x = 0
while x < 5:
    print(x)
    x += 1
```
👉 Este código imprime los números del 0 al 4.

for → recorrer una secuencia de valores:
```python
for letra in "Python":
    print(letra)
```
👉 Esto imprime cada letra de la palabra Python en una línea distinta.

💡 Los ciclos son muy poderosos. Te permiten recorrer listas (mas adelante), repetir cálculos, o pedirle al usuario datos hasta que cumpla cierta condición.

## 4.3 Casting (conversión de tipos)

Cuando pedimos datos con `input()`, **todo lo que escribe el usuario llega como texto (string)**.  
Pero muchas veces necesitamos trabajar con números para hacer cuentas.  

Ahí aparece el **casting**: convertir un dato de un tipo a otro.  

En Python se hace con funciones ya preparadas, por ejemplo:  

- `int("5")` → convierte el texto `"5"` en el número `5` (entero).  
- `float("3.14")` → convierte el texto `"3.14"` en el número `3.14` (decimal).  
- `str(100)` → convierte el número `100` en el texto `"100"`.  

Ejemplo práctico:  

```python
edad = input("¿Cuántos años tenés? ")   # llega como texto
edad = int(edad)                        # lo convertimos a número
print("El año que viene tendrás:", edad + 1)
``` 
Tambien se puede hacer de la siguiente forma:

```python
edad = int(input("¿Cuántos años tenés? ")  #Anidando el casting
```

---
# 📝 Ejercicios Progresivos – Python Básico (Partes 1 a 4)
---

¡Llego lo importante! La ejercitación, cada uno de estos ejercicios tiene que ser entregado en un archivo .py por separado, por ejemplo, si hacemos el ejercicio 1 el nombre del archivo va a ser `1.1.py` si hacemos el ejercicio 3 de la parte 2 el nombre
va a ser `2.3.py` y asi con todos.

## Parte 1 – Introducción a la programación y Python

1. Imprimí en pantalla `"Hola, mundo!"`.  
2. Imprimí tu nombre y tu edad en dos líneas diferentes usando `print()`.  
3. Escribí un comentario en el código que explique qué hace un `print()`.  

---

## Parte 2 – Tipos de datos y variables

4. Guardá tu nombre en una variable y mostralo en pantalla.  
5. Creá dos variables con números enteros y mostrá su suma.  
6. Creá una variable con un número entero, otra con un número decimal y otra con texto. Mostralas juntas en un `print()`.  
7. Reasigná el valor de una variable y mostrá la diferencia en pantalla.  
8. Guardá un texto en una variable y mostrala en pantalla.  
9. Pedí al usuario su nombre usando `input()` y mostrale un saludo personalizado.  
10. Pedí al usuario su ciudad y mostrá `"Vives en [ciudad]"`.  

---

## Parte 3 – Operadores y entrada de datos

11. Usá variables para calcular el área de un rectángulo (base × altura) y mostrala.  
12. Mostrá el resultado de `7 + 3`, `7 - 3`, `7 * 3` y `7 / 3` usando `print()`.  
13. Calculá el cuadrado de un número usando `**`.  
14. Calculá el resto de dividir 25 entre 4 con `%`.  
15. Pedí dos números al usuario y mostrales la suma y la resta.  
16. Pedí al usuario su edad, convertí el dato a entero y mostrale `"Tenés [edad] años"`.  
17. Pedí dos números y decí si el primero es mayor, menor o igual al segundo usando operadores de comparación.  
18. Pedí un número y decí si es mayor, menor o igual a 10 usando `if`, `elif` y `else`.  

---

## Parte 4 – Estructuras de control

19. Pedí un número y decí si es positivo, negativo o cero.  
20. Pedí una edad y decí si la persona es mayor o menor de edad.  
21. Pedí una palabra y decí si tiene más de 5 letras o no.  
22. Pedí un número y mostrale si es par o impar.  
23. Usá un `while` para contar del 0 al 4.  
24. Usá un `while` para pedirle al usuario una palabra hasta que escriba `"salir"`.  
25. Usá un `for` para mostrar cada letra de la palabra `"Python"`.  
26. Pedí una palabra al usuario y usá un `for` para mostrar cada letra en una línea distinta.  
27. Pedí un número al usuario y usá un `while` para imprimir todos los números menores a ese número.  
28. Pedí al usuario que ingrese `"si"` o `"no"` hasta que lo haga correctamente (validación con `while`).  
29. Pedí dos números y decí si **el primero es divisible por el segundo** usando `%`.  
30. Pedí al usuario un número y decí si está entre 1 y 10 usando `and` en un `if`.  











