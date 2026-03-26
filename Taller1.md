
# Taller de Algoritmos

---



### **Ejercicios con condicionales**

1. **Verificación de peso de despegue**
    
En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.


```
INICIO
    ESCRIBIR "Ingrese el peso total de la aeronave: "
    LEER peso

    ESCRIBIR "Ingrese el peso máximo permitido: "
    LEER P_maximo

    SI peso <= P_maximo ENTONCES
        ESCRIBIR "Aeronave lista para despegar"
    SINO
        ESCRIBIR "Excede el límite - Reducir carga o combustible"
    FIN SI
FIN

```

 **2. Control de temperatura del motor**

 Durante una inspección de rutina, se mide la temperatura de un motor de turbina. Si la temperatura es mayor a un valor crítico, se debe indicar "Peligro: sobrecalentamiento". Si está dentro del rango seguro, indicar "Operación normal". Si es demasiado baja, indicar "Motor frío – Calentar antes de operar".
    
```
INICIO
    ESCRIBIR "Ingrese la temperatura del motor: "
    LEER temperatura

    SI temperatura > 100 ENTONCES
        ESCRIBIR "Peligro: sobrecalentamiento"
    SINO
        SI temperatura >= 50 ENTONCES
            ESCRIBIR "Operación normal"
        SINO
            ESCRIBIR "Motor frío – Calentar antes de operar"
        FIN SI
    FIN SI
FIN
```
---

### **Ejercicios con bucles**

1. **Registro de altitudes de vuelo**
    
    Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.

```
INICIO
    DEFINIR altitud, i COMO ENTERO

    PARA i = 1 HASTA 6 HACER
        ESCRIBIR "Ingrese altitud en el minuto ", i*10
        LEER altitud
    FIN PARA

    ESCRIBIR "Registro completado"
FIN
```
    
2. **Control de combustible en pruebas**
    
    Durante un ensayo en banco de un motor a reacción, se mide el nivel de combustible cada minuto y se detiene el registro cuando el combustible baja del 10%. Mostrar el tiempo total de operación antes de llegar a ese punto.
    
```
INICIO
    DEFINIR combustible, tiempo COMO ENTERO

    tiempo = 0

    MIENTRAS VERDADERO HACER
        ESCRIBIR "Ingrese nivel de combustible (%): "
        LEER combustible

        SI combustible < 10 ENTONCES
            ESCRIBIR "Nivel crítico alcanzado"
            SALIR
        FIN SI

        tiempo = tiempo + 1
    FIN MIENTRAS

    ESCRIBIR "Tiempo total de operación: ", tiempo, " minutos"
FIN
```
---

### **Ejercicios con bucle y condicionales**

1. **Detección de turbulencia en trayecto**
    
    Un sensor mide la aceleración vertical de la aeronave en intervalos de un segundo durante un trayecto de 2 minutos. Si el valor medido supera un umbral, indicar que se ha detectado turbulencia en ese instante. Al final, mostrar cuántas turbulencias se detectaron.

```
INICIO
    DEFINIR i, contador COMO ENTERO
    DEFINIR aceleracion COMO REAL

    contador = 0

    PARA i = 1 HASTA 120 HACER
        ESCRIBIR "Ingrese aceleración en el segundo ", i
        LEER aceleracion

        SI aceleracion > 5 ENTONCES
            ESCRIBIR "Turbulencia detectada en segundo ", i
            contador = contador + 1
        FIN SI
    FIN PARA

    ESCRIBIR "Total de turbulencias: ", contador
FIN
```
    
2. **Control de temperatura en cabina**
    
    Un sistema mide cada 5 minutos la temperatura en cabina durante una hora. Si en algún momento se detecta una temperatura mayor a 27°C o menor a 18°C, debe indicar que se active el sistema de climatización.

```
INICIO
    DEFINIR temperatura, i COMO ENTERO

    PARA i = 1 HASTA 12 HACER
        ESCRIBIR "Ingrese temperatura en minuto ", i*5
        LEER temperatura

        SI temperatura > 27 O temperatura < 18 ENTONCES
            ESCRIBIR "Activar sistema de climatización"
        FIN SI
    FIN PARA
FIN
```
    
3. **Simulación de conteo de pasajeros**
    
    Durante el abordaje, un sistema cuenta a los pasajeros que ingresan. Si el número total supera la capacidad máxima, el sistema debe detener el conteo y mostrar un mensaje de alerta.
    
```
INICIO
    DEFINIR capacidad, total COMO ENTERO

    ESCRIBIR "Ingrese capacidad máxima: "
    LEER capacidad

    total = 0

    MIENTRAS VERDADERO HACER
        total = total + 1

        SI total > capacidad ENTONCES
            ESCRIBIR "Alerta: capacidad excedida"
            SALIR
        FIN SI
    FIN MIENTRAS
FIN
```
---

### **Ejercicios de mayor complejidad**

1. **Planificación de misión satelital**
    
    Desarrollar un algoritmo que reciba datos de consumo de energía por hora de un satélite durante un día completo. Si en cualquier hora el consumo excede un límite crítico, debe registrarse como una alerta. Al final, mostrar el consumo total y el número de alertas generadas.

```
INICIO
    DEFINIR consumo, total, alertas, i COMO ENTERO

    total = 0
    alertas = 0

    PARA i = 1 HASTA 24 HACER
        ESCRIBIR "Consumo en la hora ", i
        LEER consumo

        total = total + consumo

        SI consumo > 100 ENTONCES
            alertas = alertas + 1
        FIN SI
    FIN PARA

    ESCRIBIR "Consumo total: ", total
    ESCRIBIR "Número de alertas: ", alertas
FIN
```
    
2. **Simulación de carga y balanceo de aeronave**
    
    Una aeronave tiene varias bodegas de carga. El sistema debe permitir ingresar el peso cargado en cada bodega y verificar que:
    
    - El peso total no exceda el máximo permitido.
    - Ninguna bodega individual supere su límite.
        
        Mostrar mensajes de advertencia si alguna condición no se cumple.

```
INICIO
    DEFINIR bodegas, i COMO ENTERO
    DEFINIR peso, total COMO REAL

    ESCRIBIR "Número de bodegas: "
    LEER bodegas

    total = 0

    PARA i = 1 HASTA bodegas HACER
        ESCRIBIR "Peso en bodega ", i
        LEER peso

        SI peso > 500 ENTONCES
            ESCRIBIR "Advertencia: bodega excede límite"
        FIN SI

        total = total + peso
    FIN PARA

    SI total > 2000 ENTONCES
        ESCRIBIR "Advertencia: peso total excedido"
    SINO
        ESCRIBIR "Carga dentro del límite"
    FIN SI
FIN
```
        
3. **Monitoreo de aproximación a pista**
    
    Durante la aproximación, un sistema recibe datos de altitud y velocidad cada 5 segundos hasta el aterrizaje. Si la velocidad excede el valor máximo seguro o la altitud no desciende adecuadamente, debe indicarse un mensaje de corrección de maniobra. Mostrar un resumen final de todos los avisos emitidos.
    
```
INICIO
    DEFINIR altitud, velocidad COMO REAL
    DEFINIR avisos, i COMO ENTERO

    avisos = 0

    PARA i = 1 HASTA 20 HACER
        ESCRIBIR "Ingrese altitud: "
        LEER altitud

        ESCRIBIR "Ingrese velocidad: "
        LEER velocidad

        SI velocidad > 300 ENTONCES
            ESCRIBIR "Reducir velocidad"
            avisos = avisos + 1
        FIN SI

        SI altitud < 0 ENTONCES
            ESCRIBIR "Error en descenso"
            avisos = avisos + 1
        FIN SI
    FIN PARA

    ESCRIBIR "Total de avisos: ", avisos
FIN
```

---