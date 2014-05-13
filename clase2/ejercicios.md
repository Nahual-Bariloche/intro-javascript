## Ejercicios de Javascript



### Ejercicio "Hola Mundo desde una función"


Hacer que el programa diga "hola mundo" pero usando una función


Concepto introducido: declaración de funciones




### Ejercicio "Jugar a las escondidas"


Hacer que el programa cuente hasta 10 y luego diga "Punto y coma el que no se escondió se embroma"


Concepto introducido: iteración de 10 pasos (for), que el alumno se de cuenta de la ventaja de usar una variable y un ciclo en vez de usar 10 instrucciones



### Ejercicio "Calcular si un año es bisiesto"


Pasar un año como parámetro al argumento y mostrar un mensaje diciendo si es bisiesto o no.
Los años bisiestos son aquellos divisibles por 4 pero no por 100 salvo cuando son divisibles por 400.


Mejora: validar si el argumento que se le pasa al programa es un número usando la función isNaN




### Ejercicio "FizzBuzz"

Imprimir los números del 1 al 100 pero si el número es múltiplo de 3 imprimir Fizz, si es múltiplo de 5 imprimir Buzz y si es múltiplo de ambos imprimir FizzBuzz.

Conceptos introducidos: uso de arrays, for



### Ejercicio "Iterando con Arrays"

Declarar un array con los nombres de 5 compañeros y hacer que imprima todos sus elementos por pantalla


Tip: var cumpas = ["Juan", "Natalia", "Maria"];

Conceptos introducidos: uso de arrays, for



### Ejercicio "Estadísticas de un Array"

Declarar un array con números. Calcular y mostrar por pantalla su valor máximo, mínimo, promedio y cantidad de elementos.

Conceptos introducidos: uso de arrays, for



### Ejercicio "Hola Juan"


Hacer que el programa nos pregunte el nombre y luego diga "Hola" seguido de nuestro nombre.


Conceptos introducidos: variable, input del usuario

Prerequisitos: Instalar prompt => npm install prompt

Modo de uso:

```node
var prompt = require('prompt');

prompt.start();

prompt.get(['nombre', 'email'], function (err, result) {
  
  console.log('Entradas recibidas por consola:');
  console.log('  Nombre: ' + result.nombre);
  console.log('  Email: ' + result.email);
});
```



### Ejercicio "Adivinanza"


Hacer que el personaje piense un número del 1 al 10 y nos pida a nosotros que lo adivinemos y nos diga si acertamos o no. En el caso de que no adivinemos que nos diga cual es el número en el que estaba pensando.


Tip: Usar "Math.random()" para generar un número aleatorio y prompt para pedir que se ingresen datos


Conceptos introducidos: variable, número aleatorio, input del usuario





### Ejercicio "Validar un CUIT"


Ingresar un CUIT por argumento, validarlo y mostrar por pantalla el resultado.


Tip: Buscar en internet cómo se calcula el dígito verificador de un CUIT.

