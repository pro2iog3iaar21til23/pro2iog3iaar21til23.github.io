# Knapper lavet til et bibliotek - del.2

Det er vigtigt at være opmærksom på at ens kode skrives på en helt bestemt måde hvis den skal kunne anvendes fra et bibliotek.
Hvis knappen kun skal laves en gang, kan koden se anderledes ud!!.

## Kode til almindelig knap - men IKKE EGNET TIL BIBLIOTEK

```java
// Dette er kode der viser en almindelig-knap
// Men koden er IKKE direkte EGNET TIL ET BIBLIOTEK !!!

//DEL AF KNAP
int      knapX=10, knapY=30, knapB=120, knapH = 40;
boolean  knapOn = false;

//IKKE DEL AF KNAP
int      counter = 0;

void setup(){
  size(500,500);
}


void draw(){
  clear();
  
  //DEL AF KNAPPEN - tegning af knap
  textSize(30);
  if(knapOn){
    fill(200);
    rect(knapX,knapY,knapB,knapH);
    fill(255);
    text("tryk !",knapX+10,knapY+30);    
  }else{
    fill(100);
    rect(knapX,knapY,knapB,knapH);
    fill(200);
    text("tryk !",knapX+10,knapY+30);
  }
  
  //IKKE DEL AF KNAP - udskrivning af counter!
  fill(255);
  text("knap er tændt " + counter + " gange",10,300);
}

void mousePressed(){
  //DEL AF KNAP - registrer klik
  if(mousePressed && mouseX>knapX && mouseX<(knapX+knapB) && mouseY>knapY && mouseY<(knapY+knapH)){
    knapOn = true;
  }  
  
  //IKKE DEL AF KNAP - optælning af counter!
  if(knapOn){
    counter++;  
  }
  
}

void mouseReleased(){
  //EN DEL AF KNAP - sluk knappen når der gives slip
  knapOn = false;
}
```

## Kode til toogle-knap - dog IKKE EGNET TIL BIBLIOTEK

```java
// Dette er kode der viser en toggle-knap
// Men koden er IKKE direkte EGNET TIL ET BIBLIOTEK !!!

//DEL AF KNAP
int      knapX=10, knapY=30, knapB=120, knapH = 40;
boolean  knapOn = false;

//IKKE DEL AF KNAP
int      counter = 0;

void setup(){
  size(500,500);
}


void draw(){
  clear();
  
  //DEL AF KNAPPEN - tegning af knap
  textSize(30);
  if(knapOn){
    fill(200);
    rect(knapX,knapY,knapB,knapH);
    fill(255);
    text("tryk !",knapX+10,knapY+30);    
  }else{
    fill(100);
    rect(knapX,knapY,knapB,knapH);
    fill(200);
    text("tryk !",knapX+10,knapY+30);
  }
  
  //IKKE DEL AF KNAP - udskrivning af counter!
  fill(255);
  text("knap er tændt " + counter + " gange",10,300);
}

void mousePressed(){
  //DEL AF KNAP - registrer klik
  if(mousePressed && mouseX>knapX && mouseX<(knapX+knapB) && mouseY>knapY && mouseY<(knapY+knapH)){
    knapOn = !knapOn;
  }  
  
  //IKKE DEL AF KNAP - optælning af counter!
  if(knapOn){
    counter++;  
  }
  
}

void mouseReleased(){

}
```

# FLYT DINE KNAPPER TIL ET BIBLIOTEK

Ideen med et bibliotek er blandt andet at biblioteks-koden ikke skal kunne ses eller ændres i. Istedet skal det bare være muligt at kalde koden uden man behøver at skrive andet end f.eks. "lav knap!". Og hvis knappen skal gøre et eller andet når den bliver trykket på, skal det være muligt at spørge "er du trykket på?" og så kan man gøre det man ønsker at gøre hvis svaret er "ja!". osv.

Krav til knap-biblioteks-koden:

- "Knap koden" skal ikke blandes sammen med "ikke knap koden",- og man skal ikke behøve ændre den
- Det skal være nemt at lave flere knapper
- Man skal ikke behøve forstå hvordan knap-koden gør det den gør, men kun hvordan man anvender den

Biblioteks-koden skal være ligesom når man kører bil. Man behøver ikke forstå HVORDAN motoren virker når man trykker på speederen eller skifter gear, man skal bare forstå HVAD den gør og når anvender den!

Alt dette er muligt med Objekt orienteret programmering! Knappen skal laves om til en klasse.   
Se følgende eksempel:

```java
// Dette er kode der anvendelse af en toggle-knap fra et "bibliotek"

ToggleKnap  minToggleKnap   = new ToggleKnap(10,30,120,40);
int         counter         = 0;

void setup(){
  size(500,500);
}

void draw(){
  clear();  
  minToggleKnap.tegnKnap();  

  //IKKE DEL AF KNAP - udskrivning af counter!
  fill(255);
  text("knap er tændt " + counter + " gange",10,300);
}

void mousePressed(){
  minToggleKnap.registrerKlik();
  
  //IKKE DEL AF KNAP - optælning af counter!
  if(minToggleKnap.knapOn){
    counter++;  
  } 
}

void mouseReleased(){

}
```
