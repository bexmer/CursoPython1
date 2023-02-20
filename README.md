# Curso Dalto

## Indice

- [Curso Dalto](#curso-dalto)
  - [Indice](#indice)
  - [Datos Simples](#datos-simples)
  - [Variables](#variables)
  - [Datos compuestos](#datos-compuestos)
    - [Listas](#listas)
    - [Tupla](#tupla)
    - [Conjunto](#conjunto)
    - [Diccionarios](#diccionarios)
      - [Cuadro Comparativo](#cuadro-comparativo)
  - [Operadores](#operadores)
    - [Operadores aritmeticos](#operadores-aritmeticos)
    - [Operadores de Comparacion](#operadores-de-comparacion)
    - [Operadores Lógicos](#operadores-lógicos)
      - [**Operador AND**](#operador-and)
      - [**Operador OR**](#operador-or)
      - [**Operador Negacion**](#operador-negacion)
      - [**Prioridades**](#prioridades)
  - [Condicionales](#condicionales)
    - [If else y elif](#if-else-y-elif)

## Datos Simples

---

El tipo de texto son las comillas (`""`) o las comillas simples (`''`) siendo el string, tambien se puede poner tres veces las comillas (`"""texto"""`) este funciona para dar enters y aun sigue siendo valido,

```py
'''texto
dsfs
fds'''
```

El tipo entero siendo `int` es un tipo numerico entero, esta `float` numeros decimales y los `bool` que tiene dos modos el `True` y `False`.

```py
40 *int

40.2 *float

True   *boleano
False  *boleano
```

[Programa Relacionado](Tipos%20de%20Datos/datos-simples.py)

## Variables

---

Almacena informacion tal cual, estan los tipos de variables y son `String`, `Int`, `Boleano` y `Float`,`Decimal` y `Double`. Sin embargo como _Python_ es un lenguaje dinamico, este hace que las variables identifiquen que tipo de variable es el que esta guerdando.

```py
nombre = "Berny"  # ? Var. tipo cadena (String)
edad = 19  # ? Var. tipo Entero (Int);
salario = 1200.90  # ? Var. tipo flotante (Float, Decimal y Double)
Hombre = True  # ? Var. tipo Boleano (Bool)
```

Para poder imprimir valores y texto a la vez de una manera mas optima es agregando una `f` al principio de las comillas y para poner operaciones o variables se pone entre llaves `{}`, siendo que lo convierte a texto.

> camelCase => holaMundo
> snake_case => hola_mundo

```py
    print(nombre, ' ', edad, ' ', salario, ' ', Hombre)  # ; Se imprime todo
# ; Se imprime todo de una manera mas optima
print(f"Hola {nombre} tu edad es {edad} con un salario de {salario} siendo {Hombre}")

#//Imprime: Hola Berny tu edad es 19 con un salario de 1200.9 siendo True

```

[Programa Relacionado](Variables/variables.py)

## Datos compuestos

---

Datos que se agrupan datos simples.

### Listas

Son arrays que almacenan datos simples, en donde existe indices y elementos dentro de corchetes `[]`, siendo las posicion el indice y el elemento el dato que se esta guardando.

```py
lista = ["Berny",19,True,1.2]
```

En el ejemplo `Berny` es el elemento 1 y su posicion osea su indice es **0**, asi como esta el `19` siendo el elemento 2 y su indice o posicion es **1**, y asi susesivamente.

![Lista](img/listas.jpg)

### Tupla

Esto es similar a una lista, se define utilizando los parentesis `()`, **no se pueden modificar una vez que se han creado**, lo que las hace más eficientes en términos de rendimiento.

```py
tupla = ("Berny",19,1.2)
```

Siendo que las tuplas no se pueden modificar, pero si se puede hacer las demas cosas que ofrece las listas.

### Conjunto

los conjuntos son una estructura de datos **no ordenada y mutable** que se utiliza para almacenar elementos únicos. Se definen utilizando llaves `{}` o la función set(). Los conjuntos son útiles cuando se quiere eliminar elementos duplicados de una lista o para realizar operaciones matemáticas como la intersección, unión y diferencia de conjuntos. Los elementos de un conjunto pueden ser de cualquier tipo inmutable, como cadenas, números o tuplas. Los conjuntos también soportan operaciones como agregar y eliminar elementos, verificar si un elemento está en un conjunto y verificar la igualdad y desigualdad entre conjuntos.

```py
conjunto = {"Fall", 12, True, 'lol'} #muestra {True, 'lol', 12, 'Fall'}
conjunto = {"joll", False, 'yolo'} #muestra {False, 'yolo', 'joll'}
```

Estos no se puede acceder los elementos por el indice y no puede almacenar datos duplicados.

### Diccionarios

Los diccionarios son una estructura de datos **mutable y no ordenada** que se utiliza para almacenar pares _clave-valor_. Se definen utilizando llaves `{}` y separando cada _clave y valor con dos puntos_. Los diccionarios son útiles cuando se quiere acceder a los valores por su clave en lugar de su posición en la estructura de datos. Las claves de un diccionario pueden ser de cualquier tipo inmutable, como cadenas, números o tuplas, mientras que los valores pueden ser de cualquier tipo, incluyendo otros diccionarios. Los diccionarios soportan operaciones como agregar y eliminar elementos, acceder a los valores a través de las claves, verificar si una clave está en un diccionario y obtener listas de claves y valores. Los diccionarios también se utilizan comúnmente para representar datos estructurados en aplicaciones de procesamiento de datos y análisis.

```py
diccionario = {
    'nombre': "Begny",  # * Indice 0
    'edad': 19,  # * Indice 1
    'salario': 1200  # * Indice 2
}
```

#### Cuadro Comparativo

| Estructura de datos | Mutable | Ordenada | Única | Clave-Valor |
| ------------------- | ------- | -------- | ----- | ----------- |
| Lista               | Sí      | Sí       | No    | No          |
| Tupla               | No      | Sí       | No    | No          |
| Conjunto            | Sí      | No       | Sí    | No          |
| Diccionario         | Sí      | No       | No    | Sí          |

- Las listas son mutables, ordenadas y permiten elementos duplicados, pero no tienen una relación clave-valor.
- Las tuplas son no mutables, ordenadas y permiten elementos duplicados, pero no tienen una relación clave-valor.
- Los conjuntos son mutables, no ordenados y permiten elementos únicos, pero no tienen una relación clave-valor.
- Los diccionarios son mutables, no ordenados y no permiten claves duplicadas, pero tienen una relación clave-valor.

[Programa Ralcionado](Tipos%20de%20Datos/datos-compuestos.py)

## Operadores

---

### Operadores aritmeticos

Los aritmeticos son aquellas ecuaciones simples, como:

| Nombre                   | Simbolo        |
| ------------------------ | -------------- |
| Suma                     | **(n1 + n2)**  |
| Resta                    | **(n1 - n2)**  |
| Multiplicacion           | **(n1 \* n2)** |
| Division                 | **(n1 / n2)**  |
| Redondeo de una division | **(n1 // n2**  |
| Modulo                   | **(n1 % n2)**  |
| Potencia                 | **(n1\*\*n2)** |

Estos son acortadores de operciones.

| Nombre         | Simbolo   |
| -------------- | --------- |
| Suma           | **+=**    |
| Resta          | **-=**    |
| Multiplicacion | **\*=**   |
| Division       | **/=**    |
| Potencia       | **\*\*=** |
| Modulo         | **%=**    |

[Programa Relacionado](Operadores/op_aritmeticos.py)

### Operadores de Comparacion

| Significado       | Simbolo |
| ----------------- | ------- |
| Mayor que         | **>**   |
| Menor que         | **<**   |
| Mayor o igual que | **>=**  |
| Menor o igual que | **<=**  |
| Diferebte que     | **!=**  |
| Igual que         | **==**  |

[Programa Relacionado](Operadores/op_comparacion.py)

### Operadores Lógicos

Permiten contruir logicas, se obtiene como resultado **booleanos**

| Nombre          | Simbolo |
| --------------- | ------- |
| And (Conjucion) | **and** |
| Or (Disyucion)  | **or**  |
| Negacion        | **not** |

#### **Operador AND**

---

El `AND` debe de cumplirse todas las condiciones para dar `True`.

| Valor 1 | Operador | Valor 2 | <>      |
| ------- | -------- | ------- | ------- |
| True    | `and`    | True    | `True`  |
| False   | `and`    | True    | `False` |
| True    | `and`    | False   | `False` |
| False   | `and`    | False   | `False` |

#### **Operador OR**

---

El `OR` se debe de cumplir por al menos una condicion para que de `True`.

| Valor 1 | Operdor | Valor 2 | <>      |
| ------- | ------- | ------- | ------- |
| True    | `or`    | True    | `True`  |
| False   | `or`    | True    | `True`  |
| True    | `or`    | False   | `True`  |
| False   | `or`    | False   | `False` |

#### **Operador Negacion**

---

Este te va devolver el contrario de un `True` o un `False`.

| Valor        | <>      |
| ------------ | ------- |
| `not`(True)  | `False` |
| `not`(False) | `True`  |

#### **Prioridades**

---

> Ejemplo

a = 10, b = 12, c = 13, d = 10

((a > b) `or` (a < c)) `and` ((a == c) `or` (a >= b))

((_False_) `or` (_True_)) `and` ((_False_) `or` (_False_))

(_True_) `and` (_False_)

Resultado = **False**

[Programa Relacionado](Operadores/op_logicos.py)

## Condicionales

---

### If else y elif

La sintaxis de una condicional en Python utiliza la palabra clave `if` seguida de una expresión booleana, y opcionalmente se pueden agregar cláusulas `elif` y `else` para especificar diferentes caminos de ejecución.

```py
x = 5
if x > 0:
    print("x es positivo")
else:
    print("x es no positivo")
```

En este ejemplo, si la variable "**x**" es mayor que cero, se imprimirá "**x es positivo**". De lo contrario, se imprimirá "**x es no positivo**".

También puedes usar múltiples cláusulas `elif` para especificar diferentes condiciones que se evaluarán en orden si las anteriores no se cumplen.

```py
x = 10
if x < 0:
    print("x es negativo")
elif x == 0:
    print("x es cero")
elif x > 0 and x < 10:
    print("x es un número pequeño positivo")
else:
    print("x es un número grande positivo")
```

En este ejemplo, si "**x**" es menor que cero, se imprimirá "**x es negativo**". Si "**"x"**" es igual a cero, se imprimirá "**x es cero**". Si "**x**" está entre cero y diez, se imprimirá "**x es un número pequeño positivo**". Si "**x**" es mayor o igual a diez, se imprimirá "**x es un número grande positivo**".

[Programa Relacionado (if else)](Condicionales/if-else.py)

[Programa Relacionado (elif)](Condicionales/elif.py)
