***Helt nye programmerings-keywords:***       
***Nye termer:*** tilstands-maskine, tilstands-diagram eller state-chart          
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

## Statechart
[https://en.wikipedia.org/wiki/UML_state_machine](https://en.wikipedia.org/wiki/UML_state_machine)
------------------------------------------------
# Opgaven - aflevering på Lectio (ca. 1 uge):
I skal aflevere følgende.
- en kort beskrivelse af programmet. Forklar både state-pattern og hvordan det relaterer sig til strategy pattern. 
- tegn et flowchart, der viser tilstande for programmet
- tegn et statechart
- tegn et klassediagram

Vælg enten opgave 1 eller 2.

### opgave 1
Lav en bold, der ændrer bevægelses-state på følgende måde

- bolden starter i midten af skærmen (500x500) i tilstand A
- tilstand A : bevæger sig til højre.   Hvis x > 400, skiftes til tilstand B
- tilstand B : bevæger sig nedad.       Hvis y > 400 skiftes til tilstand C
- tilstand C : bevæger sig til venstre. Hvis x < 100 skiftes til tilstand D
- tilstand D : bevæger sig op.          Hvis y < 100 skiftes til tilstand A  
- du må gerne lave flere/andre tilstande

Forslag til jeres klient/main kode:
```java
Ball b = new Ball();

void setup(){
  size(500,500);
}

void draw(){
 clear();
 b.update();
 b.display();
}
```


Forslag til hvordan kode ser ud for bold'en:

```java
class Ball{
  float x=250,y=250,bs=20;
  State s = new StateA();

  void setState(State newState){
    s = newState;
  }

  void update(){
    s.update();  
  }

  void display(){
    ellipse(x,y,20,20);  
  }
```

### opgave 2

Lav et selvvalgt program, der implementerer state-pattern
