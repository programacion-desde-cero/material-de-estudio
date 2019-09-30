Ejercicios para practicar la estructura de control de decisión o selección (if-else-elif) usando Python.

En los siguientes videos podrás ver una explicación de la estructura de selección y también la resolución paso a paso de estos ejercicios:
+ [Selección o decisión: if, if-else, if-elif-else](https://www.youtube.com/watch?v=kIkAhld32O8)
+ [Ejercicios con la estructura de selección](https://www.youtube.com/watch?v=PKFKoAN2zEo)
+ [Ejercicio con la estructura de selección](https://www.youtube.com/watch?v=HMfaVLkjIUA)

La resolución de cada ejercicio se muestra al hacer click sobre la consigna.

### 1
<details> 
  <summary>Solicitar al usuario un número de cliente. Si el número es el 1000, imprimir "Ganaste un premio".</summary>
<br/>Solución:

```
numero=int(input("N. de cliente:"))
if numero==1000:
    print("Ganaste un premio!")    
```

</details>

### 2
<details> 
  <summary>Solicitar al usuario que ingrese dos números y mostrar cuál de los dos es menor. No considerar el caso en que ambos números son iguales.</summary>
<br/>Solución:

```
a=int(input("Ingresa un número:"))
b=int(input("Ingresa un número:"))
if a<b:
    print("el primero es menor")
else:
    print("el segundo es menor")
```

</details>

### 3
<details> 
  <summary>Solicitar al usuario que ingrese dos números y mostrar cuál de los dos es menor. Considerar el caso en que ambos números son iguales.</summary>
<br/>Solución:
  
```
a=int(input("Un número:"))
b=int(input("Otro número:"))
if a<b:
    print("El primero es menor")
elif b<a:
    print("El segundo es menor")
else:
    print("Son iguales")
  ```
  
</details>


### 4
<details> 
  <summary>Requerir al usuario que ingrese un día de la semana e imprimir un mensaje si es lunes, otro mensaje diferente si es viernes, otro mensaje diferente si es sábado o domingo. Si el día ingresado no es ninguno de esos, imprimir otro mensaje.</summary>
<br/>Solución:

```
dia=input("Dia de la semana: ")
if (dia=="lunes"):
    print("Oh, no!")
elif (dia==”viernes”):
    print(“¡Ya casi!”)
elif (dia==”sábado” or “domingo”):
    print(“Ahora sí se puede descansar”)
else:
    print(“A esperar el fin de semana”)
```

</details>


### 5
<details> 
  <summary>Escribir un programa que, dado un número entero, muestre su valor absoluto.
Nota: para los números positivos su valor absoluto es igual al número (el valor absoluto de 52 es 52), mientras que, para los negativos, su valor absoluto es el número multiplicado por -1 (el valor absoluto de -52 es 52).</summary>
<br>Solución:

```
numero=int(input("Número:"))
if numero<0:
    numero=numero*-1
print("Valor absoluto:", numero)
```

</details>


### 6
<details> 
  <summary>Solicitar al usuario que ingrese los nombres de dos personas, los cuales se almacenarán en dos variables.
A continuación, imprimir “coincidencia” si los nombres de ambas personas comienzan con la misma letra ó si terminan con la misma letra. Si no es así, imprimir “no hay coincidencia”.</summary>
<br>Solución:

```
nombre1=input("Un nombre: ")
nombre2=input("Otro nombre: ")
posicion_final_nombre1=len(nombre1)-1
posicion_final_nombre2=len(nombre2)-1
if nombre1[0] == nombre2[0] or nombre1[posicion_final_nombre1] == nombre2[posicion_final_nombre2]:
    print("coincidencia")
else:
    print("no hay coincidencia")
```

</details>


### 7
<details> 
  <summary>Crear un programa que permita al usuario elegir un candidato por el cual votar. Las posibilidades son: candidato A por el partido rojo, candidato B por el partido verde, candidato C por el partido azul.
Según el candidato elegido (A, B ó C) se le debe imprimir el mensaje “Usted ha votado por el partido [color que corresponda al candidato elegido]”.
Si el usuario ingresa una opción que no corresponde a ninguno de los candidatos disponibles, indicar “Opción errónea”.</summary>
<br>Solución:

```
candidato=input("Candidato elegido: ")
if candidato.upper()=="A":
    print("Usted ha votado por el partido rojo")
elif candidato.upper()=="B":
    print("Usted ha votado por el partido verde")
elif candidato.upper()=="C":
    print("Usted ha votado por el partido azul")
else:
    print("Opción errónea")
```

</details>


### 8
<details> 
  <summary>Escribir un programa que solicite al usuario una letra y, si es una vocal, muestre el mensaje “es vocal”.
Se debe validar que el usuario ingrese sólo un carácter. Si ingresa un string de más de un carácter, informarle que no se puede procesar el dato.</summary>
<br>Solución:

```
letra=input("Letra:")
if len(letra)!=1:
    print("Debe ser sólo una letra")
else
    if letra in "aeiou":
        print("Es vocal")
```

</details>


### 9
<details> 
  <summary>Hacer un programa que permita saber si un año es bisiesto. Para que un año sea bisiesto debe ser divisible por 4 y no debe ser divisible por 100, excepto que también sea divisible por 400.</summary>
<br>Solución:

```
anio=int(input("Año:"))
if anio%4 == 0:
    if anio%100 != 0 or anio%400 == 0:
        print("Bisiesto")
    else:
        print("No bisiesto")
else:
    print("No bisiesto")
```

</details>


### 10
<details> 
  <summary>Un instituto de enseñanza de inglés necesita un programa que le permita, cada día, procesar observaciones sobre las clases de ese día. El instituto dicta clases a estudiantes de distintos niveles y cada nivel tiene clases en un día de la semana diferente: los lunes se dicta el nivel inicial, los martes el nivel intermedio, los miércoles el nivel avanzado, los jueves son para práctica hablada y los viernes se dicta inglés para viajeros.
<br />Se debe comenzar por solicitar al usuario que ingrese la fecha actual en formato "día, DD/MM", donde [día] es un día de la semana, DD es el número de día y MM es el número de mes. Si el usuario ingresa un día de la semana inexistente o una fecha cuyo día supere el número 31 o el mes supere el número 12, finalizar el programa indicando que se produjo un error. Debe permitirse que ingrese el día de la semana en minúsculas o mayúsculas indistintamente. Como precondición se tiene que lo ingresado por el usuario tendrá la forma <[alfanumérico], [numérico]/[numérico]>.
<br />Una vez indicada la fecha, el usuario necesita poder indicar si ese día se tomaron exámenes, pero eso sólo si se trata de los niveles inicial, intermedio o avanzado, ya que las prácticas habladas y el inglés para viajeros no tienen exámenes. Si hubo exámenes, el usuario ingresará cuántos alumnos aprobaron y cuántos no, y el programa le mostrará el porcentaje de aprobados.
<br />Si el día fue el correspondiente a práctica hablada, el usuario deberá ingresar el porcentaje de asistencia a clase y el programa le indicará "asistió la mayoría" en caso de que la asistencia sea mayor al 50% o "no asistió la mayoría" si no es así.
<br />Si se trata del inglés para viajeros y la fecha actual corresponde al día 1 del mes 1 o del mes 7, se deberá imprimir "Comienzo de nuevo ciclo" y solicitar al usuario que ingrese la cantidad de alumnos del nuevo ciclo y el arancel en $ por cada alumno, para luego imprimir el ingreso total en $.</summary>
<br>Solución:

```
fecha=input("Fecha (formato 'día, DD/MM'): ")
fecha=fecha.lower()
diasemana=fecha[0:fecha.find(',')]
dianro=int(fecha[fecha.find(',')+2:fecha.find('/')])
mesnro=int(fecha[fecha.find('/')+1:])
if dianro>31 or mesnro>12:
    print("Fecha incorrecta")
else:
    if diasemana in "lunes,martes,miércoles":
        respuesta=input("¿Se tomaron exámenes? S/N: ")
        if respuesta.lower()=="s":
            aprobados=int(input("Cantidad de aprobados: "))
            reprobados=int(input("Cantidad de reprobados: "))
            print("Porcentaje de aprobados:", (aprobados*100)/(aprobados+reprobados), "%")
    elif diasemana=="jueves":
        asistencia=int(input("Porcentaje de asistencia: "))
        if asistencia>50:
            print("Asistió la mayoría")
        else:
            print("No asistió la mayoría")
    elif diasemana=="viernes":
        if dianro==1 and (mesnro==1 or mesnro==7):
            print("Nuevo ciclo")
            alumnos=int(input("Cantidad de alumnos: "))
            arancel=float(input("Arancel: $"))
            print("Ingreso total: $", alumnos*arancel)
    else:
        print("Fecha incorrecta")
print("Fin del programa")
```

</details>
