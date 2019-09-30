Ejercicios para practicar la estructura de control de bucle o repetición condicional (while) usando Python.

En los siguientes videos podrás ver una explicación de la estructura y también la resolución paso a paso de estos ejercicios:
+ [Repetición condicional: while](https://youtu.be/Rkv3GtEZEnw)
+ [Ejercicios con la estructura de repetición condicional](https://www.youtube.com/watch?v=I6T_qjYiDDM)
+ [Ejercicios con break y continue](https://www.youtube.com/watch?v=lG-DTUOZVZg)

La resolución de cada ejercicio se muestra al hacer click sobre la consigna.

### 1
<details> 
  <summary>Leer números enteros de teclado, hasta que el usuario ingrese el 0. Finalmente, mostrar la sumatoria de todos los números ingresados.</summary>
<br>Solución:

```
total=0
nro=int(input("Número: "))
while nro != 0:
    total+=nro
    nro=int(input("Número: "))
```

</details>


### 2
<details> 
  <summary>Leer números enteros de teclado, hasta que el usuario ingrese el 0. Finalmente, mostrar la sumatoria de todos los números positivos ingresados.</summary>
<br>Solución:

```
positivos=0
n=int(input("Número (0 para terminar): "))
while n!=0:
    if n>0:
        positivos+=1
    n=int(input("Número (0 para terminar): "))
print("Cantidad de positivos:", positivos)
```

</details>



### 3
<details> 
  <summary>Leer números enteros positivos de teclado, hasta que el usuario ingrese el 0. Informar cuál fue el mayor número ingresado.</summary>
<br>Solución:

```
mayor=-1
n=int(input("Número positivo:"))
while n>=0:
   if n>mayor:
       mayor=n
   n=int(input("Número positivo:"))
print("Mayor número ingresado:", mayor)
```

</details>


### 4
<details> 
  <summary>Leer un número entero positivo desde teclado e imprimir la suma de los dígitos que lo componen.</summary>
<br>Solución:

```
suma=0
n=int(input("Número positivo:"))
while n!=0:
    digito=n%10
    suma+=digito
    n=n//10
print("Suma de los dígitos:", suma)
```

</details>


### 5
<details> 
  <summary>Solicitar al usuario que ingrese números enteros positivos y, por cada uno, imprimir la suma de los dígitos que lo componen. La condición de corte es que se ingrese el número -1. Al finalizar, mostrar cuántos de los números ingresados por el usuario fueron números pares.</summary>
<br>Solución:

```
pares=0
n=int(input("Número (-1 para terminar el programa): "))
while n!=-1:
    if n%2 == 0:
        pares+=1
    suma=0
    while n!=0:
        digito=n%10
        suma+=digito
        n=n//10
    print("Suma de sus dígitos:", suma)
    n=int(input("Número (-1 para terminar el programa): "))
print("Se ingresaron", pares, "números pares")
```

</details>



### 6
<details> 
  <summary>Mostrar un menú con tres opciones: 1- comenzar programa, 2- imprimir listado, 3-finalizar programa. A continuación, el usuario debe poder seleccionar una opción (1, 2 ó 3). Si elige una opción incorrecta, informarle del error. El menú se debe volver a mostrar luego de ejecutada cada opción, permitiendo volver a elegir. Si elige las opciones 1 ó 2 se imprimirá un texto. Si elige la opción 3, se interrumpirá la impresión del menú y el programa finalizará.</summary>
<br>Solución:

```
while True:
    print("Opción 1 - comenzar programa")
    print("Opción 2 - imprimir listado")
    print("Opción 3 - finalizar programa")
    opcion=int(input("Opción elegida: "))
    if opcion==1:
        print("¡Comenzamos!")
    elif opcion==2:
        print("Listado:")
        print("Nadia, Esteban, Mariela, Fernanda")
    elif opcion==3:
        print("Hasta la próxima")
        break
    else:
        print("Opción incorrecta. Debe ingresar 1, 2 o 3")
```

</details>

### 7
<details> 
  <summary>Solicitar al usuario el ingreso de una frase y de una letra (que puede o no estar en la frase). Recorrer la frase, carácter a carácter, comparando con la letra buscada. Si el carácter no coincide, indicar que no hay coincidencia en esa posición (imprimiendo la posición) y continuar. Si se encuentra una coincidencia, indicar en qué posición se encontró y finalizar la ejecución.</summary>
<br>Solución:

```
frase=input("Frase: ")
l=input("Letra para buscar su posición: ")
i=0
while i!=len(frase):
    if l!=frase[i]:
        print("No se encontró en la posición", i)
        i+=1
        continue
    print("Se encontró en la posición", i)
    break
```

</details>

### 8
<details> 
  <summary>Crear un programa que permita al usuario ingresar los montos de las compras de un cliente (se desconoce la cantidad de datos que cargará, la cual puede cambiar en cada ejecución), cortando el ingreso de datos cuando el usuario ingrese el monto 0.
<br />Si ingresa un monto negativo, no se debe procesar y se debe pedir que ingrese un nuevo monto. Al finalizar, informar el total a pagar teniendo que cuenta que, si las ventas superan el total de $1000, se le debe aplicar un 10% de descuento.
</summary>
<br>Solución:

```
total=0
monto=float(input("Monto de una venta: $"))
while monto!=0:
    if monto<0:
        print("Monto no válido.")
    else:
        total+=monto
    monto=float(input("Monto de una venta: $"))
if total>1000:
    total-=total*0.1
print("Monto total a pagar: $", total)
```

</details>

### 9
<details> 
  <summary>Crear un programa que solicite el ingreso de números enteros positivos, hasta que el usuario ingrese el 0. Por cada número, informar cuántos dígitos pares y cuántos impares tiene.
<br />Al finalizar, informar la cantidad de dígitos pares y de dígitos impares leídos en total.
</summary>
<br>Solución:

```
numero=int(input("numero: "))
totalPares=0
totalImpares=0
while numero!=0:
   pares=0
   impares=0
   while numero!=0:   
     ultimodigito=numero%10
     if ultimodigito%2==0:
       pares+=1
       totalPares+=1
     else:
       impares+=1
       totalImpares+=1
     numero=numero//10
   print("El número ingresado tiene ",pares," digitos pares y ",impares," digitos impares")
   numero=int(input("Otro número: "))
print("Total de dígitos pares:", totalPares)
print("Total de dígitos impares:", totalImpares)
```

</details>

### 10
<details> 
  <summary>Crear un programa que permita al usuario ingresar títulos de libros por teclado, finalizando el ingreso al leerse el string “*” (asterisco). Cada vez que el usuario ingrese un string de longitud 1 que contenga sólo una barra (“/”) se considera que termina una línea.
  Por cada línea completa, informar cuántos dígitos numéricos (del 0 al 9) aparecieron en total (en todos los títulos de libros que componen en esa línea). Finalmente, informar cuántas líneas completas se ingresaron.
<br />**Ejemplo de ejecución:**
<br />Libro: Los 3 mosqueteros
<br />Libro: Historia de 2 ciudades
<br />Libro: /
<br />Línea completa. Aparecen 2 dígitos numéricos.
<br />Libro: 20000 leguas de viaje submarino
<br />Libro: El señor de los anillos
<br />Libro: /
<br />Línea completa. Aparecen 5 dígitos numéricos.
<br />Libro: 20 años después
<br />Libro: *
<br />Fin. Se leyeron 2 líneas completas.</summary>
<br>Solución:

```
lineas=0
digitos="0123456789"
cantidadDigitos=0
cadena=input("Cadena: ")
while cadena!="*":
    for caracter in cadena:
        if caracter in digitos:
            cantidadDigitos+=1
    if cadena=="/":
        lineas+=1
        print("Aparecen ", cantidadDigitos, " dígitos en la línea")
        cantidadDigitos=0
    cadena=input("Cadena: ")
print("Se leyeron ",lineas," líneas completas")
```

</details>


### 11
<details> 
  <summary>Escribir un programa que solicite el ingreso de una cantidad indeterminada de números mayores que 1, finalizando cuando se reciba un cero. 
Imprimir la cantidad de números primos ingresados.</summary>
<br>Solución:

```
cantidad=0
n=int(input("Número: "))
while n!=0:
 primo=True
 for i in range(2,n):
   if n%i==0:
     primo=False
     break
 if primo:
   cantidad+=1
 n=int(input("Número: "))
print("primos: ", cantidad)
```

</details>

### 12
<details> 
  <summary>Solicitar al usuario que ingrese una frase y luego informar cuál fue la palabra más larga (en caso de haber más de una, mostrar la primera) y cuántas palabras había. Precondición: se tomará como separador de palabras al carácter “ “ (espacio), ya sea uno o más.</summary>
<br>Solución:

```
frase=input("Frase: ").strip()
cantidad=0
len_p_mas_larga=0
while len(frase) != 0:
    cantidad=cantidad+1
    i=frase.find(" ")
    if i != -1:
        palabra=frase[0:i]
        while i < len(frase) and frase[i] == " ":
            i=i+1
        frase=frase[i:]
    else:
        palabra=frase
        frase=""
    if len(palabra) > len_p_mas_larga:
        len_p_mas_larga=len(palabra)
        p_mas_larga=palabra
if cantidad > 0:
    print("Palabra más larga:", p_mas_larga)
print("Cantidad de palabras:", cantidad)
```

</details>
