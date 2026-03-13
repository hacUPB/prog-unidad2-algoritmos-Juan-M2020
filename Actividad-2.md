## ACTIVIDAD    2

>EJERCICIO 1




>*EJERCICIO 2*

**DATOS DE ENTRADA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| ID  |  AIIdentificador del empleado || S1, S2 , S3 , S4 ,S5 , S6  |  |
| |  |

**DATOS DE SALIDA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| ID  |  AIIdentificador del empleado |
| S1, S2 , S3 , S4 ,S5 , S6  |  |
| |  |




**PROCEDIMIENTOS**

TOTAL = S1 + S2 + S3 + S4 + S5 + S6
PROM = Total / 6

**PSEUDOCODIGO**

Inicio

Leer ID, S1, S2 , S3 , S4 ,S5 , S6

Total =  S1 + S2 + S3 + S4 + S5 + S6

Prom = Total / 6
Mostrar ID,Total,Prom

Fin



**OPERADORES RELACIONALES**
|   |       |
|------|----------------|
| Igial a | = |
| Mayor que  | > |
| Meyor o igual|>=  |
|Menor que |<|
|Menor o igual que |<=|



**Ejercicio**
>Un acuario necesita determinar cuantos litros de agua caben en un acuario , pero solo dispone de una cinta metrica. Diseña un algoritmo 


# Ejercicio 
>Realice un algoritmo para determinar cuánto se debe pagar por equis cantidad de lápices considerando que si son 1000 o más el costo es de $85 cada uno; de lo contrario, el precio es de $90. Represéntelo con el pseudocódigo y el diagrama de flujo.

**DATOS DE ENTRADA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| Largo  | Largo del tanque en CM  |
| Ancho  | Ancho del tanque en CM  |
| Alto|Alto del tanque en CM  |
|Unidad de salida | Unidad de medida (litro o galon) de volumen total|

 **DATOS DE SALIDA**
 |NOMBRE  |DESCRIPCION |
|------|----------------|
|Volumen lt | Volumen del tanque en litros  |
| Volumen gal  | Volumen del tanque en galones |



# Ejercicio 
>Un almacén de ropa tiene una promoción: por compras superiores a $250 000 se les aplicará un descuento de 15%, de caso contrario, sólo se aplicará un 8% de descuento. Realice un algoritmo para determinar el precio final que debe pagar una persona por comprar en dicho almacén y de cuánto es el descuento que obtendrá. Represéntelo mediante el pseudocódigo y el diagrama de flujo.

**DATOS DE ENTRADA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| Lapices  | Cantidad de lapices  |

**DATOS DE SALIDA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| Largo  |   |

Inicio 


Fin


# Ejercicio 
>El director de una escuela está organizando un viaje de estudios, y requiere determinar cuánto debe cobrar a cada alumno y cuánto debe pagar a la compañía de viajes por el servicio. La forma de cobrar es la siguiente: si son 100 alumnos o más, el costo por cada alumno es de $65.00; de 50 a 99 alumnos, el costo es de $70.00, de 30 a 49, de $95.00, y si son menos de 30, el costo de la renta del autobús es de $4000.00, sin importar el número de alumnos.

**DATOS DE ENTRADA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| Lapices  | Cantidad de lapices  |

**DATOS DE SALIDA**
|NOMBRE  |DESCRIPCION |
|------|----------------|
| Largo  |   |


## EJERCICIO BUCLES Y CICLOS

```
Inicio 
SU = 0 
VA = 0
Mientras VA != -1
    Leer VA 
    SU = SU + VA
Fin mientras 
Escribir SU 
Fin
```
### Parte 1: Identificar Algoritmos

Responde si los siguientes enunciados representan un algoritmo. Justifica la respuesta:

1. Una página web. ❌  
2. Una receta para hacer un pastel, donde se indican ingredientes y pasos a seguir. ✅
3. "Piensa en un número y multiplícalo por otro". ❌
4. Un manual de instrucciones para armar un mueble, con pasos detallados y un orden claro. ✅
5. Una lista de compras organizada en orden alfabético ❌

### Parte 2: Variables y Constantes

Indica si las siguientes afirmaciones describen una variable o una constante:

1. El valor de la gravedad en la Tierra, 9.8 m/s². **(constante)**

2. La edad de una persona calculada con base en el año actual y su año de nacimiento.**(variable)**

3. La cantidad de dinero en una cuenta bancaria.**(variable)**

4. La velocidad de la luz en el vacío, 299,792,458 m/s.**(constante)**

5. El radio de un círculo.**(variable)**









### Parte 4: Comprensión de Herramientas
Indica si las siguientes afirmaciones son ciertas o falsas respecto al pseudocódigo y diagramas de flujo:

1. El pseudocódigo utiliza símbolos estándar para representar las operaciones lógicas. ❌
2. Los diagramas de flujo son una representación gráfica de un algoritmo. ✅
3. El pseudocódigo debe estar escrito en un lenguaje de programación específico. ❌
4. Un diagrama de flujo siempre debe tener un inicio y un fin claramente definidos. ✅

### Parte 5: Estructuras de Control
Las estructuras de control sirven para dirigir el comportamiento de un algoritmo o programa.
Permiten decidir qué instrucciones ejecutar, cuántas veces repetirlas y en qué orden hacerlo.

En pocas palabras, hacen que un proceso no sea solo una lista de pasos lineales, sino que pueda tomar decisiones, repetir acciones o elegir caminos diferentes según ciertas condiciones.

Las principales estructuras de control son:

**Secuenciales** (paso a paso, sin decisiones).

**Condicionales** (si ocurre algo, entonces haz esto; si no, haz otra cosa).

**Repetitivas o cíclicas** (repiten acciones mientras se cumpla una condición).

```
Ejemplo 1:
```

```
Ejemplo 2: Con cálculos matemáticos

Supongamos que quieres saber si puedes comprar un celular que cuesta $5,000.

Tienes $4,200 ahorrados y sabes que esta semana recibirás $1,000 más.

Primero haces un cálculo:

Total disponible = 4,200 + 1,000 = 5,200

Luego tomas la decisión:

Si el total disponible es mayor o igual a 5,000, entonces lo compro.
Si no, sigo ahorrando.

Aquí se combinan cálculo matemático + estructura condicional.
El resultado del cálculo determina qué decisión se toma.

```
## EJERCICIO 4

se requiere un algoritmo para determinar, de N (que lo ingresa el usuario por teclado) cantidades ingresadas por teclado, cuantas son cero, cuantas son menores a cero, y cuantas son mayores a cero.

```
Inicio 
N = 0
Si N < 0
    Leer N
    N = N + 1
Si no
Si n > 0
    Leer N
    N = N + 1

Fin mientras
Escribir N
Fin
```