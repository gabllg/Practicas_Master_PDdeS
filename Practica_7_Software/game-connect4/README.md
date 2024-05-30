# Connect4
Universo Santa Tecla  
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  

## index

## domainModel  

![connect4](./docs/images/conecta4.jpg)  

[WIKI](https://es.wikipedia.org/wiki/Conecta_4)

[Youtube](https://www.youtube.com/watch?v=JBSbiilzg9U)

Vocabulary

![Vocabulary](./docs/images/Practica_7_Complejidad_Diagrama_Clases_Conecta4_V3.png)  
  
### Código UML  
  
@startuml  
  
class Game  
class Board  
class Disk  
Class Gap  
Class Red  
Class Yellow  
Class Turn  
Class Connection  
Class Y  
Class X  
Class Position  
class Player  
  
Game *-down-> "2" Player  
Player *-down-> "42" Disk  
Disk *-down-> "21" Red  
Disk *-down-> "21" Yellow  
Red .down.> Turn  
Yellow .down.> Turn  
Red "4" -down-> Connection  
Yellow "4" -down-> Connection  
Gap -left- Disk  
Game *-down-> Board  
Board *-down-> "7x6" Gap  
Gap <|-down-  X  
Gap <|-down-  Y  
X <-down- "1..7" Position  
Y <-down- "n+1" Position  
Turn -right- Position  
Position -down-> Connection  
  
@enduml  
  
![Instrucciones]()  
  
![Instrucciones]()  
  
 
