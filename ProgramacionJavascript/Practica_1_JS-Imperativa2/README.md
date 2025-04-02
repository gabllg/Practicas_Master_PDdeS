# Cuestionario JS-Imperativa2
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
  
## 0-multiplicationTable
  
Dame un número:  76  
76 * 1 = 76  
76 * 2 = 152  
76 * 3 = 228  
76 * 4 = 304  
76 * 5 = 380  
76 * 6 = 456  
76 * 7 = 532  
76 * 8 = 608  
76 * 9 = 684  
76 * 10 = 760  
  
### Código  
    
~~~
const { Console } = require ("console-mpds");
const console = new Console();

const number = console.readNumber("Escribe un número? ");
let x = 1;
let result = (x) * number;
console.writeln(`
${number} x  ${x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
${number} x  ${++x}  =  ${x*result};
`);
~~~ 
    
## 1-integerDivision

Dame el dividendo:  21  
Dame el divisor:  5  
21 / 5 = 4 y sobran 1  
    
### Código
  
~~~
const { Console } = require ("console-mpds");
const console = new Console();

const dividend = console.readNumber("Cual es el dividendo? "); //21
const divider = console.readNumber("Cual es el divisor? "); //5
const result = (dividend / divider) - (dividend / divider % 1);
const rest = dividend % divider;
console.writeln(`${dividend} /  ${divider}  =  ${result}, y me sobran ${rest};`);
~~~    
    
## 2-percentage
  
Dame el tanto por ciento (sin %):  21   
21% = 21 · 1 / 100 = 21 · 0,01 = 0.21   
Dame la cantidad:  1000  
21%  · 1000 = 210  
    
### Código
  
~~~
const { Console } = require ("console-mpds");
const console = new Console();

const perCent = console.readNumber("Escribe el tanto por ciento: "); //21
const calculatePerCent = perCent * 0.01;
console.writeln(` ${perCent}% = ${perCent} · 0,01 = ${calculatePerCent}`);

const number = console.readNumber("Escribe la cifra total: "); //1000
console.writeln(`El ${perCent}% de ${number} es ${calculatePerCent * number}.`);
~~~     
    
## 3-even
  
Escribe un número?  23  
El numero 23 es impar  
  
### Código
  
~~~
const { Console } = require ("console-mpds");
const console = new Console();

const number = console.readNumber("Escribe un número: "); 
const odd = (number % 2) === 1 ?  `im` : `` ;
console.writeln(`El número ${number} es ${odd}par.`);
~~~    
    