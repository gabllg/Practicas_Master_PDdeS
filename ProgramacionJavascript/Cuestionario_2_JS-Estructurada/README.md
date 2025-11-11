# Cuestionario JS-Estructurada
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  


## Ejercicio 1

Escribe un código que determine si una cadenas de caracteres es un palíndromo, sin considerar espacios intermedios ni acentos de la cadena. P.e.: "Dábale arroz a la zorra el abad" sí es un palímdromo.
  
### Respuesta  

~~~
const { Console } = require ("console-mpds");
const console = new Console();

const sentence = console.readString(`Escribe una frase en minúsculas: `);   //dábale arróz a la zórra el abád (31)

let checkedSentence = "";
let letters = 0;

for( i = 0; i < sentence.length; i++){
  if (sentence[i] != " "){
    checkedSentence += sentence[i];
    letters = letters + 1;
  }
  if (sentence[i] === " "){
    checkedSentence += "";
  } 
}

// checkedSentence = Dábalearrozalazorraelabad
// letters = 25

const quitLetter = ["á", "é", "í", "ó", "ú"];
const addLetter = ["a", "e", "i", "o", "u"];
let convertSentence = "";

for (j = 0; j < checkedSentence.length; j++){
  for (k = 0; k < quitLetter.length; k++)
    if (checkedSentence[j] === quitLetter[k]){
      convertSentence += addLetter[k];
    }
    let x = checkedSentence[j];
    if (x != "á" && x != "é" && x != "í" && x != "ó" && x != "ú")
    convertSentence += checkedSentence[j];
}

// checkedSentence = Dabalearrozalazorraelabad
// letters = 25

let palindrome = "Sí es";
 for (let s = 0, f = letters-1; s < letters; s++, f--){
  if (convertSentence[s] != convertSentence[f]){
    palindrome = "NO es";
  } 
}

// for (let s = 0, f = letters-1; s < letters; s++, f--)
//    console.writeln(`${convertSentence[s]} - ${convertSentence[f]}`); 
//    d - d / a - a / b - b / a - a / ...

console.writeln(`Tu frase de ${letters} letras ${palindrome} un palíndromo`);
~~~
    

## Ejercicio 2
Escribe un código que determine si una serie de números positivos (terminada en 0) está ordenada ascendentemente.
  
### Respuesta  
  
~~~
const { Console } = require ("console-mpds");
const console = new Console();

let numberSerie = console.readNumber(`Escribe una serie de números: `);   //123456789

let x = ".";
numberSerie += x;

let inArray = [];
for ( i = 0; i < numberSerie.length; i++){
  if (numberSerie[i] !== x){
    inArray += numberSerie[i];
  }
}

let ascendente = [];
for (j = 0; j < inArray; j++){
  if (inArray[j] <=  inArray[j +1]){
    ascendente += inArray[j];
  }
}
if  (inArray[inArray.length -1] >= inArray[inArray.length -2]){
    ascendente += inArray[inArray.length -1];
  }

if (ascendente.length === inArray.length){
  console.writeln(`la serie de números ${inArray} SÍ es ascendente.`);
} else {
  console.writeln(`la serie de números ${inArray} NO es ascendente.`);
}

~~~

  
## Ejercicio 3

Escribe un código para "adivinar" el número del usuario entre 0 y 1.000.000 inclusive mediante la búsqueda binaria: ¿es igual o mayor que 500.000? Mayor; ¿es igual o mayor que 750.000? ...
  
### Respuesta

~~~

const { Console } = require ("console-mpds");
const console = new Console();

console.writeln(`Piensa en un número del 1 al 1.000 y responde SI o NO:`);  

let digits = console.readNumber(`¿cuantas cifras tiene tu número?`); 
if (digits === 1){
    let oneDigit_1 = console.readString(`Responde si o no: ¿Tu número es menor o igual que 5?`);
    if (oneDigit_1 == "si"){
        let oneDigit_2 = console.readString(`Responde si o no: ¿Tu número es menor o igual que 3?`);
        if (oneDigit_2 == "si"){
            let oneDigit_3 = console.readString(`Responde si o no: ¿Tu número es menor o igual que 2?`);
            if (oneDigit_3 == "si"){
                let oneDigit_4 = console.readString(`Responde si o no: ¿Tu número es el 2?`);
                if (oneDigit_4 == "si"){
                    console.writeln(`¡Bien! El número que habías pensado es el 2.`);  
                };
                if (oneDigit_4 == "no") {
                    console.writeln(`Entonces el número que habías pensado es el 1.`);
                };
            }
            if (oneDigit_3 == "no") {
                console.writeln(`Entonces el número que habías pensado es el 3.`);
            }
        };
        if (oneDigit_2 == "no"){
            let oneDigit_3 = console.readString(`Responde si o no: ¿Tu número es el 4?`);
            if (oneDigit_3 == "si") {
                console.writeln(`¡Bien! El número que habías pensado es el 4.`);
            };
            if (oneDigit_3 == "no") {
                console.writeln(`Entonces el número que habías pensado es el 5.`);
            };
        }
    };
    if ( oneDigit_1 == "no"){
        let oneDigit_2 = console.readString(`Responde si o no: ¿Tu número es menor o igual que 7?`);
        if (oneDigit_2 == "si"){
            let oneDigit_3 = console.readString(`Responde si o no: ¿Tu número es el 7?`);
            if (oneDigit_3 == "si") {
                console.writeln(`¡Bien! El número que habías pensado es el 7.`);
            };
            if (oneDigit_3 == "no") {
                console.writeln(`Entonces el número que habías pensado es el 6.`);
            };
        };
        if (oneDigit_2 == "no") {
            let oneDigit_3 = console.readString(`Responde si o no: ¿Tu número es el 8?`);
            if (oneDigit_3 == "si"){
                console.writeln(`¡Bien! El número que habías pensado es el 8.`);
            };
            if (oneDigit_3 == "no") {
                console.writeln(`Entonces el número que habías pensado es el 9.`);
            };
        };
    };
};


// if (digits === 2) {  La misma estructura partiendo de 50 };
// if (digits === 3) {  La misma estructura partiendo de 500 };


if (digits === 4) {
    console.writeln(`El número que habías pensado es 1.000.`);
};
if (digits > 4){
    console.writeln(`1.000 es el valor máximo. Vuelve a intentarlo.`);
};

// No se me ocurre otra forma de solucionar el código de forma más eficiente sin recurrir a que el usuario introduzca el número directamente, y no veo que tenga sentido que lo haga.

~~~  
  

## Ejercicio 4

Escribe un código que a partir de un número de filas y columnas muestre por pantalla una retícula correspondiente de cuadrados de 5x5 asteriscos rellenos de puntos.
  
### Respuesta

~~~

~~~
  
    
