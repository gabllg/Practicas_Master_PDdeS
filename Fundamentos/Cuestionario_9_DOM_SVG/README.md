# Cuestionario 5_Complejidad
Universo Santa Tecla - Master en Programación y Diseño Software
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
  
## Ejercicio 1

Escribe una expresión XPath para obtener el nombre del país de capital con mayor latitud a partir de countries.xml (disponible desde la documentación)  
[manager-countries](https://github.com/USantaTecla-tech-xml/manager-countries/blob/master/0.0.dataLanguages/v0.0/data.xml)  
  
### Respuesta  

/country [not (preceding-sibling::latlng/text() >= text())  
and not(following-sibling::latlng/text() >= text())]
  
  
No hay coincidencias, no pude solucionarlo.
  
  
## Ejercicio 2
Describe razonadamente en base a los conceptos de temas anteriores las consecuencias de la ausencia de un estándar como, por ejemplo, antes de la especificación de DOM.
  
### Respuesta  
  
Sería muy complicado y tedioso poder acceder a una información concreta dentro de un documento, y el DOM permite una solicitud de búsqueda de una información concreta dentro de un documento.
    
  
## Ejercicio 3

Describe en 50 palabras las similitudes y diferencias entre los lenguajes SVG y HTML.
  
### Respuesta
SVG se compone de elementos basados en coordenadas para crear objetos gráficos, y html se basa en ordenar información para poder ser publicada. Ambos lenguajes siguen una estructura jerárquica basada en elementos y subelementos.
  
  
  
## Ejercicio 4


Escribe un documento SVG para mostrar un cuadrado que encierra un círculo.
  
### Respuesta
''' 
<svg xmlns="http://www.w3.org/2000/svg" width="400" height="400" fill="none">  
<rect width="120" height="120" fill="none" stroke="#000000"/>  
<circle cx="60" cy="60" r="60" fill="d9d9d9" stroke="#000000"/>  
</svg>    
'''  
  
    
## Ejercicio 5  
  
Cuántos y cuáles son los nodos del arbol DOM del siguiente documento XML:  
'''
<?xml version="1.0" encoding="UTF-8"?>
  <elementoMixto atributo="informacion"> informacion 
    <subElemento atributo="informacion"> informacion </subElemento> informacion 
    <subElemento atributo="informacion"> informacion</subElemento> informacion 
  </elementoMixto> 
'''

### Respuesta  
  
3: un "elementoMixto" y 2 "subElemento".