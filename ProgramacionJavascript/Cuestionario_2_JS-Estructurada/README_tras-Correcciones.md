# Cuestionario JS-Estructurada
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  


Tras ver las correcciones, en estos ejercicios me obcequé con el uso de los Arrays, dado que no llegaba a comprenderlos por completo. También debo volver a repasar la teoría anterior al posponer varias veces la continuidad del máster.


## ejemplo de los ejercicios corregidos: Ejercicio 3

Escribe un código para "adivinar" el número del usuario entre 0 y 1.000.000 inclusive mediante la búsqueda binaria: ¿es igual o mayor que 500.000? Mayor; ¿es igual o mayor que 750.000? ...
  
### Respuesta de PapaPauCla:

~~~
const { Console } = require ("console-mpds");
const console = new Console();

let minNumber = 0;
let maxNumber = 1000000;
let userNumber;
let response;


do {
    userNumber = ((minNumber + maxNumber) - ((minNumber + maxNumber) % 2 )) /2;
    do {
        response = console.readString(`El número que has pensado es "+" , "*" o "-" que ${userNumber}?`)
    } while (response != "+" && response != "*" && response != "-");
    switch(response){
        case "+":
            minNumber = userNumber + 1;
            break;
        case "-":
            maxNumber = userNumber -1;
            break;
    }
    if (minNumber === maxNumber){
        response = "*";
        userNumber = minNumber;
    }
} while (response != "*"){
    console.writeln(`Tu número es el ${userNumber} !!`);
};
~~~