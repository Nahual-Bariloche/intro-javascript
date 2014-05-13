# Referencia básica de javascript

## Variables y tipos de datos

Una variable se define usando la palabra clave "var"

```node
var a;
```

Utilizando el = puedo asignarle un valor a la variable. Esta puede tomar distintos tipos de datos.
Por ejemplo, declarar una variable edad y asignarle el número 18:

```node
var edad = 18;			// variable numérica (number)
```

Otros ejemplos con distintos tipos de datos:

```node
var peso = 52.5;		// variable numérica (number)

var nombre = "Juan";	// cadena de caracteres (string)

var esMayorDeEdad = true;	// variable booleana (boolean)
```


## Mostrar por pantalla

El método log del objeto console se usa para imprimir por pantalla

```node
console.log("Hola mundo");
```


## Operadores matemáticos

Suma, resta, multiplicación, división:

```node
console.log(4 - 2);		// muestra por pantalla: 2
console.log(4 + 2);		// muestra por pantalla: 6
console.log(4 * 2);		// muestra por pantalla: 8
console.log(4 / 2);		// muestra por pantalla: 2
```

Mayor y menor:
```node
console.log(2 > 4);		// muestra por pantalla: false
console.log(2 < 4);		// muestra por pantalla: true
```

El operador == permite comparar si un objeto es igual a otro, por ejemplo:
```node
console.log(2 == 4);	// muestra por pantalla: false
console.log(2 == 2);	// muestra por pantalla: true

console.log("gato" == "perro");	// muestra por pantalla: false
console.log("a" == "a");		// muestra por pantalla: true
```

El operador != permite comparar si un objeto es diferente a otro, por ejemplo:
```node
console.log(2 != 4);	// muestra por pantalla: true
console.log(2 != 2);	// muestra por pantalla: false

console.log("perro" != "gato");	// muestra por pantalla: true
```

Calcular el resto de una división:

```node
console.log(8 % 2);		// muestra por pantalla: 0 (8 es divisible por 2)
console.log(7 % 2);		// muestra por pantalla: 1 (7 es 2 * 3 con resto 1)
console.log(8 % 3);		// muestra por pantalla: 2 (8 es 3 * 2 con resto 2)
```



*Math.random()* devuelve un número (pseudo) aleatorio entre 0 y 1

```node
console.log(Math.random());		// muestra por pantalla por ejemplo:  0.5335811674594879
```



## Control del flujo


### Condicional: if...else...


Ejecuta una sentencia si una condición específicada es evaluada como verdadera. Si la condición es evaluada como falsa, otra sentencia puede ser ejecutada.

```node
if(a > b){
	console.log("a es mayor a b");
} else {
	console.log("a es menor o igual a b");
}
```

En este ejemplo si a fuera 2 y b 1 se imprime por pantalla: a es mayor a b.
En cambio si a fuera 1 y b 2 se imprime por pantalla



### Ciclos: for

Permite ejecutar una o más sentencias una cantidad determinadas de veces. 

El ciclo se ejecuta hasta que se cumpla la condición de finalización, por ejemplo para mostrar por pantalla 10 veces puedo usar lo siguiente:
```node
for(var i = 0; i < 10; i++)
{
	console.log("Esto se va a imprimir por pantalla 10 veces");
}
```

Imrpimir los números del 1 al 10:

```node
for(var i = 1; i <= 10; i++)
{
	console.log(i);
}
```



## Funciones

```node
function holaMundo()
{
	console.log("Hola mundo");
}

function sumar(a, b)
{
	return a + b;
}
console.log(sumar(2,3));	// imprime por pantalla: 5
```



## Tipos de datos

```node
var edad = 18;			
console.log(typeof(edad));		// muestra por pantalla: number

var peso = 52.5;
console.log(typeof(nombre));	// muestra por pantalla: string

var nombre = "Juan";	
console.log(typeof(peso));		// muestra por pantalla: number

var esMayorDeEdad = true;
console.log(typeof(esMayorDeEdad));	// muestra por pantalla: boolean

console.log(typeof(nodefinida));	// muestra por pantalla: undefined
```



### Conversión de tipos


parseInt(string)  Toma una cadena de caracteres y devuelve su conversión a número, si la cadena de caracteres no es un número devuelve NaN.

```node
console.log(parseInt("5"));   // muestra por pantalla: 5

cosole.log(parseInt("hola"));    // muestra por pantalla: NaN
```





## Arrays

Este tipo de dato permite trabajar con vectores o matrices.
Se define utilizando corchetes y los elementos separados por coma, por ejemplo:

```node
var edades = [14, 15, 16, 17, 18];
```

Se accede a los elementos particulares usando corchetes y el número de elemento al que quiero acceder comenzando por 0 para el primer elemento. Por ejemplo:

```node
var bebidas = ["Café", "Té", "Chocolate"];
console.log(bebidas[0]);	// muestra por pantalla: Café
console.log(bebidas[1]);	// muestra por pantalla: Té
console.log(bebidas[2]);	// muestra por pantalla: Chocolate

bebidas[0] = "Mate";		// asigno el valor "Mate" al primer elemento
console.log(bebidas[0]);	// muestra por pantalla: Mate
```

Se obtiene la cantidad de elementos del array usando la propiedad *length*

```node
var edades = [14, 15, 16];
console.log(bebidas.length);	// muestra por pantalla: 3
```



## Pasar argumentos al programa

Cuando se ejecuta un programa de node por consola se le pasa como argumento el nombre del archivo a ejecutar, por ejemplo para ejecutar un archivo llamado test.js

```
node test.js
```

Pero también puedo pasar más parámetros, por ejemplo:

```
node test.js argumento
```

Esos argumentos pueden ser capturados para usar en el programa usando process.argv

```node
console.log(process.argv[0]);	// imprime por pantalla: node
console.log(process.argv[1]);	// imprime por pantalla: test.js
console.log(process.argv[2]);	// imprime por pantalla: argumento
```

