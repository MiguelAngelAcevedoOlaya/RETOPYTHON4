## Resolver los siguientes problemas usando un notebook de python y subirlos a un repo.

* Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.

* Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.

* Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.

* Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:
  * Positivo: "El número x es positivo"
  * Negativo: "El número x es negativo"
  * Cero (0): "El número x es el neutro para la suma"

* Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.

* Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

### PUNTO 1
Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.

Primero revisamos en que números del código ASCII hay minusculas

* 97=a
* 101=e
* 105=i
* 111=o
* 117=u
* 129 <= a <= 134
* 136 <= a <= 141
* 147 <= a <= 151
* 160 <= a <= 163

Ahora se le pide al usuario que ingrese un  numero aleatorio

  
```
numero_ASCII = int(input("Elige un numero preferiblemente entre 1 y 255 = "))
```

Como segundo paso se utiliza un condicioal if en el que si el numero esta entre los rangos establecidos en la lista anterior, sea una vocal minuscula, y en caso tal que no, se imprima que no lo es

```
if numero_ASCII == 97:
  print("Corresponde a una vocal minúscula")
elif numero_ASCII == 101:
  print("Corresponde a una vocal minúscula")
elif numero_ASCII == 105:
  print("Corresponde a una vocal minúscula")
elif numero_ASCII == 111:
  print("Corresponde a una vocal minúscula")
elif numero_ASCII == 117:
  print("Corresponde a una vocal minúscula")
elif 129<= numero_ASCII <= 134:
  print("Corresponde a una vocal minúscula")
elif 136<= numero_ASCII <= 141:
  print("Corresponde a una vocal minúscula")
elif 147<= numero_ASCII <= 151:
  print("Corresponde a una vocal minúscula")
elif 160<= numero_ASCII <= 163:
  print("Corresponde a una vocal minúscula")
else:
  print("No corresponde a vocal minúscula")
```

### PUNTO 2

Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.

Para esto primero le pedimos al usuario que ingrese una letra a su eleccion y que imprima la longitud de su cadena para comporar que sea de 1

```
palabra = input("La letra ingresada es ")
print(len(palabra))
```

Ahora usamos el codigo ord(), que nos permite imprimir el valor número en codigo ASCII de la letra seleccionada por el usuario

```
print(ord(palabra))
```

Definimos número par como el ord(palabra)

```
numero_par= ord(palabra)
```

Ponemos un codigo de tipo condicional en el que si el residuo del numero al dividirlo entre 2 es 0, la letra pertenecera a número par en ASCII, y en caso tal que no lo sea, pues no pertencera a los pares

```
if numero_par % 2 ==0.0:
  print("La letra " +str(palabra)+ " es par en su correspondiente número ASCII")
else:
  print("La letra " +str(palabra)+ " no es par en su correspondiente número ASCII")
```

### PUNTO 3

Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.


Primero se le solicita al usuario que ingrese el caracter que guste

Ahora utilizaremos el codigo isnumeric, para comprobar si el caracter pertenece a cualquier número, en caso tal que no imprimira que no es un número, en caso tal de que si, definiremos la variable como un entero y le pondremos otra condicional if en el que si el número esta entre 0 y 9 si es un digito, y si no no pertenecera

```
caracter = input("Ingresa un caracter ")
y = caracter.isnumeric()
if y == caracter.isnumeric():
  caracter=int(caracter)
  if 0 <= caracter <= 9:
    print(str(caracter)+ " Es un digito")
  else:
    print(str(caracter)+ " No es un digito")
else:
  print("No es un número")
```

### PUNTO 4

Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:
  * Positivo: "El número x es positivo"
  * Negativo: "El número x es negativo"
  * Cero (0): "El número x es el neutro para la suma"

Primero se le solicita al usuario que ingrese el numero que desee, definiendo esta variable como flotante, osea que permite todos los números reales.

Ahora utilizaremos un codigo if else, en el que si el número es mayor que 0 es postivo, y si es menor que 0 sera negativo, en caso de ser neutro pondremos que es nuetro para la suma

```
numero_4 = float(input("El múmero que quieres elegir es "))
if numero_4 > 0:
  print("El número x es positivo")
elif numero_4 == 0:
  print("El número x es el neutro para la suma")
elif numero_4 < 0:
  print("El número x es negativo")
```

### PUNTO 5

Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.


En primer lugar se le pedira al usuario que ingrese los valores del centro de la circunferencia en x, y, y ademas solicitarle el valor del radio

```
x_centro = float(input("Ingrese el valor del centro en x "))
y_centro = float(input("Ingrese el valor del centro en y "))
r_radio = float(input("Ingrese el valor del radio"))
```

Ahora se le solicitar al usuario que ingrese el valor x,y que desea ingresar para confirmar si esta o no dentro del circulo

```
x_eleccion = float(input("Ingrese el valor de x "))
y_eleccion = float(input("Ingrese el valor de y "))
```

Ahora ingresamos la ecuación (x-a)2 + (y-a)2 = r**2

si el numero ingresado es menor al radio, entonces esta dentro del circulo, si es mayor estara por fuera, y si es igual entonces estara en el circulo

```
if (x_eleccion - x_centro)**2 + (y_eleccion - y_centro)**2 < r_radio**2:
  print("El punto " +str(x_eleccion)+ "," +str(y_eleccion)+ " esta dentro del circulo")
elif (x_eleccion - x_centro)**2 + (y_eleccion - y_centro)**2 == r_radio**2:
  print("El punto " +str(x_eleccion)+ "," +str(y_eleccion)+ " esta en el circulo")
else:
  print("El punto " +str(x_eleccion)+ "," +str(y_eleccion)+ " esta fuera del circulo")
```

### PUNTO 6

Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

En primer lugar analizamos la teoria que nos dice que en caso tal que la suma de las dos longitudes mas chicas sea mayor que la longitd del lado mayor, si se podra construir un trinagulo.

Ahora establecemos un codigo que solicite al usuario ingresar tres longitudes distintas.

```
l_1 = float(input("Longitud 1 es "))
l_2 = float(input("Longitud 2 es "))
l_3 = float(input("Longitud 3 es "))
```

Ahora se establece un condicional siguiendo la teorica en que si L_mayor es < L_menor1 + L_menor2 si se podra construir un trinagulo

```
if l_1> l_2 and l_1> l_3:
  if l_1 < l_2 + l_3:
    print("Sepuede construir un triangulo")
  else:
    print("No se puede contruir un trinagulo")
elif l_2> l_1 and l_2> l_3:
  if l_2 < l_1 + l_3:
    print("Sepuede construir un triangulo")
  else:
    print("No se puede contruir un trinagulo")
elif l_3> l_1 and l_3> l_1:
  if l_3 < l_1 + l_2:
    print("Sepuede construir un triangulo")
  else:
    print("No se puede contruir un trinagulo")
```

Link del notebook: 
https://colab.research.google.com/drive/1aohk3O5l6fLLWTl8CZ_7gphbV3DZck9k?usp=sharing

