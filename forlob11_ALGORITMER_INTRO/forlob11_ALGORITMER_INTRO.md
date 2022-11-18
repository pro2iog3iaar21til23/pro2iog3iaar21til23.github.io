***Helt nye programmerings-keywords:*** ...
***Nye termer:*** algoritme, "orden", sorteringsalgoritme
***Vigtige termer ( i allerede kender ):*** pseudokode

------------------------------------------------

# Introduktion til algoritmer ( og datastrukturer)

Vi anvender bl.a. følgende site som materiale:    
[https://www.educative.io/courses/visual-introduction-to-algorithms](https://www.educative.io/courses/visual-introduction-to-algorithms)   

Algoritmer er, som i kan se i videoen på første lektion i ovenstående materiale, opskrifter på "hvordan man gør noget". Det er selvfølgelig en meget bred definition og vi kigger da heller ikke på hvad som helst.   

Vi vil kigge på følgende:
- pseudokode. Når man skriver algoritmer er pseudokode en smart måde at forklare algoritmen, uden at skulle vise hele koden.
- sorteringsalgoritmer
- vurdering af kode-effektivitet (hovedsageligt hastighed)
- datastrukturer (vi har selvfølgelig arrays, men der er andre)
- måske andet ...

------------------------------------------------
Vi laver to opgaver til at starte med.

------------------------------------------------

# Opgave 1 - Pseudokode
## Aflevering : Skriv noget i jeres log-bog

Prøv sammen med en makker at skrive pseudokode til den kort-sortering i ser på animationen nedenfor:

[https://www.educative.io/courses/visual-introduction-to-algorithms/jvR3R](https://www.educative.io/courses/visual-introduction-to-algorithms/jvR3R)

------------------------------------------------

# Opgave 2 - Skriv koden til en sorterings-algoritme
## Aflevering : Skriv noget i jeres log-bog

### del 1:
I skal skriv følgende kode færdig:
```java
void setup(){
 int[] usorteret =  {1,6,3,8,1,3,9,0,1,5};
 int[] sorteret  = new int[usorteret.length];
 //Skriv kode, her, der flytter fra "usorteret" array til "sorteret" array!!!
 printList(usorteret);
 printList(sorteret);
}  

void printList(int[] list){for(int e:list) print(e + " "); println();}
```

### del 2:
Pak jeres sorteringsmetode ned i en funktion:
```java
void setup(){
 int[] usorteret =  {1,6,3,8,1,3,9,0,1,5};
 //I skal skrive koden til funktionen "minSortering"
 int[] sorteret  = minSortering(usorteret);
 printList(usorteret);
 printList(sorteret);
}  

void printList(int[] list){for(int e:list) print(e + " "); println();}
```
