# Practica JS-Estructurada 2
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
  
## Ejercicio - Menú para consultar una lista de paises
  

  
### Código  
    
~~~
const { Console } = require("console-mpds");
const console = new Console();

const countries = ["Escocia", "Gales", "Inglaterra", "Irlanda", "Italia", "Francia"];

let option = console.readNumber("Elige una de las siguientes opciones: \n\t 1 = Lista de paises \n\t 2 = Comprobar país  \n\t 3 = Salir \n");

switch (option) {
    case 1:
        list = [];
        for (i = 0; i < (countries.length - 2); i++) {
            list += countries[i] + ", ";
        };
        list += countries[countries.length - 2] + " y " + countries[countries.length - 1] + ".";
        console.writeln(list);
        break;

    case 2:

        let checking = console.readString("¿Qué país quieres comprobar?");
        let inList = 0;
        
        for (k = 0; k < (countries.length); k++) {
            if (checking === countries[k]) {
                inList = 1;
            };
        };
        console.writeln(`Tu país ${inList === 1 ? "Sí" : "NO"} esta en la lista.`);

    case 3:
        break;
};

if (option > 3) {
    console.writeln("Error: debes elegir entre los números 1, 2 y 3.");
};

~~~ 
    

    