# Forløb 8
## Biblioteket pakkes ned i en Jar

Jeres bibliotek er ikke et rigtigt bibliotek før det er pakket ned i en JAR-file.
JAR står for "Java Archive", og processing er jo bare Java nedenunder motorhjelmen, så en JAR fil er altså et måde at lave et bibliotek på i processing.


------------------------------------------------------------------------------------------------------------------------------------------------------


## Lav din egen JAR
Det er muligt selv at konstruere en JAR fil vha. i en konsol, men vi vælger en lidt lettere metode og får processing til det.    

Metoden har jeg beskrevet nedenfor:   
1. Gå til menuen "File" vælg "Export Application..."
2. Der kommer en dialog-boks op, her skal du vælge "windows" (også selv om du anvender mac eller noget andet)
3. Når processing er færdig med at eksportere applikationen åbner den automatisk den mappe hvor eksporten er placeret
4. I eksport-mappen vælger du mappen "application.windows64" og derefter mappen "lib"
5. I mappen "lib" ligger din JAR fil - den hedder det samme som din applikation

Video forklaring:    
<iframe width="560" height="315" src="https://www.youtube.com/embed/iScvXVpLOAI" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


------------------------------------------------------------------------------------------------------------------------------------------------------


## Overfør din JAR over i en anden applikation
Hele ideen med at pakke alt din biblioteks-kode ned i en JAR er at den nemt kan anvendes af andre, som et slags bibliotek ;-)   

Det eneste man skal gøre, for at anvende en JAR, er at trække JAR'en ind i sin applikation, processing vil nu lava en mappe, der hedder "code" og placere
Jar-filen der, og det er herefter muligt at anvende alt det kode der er inde i JAR-filen.

Video forklaring:   
<iframe width="560" height="315" src="https://www.youtube.com/embed/oxlU4Ghkc08" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


------------------------------------------------------------------------------------------------------------------------------------------------------


## Anvend kode fra en JAR

Nedenfor ses et eksempel på kode der anvender klasser og metoder fra JAR-filen.
Bemærk dog at dine klasser sandsynligvis hedder noget andet!!!:

```java
 //GUIBib er selve bibliotek-programmets navn!
GUIBib bib = new GUIBib();

//Læg mærke til at GUIHandler klassen er "inde" i GUILib,
//derfor denne specielle måde at lave en GUIHandler
GUIBib.GUIHandler handler = bib.new GUIHandler();

//Kanp er også inde i "GUIBib"
GUIBib.Knap k;

void setup(){
  k = handler.createKnap();
}
```


Video forklaring:    
<iframe width="560" height="315" src="https://www.youtube.com/embed/gYuJdr9r1k0" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


------------------------------------------------------------------------------------------------------------------------------------------------------


## Tilpas din processing JAR-kode - så den kan bruges i andre processing programmer!!!!

Hvis man er allerede har prøvet at anvende JAR-filen er man blevet begravet i Exceptions!!!
Men hvorfor???  

#### Problem:
Forklaringen er at den processing-kode der er inde i JAR filene anvender det forkerte processing-objekt!

#### En løsning:
Man bliver nødt til at omskrive koden i sit bibliotek og anvende det på en lidt anderledes måde:

```java
//ØVERST I BIBLIOTEK KODEN
PApplet p;
```
```java
///BIBLIOTEKS KODE, DER ANVENDER PROCESSING !
class Knap{
  void tegnKnap(){
    p.rect(10,10,10,10);  // Husk skriv "p." foran!!
  }
}
```

```java
//KODEN DER ANVENDER Biblioteket
GUIBib bib = new GUIBib();
GUIBib.GUIHandler handler = bib.new GUIHandler();
GUIBib.Knap k;
void setup(){
  bib.p = this;   //Gemmer den "rigtige" processing inde i Biblioteket
  k = handler.createKnap();
}

```

Video forklaring:    
<iframe width="560" height="315" src="https://www.youtube.com/embed/oZEs4unZWo0" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
