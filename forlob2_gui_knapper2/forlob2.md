# Knapper lavet til et bibliotek - del.2

Det er vigtigt at være opmærksom på at ens kode skrives på en helt bestemt måde hvis den skal kunne anvendes fra et bibliotek.
Hvis knappen kun skal laves en gang, og ikke skal genbruges kan koden se således ud for en såkaldt "toggle-knap".

```java
int      knapX=100, knapY=100, knapB=100, knapH = 40;
boolean  knapOn = false;  

void setup(){
  size(500,500);
}


void draw(){
  //tegn knap
  if(knapOn){
    fill(200,200,50);  
  }else{
    fill(100);
  }
  rect(knapX,knapY,knapB,knapH);
}

void mousePressed(){
  if(mouseX>knapX && mouseX<(knapX+knapB) && mouseY>knapY && mouseY<(knapY+knapH)){
    knapOn = !knapOn;
  }
}
```
