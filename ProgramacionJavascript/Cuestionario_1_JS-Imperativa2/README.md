# Cuestionario JS-Imperativa2
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
  
## Ejercicio 1

¿Qué valores deben tener las variables "x", "y" y "z" para que la expresión "x === y === z" se evalúe "true"?
  
### Respuesta  

True. ejemplo:  
  
""  
const x = true;  
const y = true;  
const z = true;  
console.writeln(x===y===z);  
""  

// Corregido: no contemplé otras opciones más allá de encontrar una solución, centrándome en un caso particular. Por ejemplo: *valor distinto* === *valor distinto* === false
    
  
## Ejercicio 2
¿Qué valores deben tener las variables "x", "y" y "z" para que la expresión "x == y == z" se evalúe "true"?
  
### Respuesta  
  
También True;  si en el ejemplo anterior eran del mismo tipo y valor, en este ejemplo seguiran siendo del mismo *valor.* Ejemplo:  // Corregido: confundí la relación de igualdad de "==".
  
""  
const x = true;  
const y = true;   
const z = true;  
console.writeln(x==y==z);  
""  

En los operadores relacionales de las reglas de coerción, *true* con *true* siempre va a dar *true*, y al no tener distintos niveles de precedencia tienen la misma asociatividad (left -to-right).  

  
## Ejercicio 3

¿Qué valores deben tener las variables "x", "y" y "z" para que la expresión "x < y < z" se evalúe "true"?  
  
### Respuesta
En este caso mantienen el nivel de asociatividad y precedencia, pero según las reglas de Coerción, *True < True = False*, y *False < True = True.* Por lo que si:  

'''    
const x = true;  
const y = true;  
const z = true;  
console.writeln(x < y < z);  
'''    
entonces:  
  
True *(x)* < True *(y)* = False  
False < True *(z)* = **True**  
  
  
## Ejercicio 4


Determina todos los posibles órdenes de evaluación de la siguiente expresión "12+34+5*6"  
// Corregido: La fórmula es distinta porque en la página web de la escuela interpreta los * como en los archivos .md, y aparecen en cursiva. Copio los enunciados desde la web hasta este .md para resolverlos y no trajo los símbolos *. La expresión planteada es **"1 * 2 + 3 * 4 + 5 * 6"**
  
### Respuesta

Solo veo un orden posible:  
Primero 5 * 6, *(nivel 15 de precedencia)* = 30  
Después, dos operadores "+" *(nivel 14 de precedencia)* tienen una asociatividad left-to-right,  
por lo tanto:   
12 + 34 + 30 = 76
  
    
## Ejercicio 5  
  
Determina todos los posibles órdenes de evaluación de la siguiente expresión "true && false || false && true || true && false"  

### Respuesta  
  
Los operadores "&&" lógicos tienen un nivel de precedencia mayor *(7)* que los lógicos "||" *(6)*;    
Comprobando las reglas de Coerción,    
la expresión se reduciría a: *false || false || false*, por lo tanto:  
false || false || false = false  