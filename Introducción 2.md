# 🧩 Parte 5: Funciones – tus propias herramientas

Hasta ahora escribimos programas donde las instrucciones se ejecutaban una detrás de otra, y si queríamos repetir algo, teníamos que copiarlo o escribirlo otra vez.  
Eso no solo es incómodo, sino que además hace que el código sea más difícil de mantener y entender.

Ahí es donde entran las **funciones**, una de las partes más poderosas y útiles de cualquier lenguaje de programación.  
En Python, las funciones nos permiten **organizar el código**, **reutilizarlo** y **hacerlo más claro**.

---

## 🔹 5.1 ¿Qué es una función?

Una función es un bloque de código con un **nombre** que ejecuta una tarea específica.  
Podés **definirla una vez** y luego **usarla (o “llamarla”) todas las veces que quieras**.

En Python se define una función con la palabra clave `def` (de “define”).

```python
def saludar():
    print("Hola desde una función!")

saludar()  # Llamamos a la función
```

🔸 Lo que sucede:
1. La palabra `def` indica que estamos creando una función.
2. `saludar` es el nombre que le damos (podés elegir el que quieras, pero sin espacios ni acentos).
3. Los paréntesis `()` indican que es una función, incluso si no recibe datos.
4. Todo el código dentro del bloque (indentado) **solo se ejecuta cuando la función es llamada**.

---

## 🔹 5.2 Parámetros: dar datos a una función

Las funciones pueden recibir información para trabajar con ella.  
Esos datos se llaman **parámetros**.

```python
def saludar_persona(nombre):
    print("Hola,", nombre, "!")

saludar_persona("Ana")
saludar_persona("Carlos")
```

📘 Explicación:
- `nombre` es un **parámetro**.
- Cuando llamamos a la función, le pasamos un **argumento** (por ejemplo, `"Ana"`).
- Dentro de la función, el parámetro se comporta como una variable.

---

## 🔹 5.3 Múltiples parámetros

Podemos pasar más de un valor, separados por comas.

```python
def sumar(a, b):
    print("La suma es:", a + b)

sumar(3, 5)
sumar(10, -2)
```

💡 El orden en el que pasás los argumentos **debe coincidir** con el orden de los parámetros.

---

## 🔹 5.4 Devolver valores con `return`

Hasta ahora, las funciones mostraban resultados con `print()`.  
Pero a veces necesitamos que la función **devuelva un valor** para seguir trabajando con él.

```python
def sumar(a, b):
    resultado = a + b
    return resultado

total = sumar(5, 3)
print("El resultado es:", total)
```

📘 `return`:
- Devuelve un valor al código que llamó a la función.
- Termina inmediatamente la ejecución de la función.
- Podés guardar ese valor en una variable, o usarlo directamente.

---

## 🔹 5.5 Funciones con entrada del usuario

También podemos combinar funciones con `input()` y `casting` para pedir datos al usuario:

```python
def pedir_numero():
    numero = int(input("Ingresá un número: "))
    return numero

x = pedir_numero()
print("Ingresaste:", x)
```

💬 Acá usamos `int()` para convertir el texto que ingresa el usuario a número entero.

---

## 🔹 5.6 Funciones con condicionales

Las funciones pueden incluir estructuras de control como `if`, `for`, `while`…  
No hay límites: dentro de una función podés usar todo lo que aprendiste.

```python
def mayor_que_diez(num):
    if num > 10:
        print("El número es mayor que 10")
    else:
        print("El número es 10 o menor")

valor = int(input("Ingresá un número: "))
mayor_que_diez(valor)
```

---

## 🔹 5.7 Funciones que llaman a otras funciones

Una función puede usar o llamar a otra función.  
Esto ayuda a dividir tareas en pasos más chicos y claros.

```python
def pedir_numero():
    return int(input("Ingresá un número: "))

def mostrar_doble():
    n = pedir_numero()
    print("El doble es:", n * 2)

mostrar_doble()
```

📘 Ventaja: si más adelante querés cambiar cómo se pide el número, solo cambiás **una función**, y todo el programa se actualiza.

---

## 🔹 5.8 Buenas prácticas

- Usá **nombres descriptivos** para las funciones: `calcular_total()`, `mostrar_menu()`, etc.  
- Evitá nombres genéricos como `funcion1()` o `hacer_algo()`.
- No hagas funciones gigantes: cada una debería cumplir **una sola tarea clara**.
- Comentá lo que hace la función si no es obvio.

---

# 💪 Ejercicios – Parte 5: Funciones

## Nivel 1 – Fundamentos

1. Crear una función `saludar()` que imprima “¡Hola mundo!”.  
2. Crear una función `presentarse()` que pida tu nombre y muestre un saludo personalizado.  
3. Escribir una función `mostrar_doble()` que reciba un número y muestre su doble.  
4. Crear una función `sumar_dos_numeros(a, b)` que muestre la suma de ambos.  
5. Crear una función `restar(a, b)` que muestre la resta.

---

## Nivel 2 – Con retorno

6. Crear una función `multiplicar(a, b)` que **devuelva** el producto. Mostrar el resultado fuera de la función.  
7. Escribir una función `promedio(a, b, c)` que devuelva el promedio de tres números.  
8. Crear una función `es_par(numero)` que devuelva `True` si es par, `False` si es impar.  
9. Escribir una función `es_mayor_de_edad(edad)` que devuelva `True` si la edad es 18 o más.  
10. Crear una función `area_rectangulo(base, altura)` que devuelva el área.

---

## Nivel 3 – Combinando conceptos

11. Crear una función `pedir_numero()` que pida un número por input, lo convierta a entero y lo devuelva.  
12. Crear una función `comparar_numeros()` que pida dos números y diga cuál es mayor.  
13. Escribir una función `tabla_multiplicar(n)` que muestre la tabla del número ingresado (del 1 al 10).  
14. Crear una función `mostrar_mayores(lista)` que muestre los números mayores a 10.  
15. Crear una función `convertir_a_celsius(fahrenheit)` que devuelva el valor en grados Celsius.

---

## Nivel 4 – Funciones más dinámicas

16. Crear una función `sumar_lista(lista)` que sume todos los números de una lista.  
17. Escribir una función `buscar_palabra(palabra, texto)` que diga si la palabra aparece en el texto.  
18. Crear una función `contar_vocales(cadena)` que devuelva cuántas vocales tiene una palabra.  
19. Crear una función `invertir_texto(cadena)` que devuelva la palabra escrita al revés.  
20. Escribir una función `menu_principal()` que muestre un pequeño menú con 3 opciones y ejecute una función distinta según la elección.

---

*** Si vez algún ejercicio que requiera de usar colecciones o listas (y no te llevas bien con el tema) se puede posponer y seguir con la parte 6, para después volver :) ***

# 🧩 Parte 6: Listas y colecciones básicas

Las **listas** son una de las estructuras de datos más usadas en Python: te permiten guardar **varios valores en una sola variable**, en un orden determinado.  
Imaginatelas como una fila de casilleros numerados empezando desde 0.

---

## 🔹 6.1 ¿Qué es una lista?

Una lista es una colección ordenada y **mutable** (podés cambiarla).  
Se define con corchetes `[]` y los elementos van separados por comas.

```python
frutas = ["manzana", "banana", "naranja"]
numeros = [10, 5, 3, 8]
mixta = [1, "hola", 3.14, True]
```

📘 Características clave:
- Ordenada: cada elemento tiene una posición (índice) comenzando en 0.
- Mutable: podés cambiar, agregar o quitar elementos.
- Puede contener distintos tipos a la vez (números y textos mezclados).

---

## 🔹 6.2 Acceder a los elementos (indexing)

Para obtener un elemento usamos su índice:

```python
print(frutas[0])  # "manzana"
print(frutas[2])  # "naranja"
```

⚠️ Si pedís un índice que no existe (por ejemplo `frutas[10]`) obtendrás un error.

---

## 🔹 6.3 Longitud de una lista

`len()` devuelve cuántos elementos hay en la lista:

```python
print(len(frutas))  # 3
```

---

## 🔹 6.4 Modificar una lista

Podés cambiar el valor en un índice:

```python
frutas[1] = "pera"   # cambia "banana" por "pera"
```

---

## 🔹 6.5 Agregar y eliminar elementos

- `append(valor)` → agrega al final.  
- `insert(indice, valor)` → inserta en la posición indicada.  
- `remove(valor)` → elimina la primera ocurrencia del valor.  
- `pop()` → quita y devuelve el último elemento; `pop(i)` quita el elemento en la posición `i`.

```python
frutas.append("kiwi")
frutas.insert(1, "limón")
frutas.remove("naranja")
ultimo = frutas.pop()
```

---

## 🔹 6.6 Recorrer listas con `for`

```python
for fruta in frutas:
    print(fruta)
```

Esto imprime cada elemento en la lista, uno por uno.

---

## 🔹 6.7 Buscar elementos y el operador `in`

`in` sirve para consultar si un elemento está en la lista:

```python
if "manzana" in frutas:
    print("Tenés manzana")
```

---

## 🔹 6.8 Listas y funciones

Las listas se usan mucho dentro de funciones: podés pasarlas como parámetro, devolverlas, modificarlas adentro de una función, etc.

```python
def contar_elementos(lista):
    return len(lista)

print(contar_elementos([1, 2, 3, 4]))
```

---

## 🔹 6.9 Tuplas: listas que no cambian

Las **tuplas** son como listas, pero **inmutables**: una vez creadas no se pueden modificar. Se escriben con paréntesis `()`:

```python
dias = ("lunes", "martes", "miércoles")
```

Usá tuplas cuando querés asegurarte de que los datos no cambien.

---

## 🔹 6.10 Buenas prácticas con listas

- Evitá mezclar demasiados tipos si vas a procesar la lista numéricamente.  
- Usá nombres claros: `nombres`, `precios`, `temperaturas`.  
- Cuando necesites un conjunto fijo de valores que no cambian, pensá en usar una tupla.

---

# 💪 Ejercicios – Parte 6: Listas y colecciones (15 ejercicios)

1. Crear una lista `frutas` con 4 nombres y mostrar el primer y último elemento.  
2. Agregar una fruta al final de la lista y mostrar la lista completa.  
3. Insertar una fruta en la posición 1 y mostrar la lista.  
4. Reemplazar el segundo elemento por otra fruta y mostrar el cambio.  
5. Eliminar un elemento por su valor usando `remove()` y mostrar la lista.  
6. Usar `pop()` para quitar el último elemento y mostrar cuál se eliminó.  
7. Mostrar la cantidad de elementos de la lista usando `len()`.  
8. Recorrer la lista con un `for` y mostrar cada elemento en mayúsculas usando `.upper()`.  
9. Comprobar si `"banana"` está en la lista usando `in` y mostrar un mensaje.  
10. Crear una lista de números y sumar todos los elementos usando un `for`.  
11. Crear una función `sumar_lista(lista)` que devuelva la suma de sus elementos.  
12. Crear una lista vacía y pedirle al usuario 5 números (con `int(input())`) para agregarlos con `append()`. Mostrar la lista final.  
13. Pedir al usuario un número y decir si está dentro de la lista (si la lista contiene números).  
14. Crear una tupla con los días de la semana (solo 3 por simplicidad) y mostrar el segundo día.  
15. Escribir una función `promedio_lista(lista)` que calcule el promedio de números en la lista (usar `len()` y la suma).

---

*** En esta parte si algún ejercicio requiere del anterior se puede hacer todo en un mismo archivo y separar todo en funciones/separar con lineas de comentarios o copiar el ejercicio anterior (por ejemplo si se trata de una lista)
en otro archivo y seguir utilizándolo :) ***
