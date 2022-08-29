# Radio button - Byg en "Radio button" med tre knapper

I skal nu udvide jeres bibliotek fra sidst med en ny knap-type. En såkaldt "radio button".

[https://en.wikipedia.org/wiki/Radio_button](https://en.wikipedia.org/wiki/Radio_button)

Kravet til knappen er følgende:

- skal fungere som en almindelig Radio button, se ovenfor
- subklasse til jeres super-klasse "Knap" eller måske har i lavet en superklasse kaldet "Komponent"
- skal indeholde 3 options (kan måske laves af tre almindelige knapper)
- man skal kunne sætte tekster på de tre options
- man skal kunne få info om knappens tilstand på et hvert tidspunkt. Altså få at vide hvilken option der er valgt

Se et eksempel nedenfor:

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ct2pNKVozhw?rel=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Lidt inspiration

Nedenfor ses koden, der anvender min radio-button, dvs. den i ser i videoen:

```java
int counter = 0;
Radio3Knap r3;

void setup(){
  size(500,500);
  r3 = new Radio3Knap(30,30,90,150);
}

void draw(){
  clear();
  
  r3.display();
  
  fill(255);
  text("v-1 er tændt " + counter + " gange",10,300);
}

void mousePressed(){
  if(r3.knapPressed() && r3.valg1){
    counter++;  
  }  
}

void mouseReleased(){
  r3.knapReleased();
}


````
