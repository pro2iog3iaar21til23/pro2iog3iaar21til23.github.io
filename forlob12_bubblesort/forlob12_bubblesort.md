***Helt nye programmerings-keywords:***         
***Nye termer:***  bubblesort og api        
***Vigtige termer ( i allerede kender ):*** pseudokode       

------------------------------------------------
I dette forløb skal vi først lave et lille API(application programming interface). API'et er bare nogle array-funktioner vi skal anvende når vi bygger vores sorteringsalgoritmer.

Herefter skal vi prøve at bygge sorteringsalgoritmen bubblesort.

------------------------------------------------
# Opgave 1 - Array-API
## Aflevering : Skriv i jeres log-bog

I skal bygge følgende funktioner, som i skal bruge senere.

```
int minIndex(int[] list):     
Denne funktion skal modtage en array "liste"
og returnere index på det mindste tal i "liste".

int maxIndex(int[] list):    
Denne funktion skal modtage en array "liste"
og returnere index på det største tal i "liste".

void swap(int[] list, int i1, int i2):    
Denne funktion modtager arrayet "liste", index i1 og index i2.
Den retunerer ikke noget men bytter om på element i1 og i2.

void printList(int[] list):
Udskriver en array kaldet "liste" på en linje.
```

------------------------------------------------
# Opgave 2 - Bubblesort
## Aflevering : Skriv i jeres log-bog

I skal nu prøve at bygge "bubble-sort". Anvend funktionerne "swap" og "printList" fra første opgave.   

Pseudokode (måske lidt sjusket):

```
1. Hvis list[i] > list[i+1], byt rundt
2. Sæt i=i+1 og gentag (1) - indtil i < "liste længde"-1 er falskt.
3. Hvis antallet af "swaps" > 0 gentag ellers Stop!  

```

Jeres setup skal se således ud:
```java
void setup(){
  int[] list = { 1,2,6,3,8,1,2,9,7,6};
  bubbleSort(list);
  printList(list);
}
```
