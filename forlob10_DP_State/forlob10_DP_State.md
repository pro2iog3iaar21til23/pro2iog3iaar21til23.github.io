***Helt nye programmerings-keywords:***       
***Nye termer:*** tilstands-maskine      
***Vigtige termer ( i allerede kender ):*** flowdiagram      

------------------------------------------------
# Design Pattern - State Pattern
Vi har nu kigget på "Strategy pattern" og det er derfor næsten synd at forlade "design patterns" uden at have kigget "state pattern".
Begge patterns anvender komposition til at indkapsle en tilstand. Men hvor vi selv skiftede tilstand i "strategy pattern", skifter tilstanden i et "state pattern" sig selv ud med en ny tilstand!!

------------------------------------------------
## State pattern
[https://refactoring.guru/design-patterns/state](https://refactoring.guru/design-patterns/state)

## Flowchart
Vi anvender et flowchart til at beskrive programmets tilstande, det er nemmest
[https://en.wikipedia.org/wiki/Flowchart](https://en.wikipedia.org/wiki/Flowchart)

------------------------------------------------
# Opgaven - aflevering på Lectio (ca. 1 uge):
Vælg en af nedenstående opgaver, i begge tilfælde skal i aflevere følgende.
- en kort beskrivelse af programmet
- et flowdiagram, der viser tilstande for programmet
- koden

## Vælg en af følgende opgaver:

### opgave 1 - selvvalgt program, der implementerer state-pattern

### opgave 2 - en bold, der ændrer bevægelses-state på følgende måde

- bolden starter i midten af skærmen (500x500) i tilstand A
- tilstand A : bevæger sig til højre.   Hvis x > 400, skiftes til tilstand B
- tilstand B : bevæger sig nedad.       Hvis y > 400 skiftes til tilstand C
- tilstand C : bevæger sig til venstre. Hvis x < 100 skiftes til tilstand D
- tilstand D : bevæger sig op.          Hvis y < 100 skiftes til tilstand A  
