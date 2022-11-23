***Helt nye programmerings-keywords:***         
***Nye termer:***  kørselstid eller afviklingstiden    
***Vigtige termer ( i allerede kender ):***

---------------------------------------------------------

# Køretiden

Afviklingstiden eller køretiden for et program er den tid det tager at afvikle.   
Vi er selvfølgelig interesserede i at lave hurtige programmer og vil derfor gerne kunne vurdere programmets køretid.    
Men køretiden for et program er afhængigt af mange faktorer såsom: harddware, operativsystem, udviklingsmiljøet, programmeringssproget, de forskellig operationer der udføres i koden og de andre programmer der kører på computeren.   
Mange af disse faktorer er ikke de samme hver gang koden afvikles, det er derfor nødvendigt at betragte noget, der ikke varierer hver gang koden afvikles. Derfor vælger man at betragte den del af koden, der dominerer kørselstiden mest.

---------------------------------------------------------

# Køretiden for sorteringsalgoritmer

Når vi kigger på sorteringsalgoritmer - sorterer vi elementer i et array.    
Læsning og skrivning til et array er ret "dyrt".   
Desuden er antallet af læsninger og skrivninger ofte afhængigt af både antallet af elementer i arrayet og sammensætningen.    

Vi vælger derfor at tælle enten:
- "sammenligninger" (sammenligninger af to elementer fra arrayet)
- "ombytninger" (ombytninger af to elementer i arrayet)

---------------------------------------------------------
# Anvendelse af printList

For at tælle "sammenligninger" og "ombytninger" er det nødvendigt at anvende metoden "printList".
Anvend "printList" til at udskrive arrayet for hvert gennemløb... således kan du herefter tælle ombytninger og ræsonnere dig frem til antal sammenligninger.

---------------------------------------------------------

# Opgave 1 - Kørselstid for forløb11-løsning
## Aflevering : Skriv i jeres log-bog

## 1.1
Modificer koden i fra "løsning forløb 11" så du får følgende udskrift:
```
usorteret:1 12 32 5 1 8 9 8 11 17
sorteret :0 0 0 0 0 0 0 0 0 0
usorteret:32 12 32 5 1 8 9 8 11 17
sorteret :1 0 0 0 0 0 0 0 0 0
usorteret:32 12 32 5 32 8 9 8 11 17
sorteret :1 1 0 0 0 0 0 0 0 0
usorteret:32 12 32 32 32 8 9 8 11 17
sorteret :1 1 5 0 0 0 0 0 0 0
usorteret:32 12 32 32 32 32 9 8 11 17
sorteret :1 1 5 8 0 0 0 0 0 0
usorteret:32 12 32 32 32 32 9 32 11 17
sorteret :1 1 5 8 8 0 0 0 0 0
usorteret:32 12 32 32 32 32 32 32 11 17
sorteret :1 1 5 8 8 9 0 0 0 0
usorteret:32 12 32 32 32 32 32 32 32 17
sorteret :1 1 5 8 8 9 11 0 0 0
usorteret:32 32 32 32 32 32 32 32 32 17
sorteret :1 1 5 8 8 9 11 12 0 0
usorteret:32 32 32 32 32 32 32 32 32 32
sorteret :1 1 5 8 8 9 11 12 17 0
usorteret:32 32 32 32 32 32 32 32 32 32
sorteret :1 1 5 8 8 9 11 12 17 32
```
## 1.2
Hvor mange gange udskrives array {9,8,7,6,5,4,3,2,1,0} inden det er sorteret?
## 1.3
Hvor mange sammenligninger laves pr. gang arrayet i 1.2 ,udskrives?
## 1.4
Hvor mange sammenligninger giver det i alt inden arrayet i 1.2 er sorteret?
## 1.5
Hvis arrayet består af N omvendt sorterede elementer, hvor mange sammenligninger koster en sortering så?

---------------------------------------------------------

# Opgave 2 - Kørselstid for bubblesort
## Aflevering : Skriv i jeres log-bog

## 2.1
Modificer bubble-sort koden så du får følgende sorterings-udskrift, hvis arrayet er {1,8,4,6,5}:
```
1 8 4 6 5
1 4 6 5 8
1 4 5 6 8
```
## 2.2
Hvor mange gange udskrives array {9,8,7,6,5,4,3,2,1,0} inden det er sorteret?
## 2.3
Hvor mange sammenligninger laves pr. gang arrayet i 2.2 ,udskrives?
## 2.4
Hvor mange sammenligninger giver det i alt inden arrayet i 2.2 er sorteret?
## 2.5
Hvis arrayet består af N omvendt sorterede elementer, hvor mange sammenligninger koster en sortering så?
