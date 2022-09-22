# Forløb 5
## GUIHandleren : Få et objekt til at holde styr på alle de andre

Ideen med GUIHAndleren er at have en objekt der kan bruges til at holde styr på alle de andre komponenter.
Hvis alle komponenter knapper, tekstfelter, radio-buttons osv. aller nedarver fra en fælles komponent-klasse - kan alle indsættes i samme liste - og man kan håndtere alt vha. loops.

Se følgende kode - kan i se det er noget mere ovberskueligt!:
```java
GUIHandler guiHandler = new GUIHandler();

void setup(){
  size(500,500);
  guiHandler.createButton(100,10,100,50);
  guiHandler.createTextField(100,100,100,50);
}

void draw(){
  guiHandler.displayAll();
}

void mousePressed(){
  guiHandler.detectClick();
}

void mouseReleased(){
  guiHandler.detectRelease();
}

void keyPressed(){
  guiHandler.detectKeyPressed();
}
```

GUIHandleren kan nu f.eks. se således ud:

```java
class GUIHandler{
  ArrayList<Komponent> mineKomponenter = new ArrayList<Komponent>();

  Button createButton(int x, int y, int w, int h){
    Button b = new Button(x,y,w,h);
    mineKomponenter.add(b);
    return b;
  }

  TextField createTextField(int x, int y, int w, int h){
    TextField t = new TextField(x,y,w,h);
    mineKomponenter.add(t);
    return t;  
  }

  void displayAll(){
    for(Komponent k : mineKomponenter){
      k.display();
    }
  }

  void detectClick(){
    for(Komponent k : mineKomponenter){
      k.detectClick();
    }
  }

  void detectRelease(){
    for(Komponent k : mineKomponenter){
      k.detectRelease();
    }  
  }

    void detectKeyPressed(){
    for(Komponent k : mineKomponenter){
      k.detectRelease();
    }  
  }

}
```
