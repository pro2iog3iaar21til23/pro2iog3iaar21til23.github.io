***Helt nye programmerings-keywords:***........         
***Nye termer:***.............................. bubblesort og api        
***Vigtige termer ( i allerede kender ):***.... pseudokode       

------------------------------------------------
I dette forløb skal vi først lave et lille array - API (application programming interface). API'et er bare nogle funktioner vi kommer til at bruge når vi skal bygge forskellige sorterings alogoritmer.

Herefter skal vi prøve at bygge sorteringsalgoritmen bubblesort.

------------------------------------------------
# Opgave 1 - Array-API
## Aflevering : Skriv i jeres log-bog

I skal bygge følgende funktioner ( som i skal bruge senere ).

1. *int minIndex(int[] list)*:
Denne funktion skal modtage en array "liste" og returnere index på det mindste tal i "liste".

2.  *int maxIndex(int[] list)*:
Denne funktion skal modtage en array "liste" og returnere index på det største tal i "liste".

3. *void swap(int[] list, int i1, int i2):*
Denne funktion modtager arrayet "liste", index i1 og index i2. Den retunerer ikke noget med bytter om på elementet på plads i1 og elementet på plads i2.

void printList(int[] list) { for (int e : list) print(e + " ");println();}


------------------------------------------------
# Opgave 2 - Bubblesort
## Aflevering : Skriv i jeres log-bog

I skal nu prøve at bygge "bubble-sort". Det er vigitigt i anvender funktion "swap" fra første opgave.   

En mulig pseudokode (måske lidt sjusket):

```
1. Hvis list[i] > list[i+1], byt rundt
2. Sæt i=i+1 og gentag 1 - indtil enden af arrayet
3. Hvis antallet af "swaps" > 0 gentag ellers Stop!  

```
