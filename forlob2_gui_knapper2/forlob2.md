# Knapper lavet til et bibliotek - del.2

Det er vigtigt at være opmærksom på at ens kode skrives på en helt bestemt måde hvis den skal kunne anvendes fra et bibliotek.
Hvis knappen kun skal laves en gang, og ikke skal genbruges kan koden se således ud for en såkaldt "toggle-knap".

```java
// Dette er kode der viser en toggle-knap
// Men koden er IKKE EGNET TIL ET BIBLIOTEK !!!

int      knapX=10, knapY=30, knapB=120, knapH = 40;
boolean  knapOn       = false;  
boolean  knapClicked  = false;

int      counter = 0;

void setup(){
  size(500,500);
}


void draw(){
  clear();
  
  //tegning af knap
  textSize(30);
  if(knapOn){
    fill(200);
    rect(knapX,knapY,knapB,knapH);
    fill(255);
    text("tændt",knapX+10,knapY+30);    
  }else{
    fill(100);
    rect(knapX,knapY,knapB,knapH);
    fill(200);
    text("slukket",knapX+10,knapY+30);
  }
  
  //ikke en del af knappen - men bare en der udskrivning af antal gange man tænder knappen!
  fill(255);
  text("knap har været tændt " + counter + " frames",10,300);

  //ikke en del af knappen -  men bare optælning af antal gange man tænder knappen!
  if(knapOn){
    counter++;  
  }

}

void mousePressed(){
  
  //registrering af klik på knap
  if(mouseX>knapX && mouseX<(knapX+knapB) && mouseY>knapY && mouseY<(knapY+knapH)){
    knapOn = !knapOn;
  }
 
  
}
```
