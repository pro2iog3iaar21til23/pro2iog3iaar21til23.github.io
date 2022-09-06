# Forløb 5
## Lav et tekstfelt

Et tekstfelt er en absolut nødvendighed i alle gui-frameworks.    
Der er desuden mange forkskellig typer teskfelter.     

Det i skal lave er et meget simpelt tekstfelt, der som minimum skal opfylde følgende krav:

- Når man trykker på en tast på keyboardet skal den rigstreres og tilføjes til indeholdet i tekstfeltet
- Hvis man trykker på slet ( dvs. backspace ) skal det sidste tegn i tekstfeltet slettes
- Man skal kunne "vælge" tekstfeltet ved at klikke på det og "fravælge" det ved at klikke et andet sted
- Kun hvis tekstfeltet er valgt skal det være muligt at skrive i det

Nedenfor ses noget kode, som i gerne må genbruge i jeres tekstfelt.    
Vær dog sikker på i forstår koden inden i anvender den:

```java
String content = "";

void setup(){
   size(500,500);
}

void draw(){
  clear();
  text(content,100,250);
}

void keyPressed(){
  if(keyCode != 8){
    content += key;
  }else{
    content = content.substring(0,content.length()-1);  
  }
}
```
