# Practica JS-Estructurada 2
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
  
## Ejercicio - Estaciones del año
  

  
### Código  
    
~~~
const { Console } = require ("console-mpds");
const console = new Console();

const enterDay = console.readNumber("Escribe un día del 1 al 30: "); 
const enterMonth = console.readNumber("Escribe un mes del 1 al 12: "); 

const monthTime = ["primeros", "mediados", "finales"];
let daysOnMonth;
if (enterDay >= 1 && enterDay <= 10){
  daysOnMonth = monthTime[0]; // primeros
};
if (enterDay >= 11 && enterDay <= 20){
  daysOnMonth = monthTime[1]; // mediados
};
if (enterDay >= 21 && enterDay <= 30){
  daysOnMonth = monthTime[2]; // finales
};

const seasons = ["la Primavera", "el Verano", "el Otoño", "el Invierno"];
let seasonName;
if (enterMonth >= 3 && enterMonth <= 5){
  seasonName = seasons[0];
}
if (enterMonth >= 6 && enterMonth <= 8){
  seasonName = seasons[1];
}
if (enterMonth >= 9 && enterMonth <= 11){
  seasonName = seasons[2];
}
if (enterMonth === 12 || enterMonth <= 2 ){
  seasonName = seasons[3];
};

const seasonParts = ["al principio de", "en mitad de", "al terminar"];
let seasonTime;
if (enterMonth %3 === 0){
  seasonTime = seasonParts[0]; 
};
if (enterMonth %3 === 1){
  seasonTime = seasonParts[1]; 
};
if (enterMonth %3 === 2){
  seasonTime = seasonParts[2]; 
};

const allMonths = [
  "Enero","Febrero","Marzo","Abril",
  "Mayo","Junio","Julio","Agosto",
  "Septiembre","Octubre","Noviembre","Diciembre"];

let nameMonth = allMonths[(enterMonth - 1)];

console.writeln(`el día ${enterDay} del ${nameMonth} cae a ${daysOnMonth} de mes y ${seasonTime} ${seasonName}`);
~~~ 
    

    